| Task | Model | Classification (Success/Failure) | Observation (What actually happened?) | Why did this happen? (Architectural Reason) |
| :--- | :--- | :--- | :--- | :--- |
| Generation | BERT | Failure | Failed to generate coherent text; produced errors or meaningless output. | BERT is an encoder-only model and is not trained for autoregressive text generation. |
| Generation | RoBERTa | Failure | Unable to generate meaningful text, showing behavior similar to BERT. | RoBERTa is also an encoder-only model without a decoder for sequence generation. |
| Generation | BART | Success | Generated fluent and contextually relevant continuation of the given prompt. | BART uses an encoder–decoder architecture designed for sequence-to-sequence generation tasks. |
| Fill-Mask | BERT | Success | Correctly predicted masked words such as “create” and “generate.” | BERT is trained using Masked Language Modeling (MLM), making it well suited for this task. |
| Fill-Mask | RoBERTa | Success | Predicted accurate and contextually appropriate masked tokens. | RoBERTa improves upon MLM training using more data and better optimization strategies. |
| Fill-Mask | BART | Partial | Produced reasonable predictions but with less consistency than BERT or RoBERTa. | BART is trained using denoising objectives rather than explicit masked language modeling. |
| QA | BERT | Partial | Extracted relevant keywords from the context but answers were brief or incomplete. | The model is not fine-tuned on a question-answering dataset like SQuAD. |
| QA | RoBERTa | Partial | Provided slightly clearer answers but still lacked detailed explanations. | Better pretraining improves understanding, but absence of QA-specific fine-tuning limits performance. |
| QA | BART | Partial | Generated readable answers, but accuracy varied across questions. | Encoder–decoder structure helps answer formulation, but no QA-specific fine-tuning was applied. |

