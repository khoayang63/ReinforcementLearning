# 🤖 Reinforcement Learning (RL) & LLM Alignment

Chào mừng bạn đến với kho lưu trữ thực hành về **Học tăng cường (Reinforcement Learning - RL)**! 

Đây là nơi tổng hợp các mã nguồn thực nghiệm từ các thuật toán RL cổ điển trong game cho đến các phương pháp căn chỉnh mô hình ngôn ngữ lớn (LLM Alignment) hiện đại nhất hiện nay. Dự án sử dụng các thư viện phổ biến trong hệ sinh thái Hugging Face như `transformers`, `peft`, và `trl`.

---

## 📌 Nội dung chính của Repository

Dự án được chia làm 2 chủ đề lớn:

### 1. Học tăng cường cổ điển (Classic RL)
* **[DDQN.ipynb](./DDQN.ipynb)**: Huấn luyện Rắn săn mồi (Snake Game) tự chơi trên lưới 10x10 bằng thuật toán **Double Deep Q-Network (DDQN)**.
* **[PPO.ipynb](./PPO.ipynb)**: Nâng cấp game Rắn săn mồi với thuật toán **Proximal Policy Optimization (PPO)** dạng Actor-Critic kết hợp kỹ thuật tinh chỉnh phần thưởng (Reward Shaping) giúp mô hình hội tụ siêu nhanh.

### 2. Căn chỉnh LLM bằng Học tăng cường (Modern LLM Alignment)
* **[LoRA_pipeline.ipynb](./LoRA_pipeline.ipynb)**: Hướng dẫn chi tiết cách tinh chỉnh hiệu quả tham số (PEFT) cho mô hình Llama-3.2-1B bằng kỹ thuật **LoRA** và lượng hóa **QLoRA 4-bit** để chạy được trên GPU cá nhân.
* **[qwen2_5_1_5b_dpo_finetune.ipynb](./qwen2_5_1_5b_dpo_finetune.ipynb)**: Quy trình 2 bước căn chỉnh hành vi LLM theo ý muốn con người: huấn luyện **SFT** học theo mẫu $\rightarrow$ tối ưu hóa ưu tiên bằng **DPO (Direct Preference Optimization)**.
* **[GRPO.ipynb](./GRPO.ipynb)**: Thực hành thuật toán **GRPO (Group Relative Policy Optimization)** - phương pháp tối ưu hóa nhóm tương đối đột phá được DeepSeek-R1 sử dụng để huấn luyện mô hình tự suy luận Toán học bằng Tiếng Việt.

---

## 🛠️ Các thư viện cốt lõi sử dụng

Để thực hiện các dự án RL này, chúng ta sử dụng các thư viện cơ bản và mạnh mẽ nhất hiện nay:
* 🤗 **`transformers`**: Thư viện nền tảng của Hugging Face để tải và làm việc với các mô hình ngôn ngữ lớn (Qwen, Llama).
* 🏷️ **`peft` (Parameter-Efficient Fine-Tuning)**: Giúp đóng băng mô hình gốc và chỉ huấn luyện một số lượng nhỏ tham số (LoRA Adapter), giúp tiết kiệm cực kỳ nhiều bộ nhớ GPU.
* 🚀 **`trl` (Transformer Reinforcement Learning)**: Thư viện chuyên biệt cung cấp các Trainer tối ưu hóa bằng RL cho LLM như `DPOTrainer` và `GRPOTrainer`.
* 💾 **`bitsandbytes`**: Lượng hóa mô hình về dạng 4-bit/8-bit để chạy mượt mà ngay cả trên các GPU cấu hình thấp (như Tesla T4 16GB).

---

