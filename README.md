# chat-robot

## 基于rasa的一个特别简单的闲聊机器人

![image](https://github.com/Amy2017new/chat-robot/blob/main/IMG/chat-robot.png)


## nlu 和 core 的测试结果如下

➜  chat-robot git:(main) ✗ rasa test nlu
2021-01-07 11:16:36 INFO     rasa.model  - Loading model models/20210107-094606.tar.gz...
2021-01-07 11:16:40 INFO     rasa.nlu.test  - Running model for predictions:
  0%|                                                                                                                                 | 0/29 [00:00<?, ?it/s]Building prefix dict from the default dictionary ...
Loading model from cache /var/folders/xc/5m3vgt7s24xfr9mpvx1_xmjdnhphgd/T/jieba.cache
Loading model cost 0.699 seconds.
Prefix dict has been built successfully.
100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 29/29 [00:00<00:00, 34.63it/s]
2021-01-07 11:16:41 INFO     rasa.nlu.test  - Intent evaluation results:
2021-01-07 11:16:41 INFO     rasa.nlu.test  - Intent Evaluation: Only considering those 29 examples that have a defined intent out of 29 examples.
2021-01-07 11:16:41 INFO     rasa.nlu.test  - Classification report saved to results/intent_report.json.
2021-01-07 11:16:41 INFO     rasa.nlu.test  - Incorrect intent predictions saved to results/intent_errors.json.
2021-01-07 11:16:41 INFO     rasa.utils.plotting  - Confusion matrix, without normalization:
[[ 3  0  0  0  1  0  0]
 [ 0  2  0  0  0  0  0]
 [ 0  0  3  0  0  0  0]
 [ 0  0  0  4  0  0  0]
 [ 0  0  0  0 12  0  0]
 [ 0  0  0  0  0  2  0]
 [ 0  0  0  0  0  0  2]]
2021-01-07 11:16:43 INFO     rasa.nlu.test  - Entity evaluation results:
➜  chat-robot git:(main) ✗ rasa test core
2021-01-07 11:16:55 INFO     rasa.model  - Loading model models/20210107-094606.tar.gz...
Processed story blocks: 100%|██████████████████████████████████████████████████████████████████████████████████| 4/4 [00:00<00:00, 2765.78it/s, # trackers=1]
2021-01-07 11:17:02 INFO     rasa.core.test  - Evaluating 4 stories
Progress:
100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 4/4 [00:00<00:00, 45.93it/s]
2021-01-07 11:17:02 INFO     rasa.core.test  - Finished collecting predictions.
2021-01-07 11:17:02 INFO     rasa.core.test  - Evaluation Results on CONVERSATION level:
2021-01-07 11:17:02 INFO     rasa.core.test  - 	Correct:          1 / 4
2021-01-07 11:17:02 INFO     rasa.core.test  - 	F1-Score:         0.400
2021-01-07 11:17:02 INFO     rasa.core.test  - 	Precision:        1.000
2021-01-07 11:17:02 INFO     rasa.core.test  - 	Accuracy:         0.250
2021-01-07 11:17:02 INFO     rasa.core.test  - 	In-data fraction: 1
2021-01-07 11:17:02 INFO     rasa.core.test  - Stories report saved to results/story_report.json.
2021-01-07 11:17:03 INFO     rasa.core.test  - Evaluation Results on ACTION level:
2021-01-07 11:17:03 INFO     rasa.core.test  - 	Correct:          19 / 22
2021-01-07 11:17:03 INFO     rasa.core.test  - 	F1-Score:         0.885
2021-01-07 11:17:03 INFO     rasa.core.test  - 	Precision:        0.909
2021-01-07 11:17:03 INFO     rasa.core.test  - 	Accuracy:         0.864
2021-01-07 11:17:03 INFO     rasa.core.test  - 	In-data fraction: 1
2021-01-07 11:17:03 INFO     rasa.utils.plotting  - Confusion matrix, without normalization:
[[0 0 0 0 0 0 0]
 [1 9 0 0 0 0 0]
 [0 0 3 0 0 0 0]
 [2 0 0 0 0 0 0]
 [0 0 0 0 1 0 0]
 [0 0 0 0 0 4 0]
 [0 0 0 0 0 0 2]]
