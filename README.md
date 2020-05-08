# TQA

**How to install transformers library?**
* sudo pip3 install transformers
* **or**
* git clone https://github.com/huggingface/transformers
* cd transformers
* pip install .

**Training**
* export TQA_DIR='./data'

* python3 run_multiple_choice.py \
--model_type roberta \
--task_name swag \
--model_name_or_path roberta-base \
--do_train \
--do_eval \
--do_lower_case \
--data_dir $TQA_DIR \
--learning_rate 5e-5 \
--num_train_epochs 3 \
--max_seq_length 80 \
--output_dir models_bert/swag_base \
--per_gpu_eval_batch_size=16 \
--per_gpu_train_batch_size=16 \
--gradient_accumulation_steps 2 \
--overwrite_output