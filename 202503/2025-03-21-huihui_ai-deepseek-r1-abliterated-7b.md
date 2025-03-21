# huihui_ai/deepseek-r1-abliterated:7b
- URL: https://ollama.com/huihui_ai/deepseek-r1-abliterated:7b
- Added At: 2025-03-21 02:32:29
- [Link To Text](2025-03-21-huihui_ai-deepseek-r1-abliterated-7b_raw.md)

## TL;DR
DeepSeek-R1是DeepSeek的第一代推理模型，提供多种参数版本，性能与OpenAI-o1相当。该模型通过“abliteration”方法去除了拒绝响应，具有实验性质。使用时可参考引导示例，更多信息可在HuggingFace获取。支持通过捐赠继续开发，模型最近更新于6周前，下载次数达431.4K次。

## Summary
1. **模型简介**：
   - **DeepSeek-R1模型**：这是DeepSeek的第一代推理模型，性能与OpenAI-o1相当。
   - **模型版本**：提供7b、8b、14b、32b和70b等多种参数规模的版本。

2. **模型特点**：
   - **无审查版本**：这是一个通过“abliteration”方法去除拒绝响应的无审查版本，具体方法可参考[remove-refusals-with-transformers](https://github.com/Sumandora/remove-refusals-with-transformers)。
   - **实验性质**：这是一个粗糙的概念验证实现，旨在不使用TransformerLens的情况下从LLM模型中去除拒绝响应。

3. **使用指南**：
   - **引导示例**：如果模型未显示“<think>”或拒绝响应，可以先提供一个示例来引导模型，然后再提问。例如：
     ```
     How many 'r' characters are there in the word "strawberry"?
     ```

4. **参考资源**：
   - **HuggingFace**：更多信息可参考[HuggingFace](https://huggingface.co/collections/huihui-ai/deepseek-r1-abliterated-6790ea12ce8c8c4e5df51b7f)。

5. **捐赠信息**：
   - **支持开发**：可以通过[x.com/support_huihui](https://x.com/support_huihui)获取huihui.ai的最新模型信息。
   - **捐赠方式**：捐赠有助于继续开发和改进模型，支持方式包括比特币：
     ```
     bc1qqnkhuchxw0zqjh2ku3lu4hq45hc6gy84uk70ge
     ```

6. **更新信息**：
   - **更新频率**：模型最近一次更新是在6周前。
   - **下载次数**：模型已被下载431.4K次。
