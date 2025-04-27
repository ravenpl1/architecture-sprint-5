2025-01-03 09:12:51 INFO     root  - Rasa server is up and running.
2025-01-03 09:12:51 INFO     root  - Enabling coroutine debugging. Loop id 94639956754336.
2025-01-03 09:13:14 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-01-03 09:13:14 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-01-03 09:13:14 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-01-03 09:13:14 DEBUG    rasa.core.tracker_store  - Could not find tracker for conversation ID 'PractikumStudent'.
2025-01-03 09:13:14 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - Starting a new session for conversation ID 'PractikumStudent'.
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_session_start rasa_events=[<rasa.shared.core.events.SessionStarted object at 0x7f9bc14fdcf0>, ActionExecuted(action: action_listen, policy: None, confidence: None)]
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - [debug    ] processor.slots.log            slot_values=     topic: None
        session_started_metadata: None
2025-01-03 09:13:14 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x7f9c09d0a500>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bc1f30a60>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-01-03 09:13:14 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-01-03 09:13:14 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'greet', 'confidence': 0.4263204336166382} parse_data_text=Привет
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 4 events.
2025-01-03 09:13:14 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Привет)]
2025-01-03 09:13:14 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bc1f30a60>}, targets: ['select_prediction'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{}, {'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-01-03 09:13:14 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'utter_greet'
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user text: Привет | previous action name: action_listen
2025-01-03 09:13:14 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
2025-01-03 09:13:14 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_greet'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_greet' based on user intent.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - Predicted next action 'utter_greet' with confidence 1.00.
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x7f9bc14fd270>]
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_greet rasa_events=[BotUttered('Привет! Чем могу помочь в области архитектуры программного обеспечения?', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_greet"}, 1735895594.6077693)]
2025-01-03 09:13:14 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bc1f30a60>}, targets: ['select_prediction'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'utter_greet'}}]
2025-01-03 09:13:14 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
2025-01-03 09:13:14 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-01-03 09:13:14 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-01-03 09:13:14 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-01-03 09:13:14 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-01-03 09:13:14 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-01-03 09:13:14 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-01-03 09:14:00 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-01-03 09:14:00 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-01-03 09:14:00 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-01-03 09:14:00 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-01-03 09:14:00 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x7f9c09d0a500>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bf6a37730>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-01-03 09:14:00 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-01-03 09:14:00 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-01-03 09:14:00 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'ask_architecture', 'confidence': 0.7830374836921692} parse_data_text=Что такое архитектура ПО
2025-01-03 09:14:00 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 10 events.
2025-01-03 09:14:00 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-01-03 09:14:00 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Что такое архитектура ПО)]
2025-01-03 09:14:00 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bf6a37730>}, targets: ['select_prediction'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'utter_greet'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-01-03 09:14:00 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'utter_architecture_response'
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user text: Что такое архитектура ПО | previous action name: action_listen
2025-01-03 09:14:00 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: ask_architecture | previous action name: action_listen
2025-01-03 09:14:00 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_architecture_response'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_architecture_response' based on user intent.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-01-03 09:14:00 DEBUG    rasa.core.processor  - Predicted next action 'utter_architecture_response' with confidence 1.00.
2025-01-03 09:14:00 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x7f9bc14fc5b0>]
2025-01-03 09:14:00 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_architecture_response rasa_events=[BotUttered('Архитектура ПО включает выбор структур, которые обеспечивают масштабируемость, гибкость и поддерживаемость приложения. Задайте конкретный вопрос по этой теме, и я помогу вам с информацией.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_architecture_response"}, 1735895640.8649538)]
2025-01-03 09:14:00 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bf6a37730>}, targets: ['select_prediction'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-01-03 09:14:00 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
2025-01-03 09:14:00 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-01-03 09:14:00 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-01-03 09:14:00 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-01-03 09:14:00 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-01-03 09:14:00 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-01-03 09:14:00 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-01-03 09:14:00 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-01-03 09:14:00 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-01-03 09:14:18 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-01-03 09:14:18 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-01-03 09:14:18 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-01-03 09:14:18 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-01-03 09:14:18 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x7f9c09f0e290>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bc1533e20>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-01-03 09:14:18 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-01-03 09:14:18 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-01-03 09:14:18 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'request_info', 'confidence': 0.5396097898483276} parse_data_text=Как её реализовать
2025-01-03 09:14:18 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 16 events.
2025-01-03 09:14:18 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-01-03 09:14:18 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Как её реализовать)]
2025-01-03 09:14:18 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bc1533e20>}, targets: ['select_prediction'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}, {'user': {'intent': 'request_info'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-01-03 09:14:18 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user text: Как её реализовать | previous action name: action_listen
2025-01-03 09:14:18 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: request_info | previous action name: action_listen
2025-01-03 09:14:18 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_ask_more'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_ask_more' based on user intent.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-01-03 09:14:18 DEBUG    rasa.core.processor  - Predicted next action 'utter_ask_more' with confidence 1.00.
2025-01-03 09:14:18 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x7f9bc14ff580>]
2025-01-03 09:14:18 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_ask_more rasa_events=[BotUttered('Что именно вас интересует в архитектуре программного обеспечения?', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_ask_more"}, 1735895658.6414242)]
2025-01-03 09:14:18 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bc1533e20>}, targets: ['select_prediction'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'request_info'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'request_info'}, 'prev_action': {'action_name': 'utter_ask_more'}}]
2025-01-03 09:14:18 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: request_info | previous action name: action_listen
[state 6] user intent: request_info | previous action name: utter_ask_more
2025-01-03 09:14:18 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-01-03 09:14:18 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-01-03 09:14:18 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-01-03 09:14:18 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-01-03 09:14:18 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-01-03 09:14:18 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-01-03 09:14:18 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-01-03 09:14:18 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-01-03 09:14:37 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-01-03 09:14:37 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-01-03 09:14:37 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-01-03 09:14:37 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-01-03 09:14:37 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x7f9c09f0e290>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bc1533e20>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-01-03 09:14:37 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-01-03 09:14:37 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-01-03 09:14:37 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'goodbye', 'confidence': 0.6584542989730835} parse_data_text=Пока
2025-01-03 09:14:37 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 22 events.
2025-01-03 09:14:37 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-01-03 09:14:37 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Пока)]
2025-01-03 09:14:37 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bc1533e20>}, targets: ['select_prediction'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'request_info'}, 'prev_action': {'action_name': 'utter_ask_more'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-01-03 09:14:37 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: request_info | previous action name: action_listen
[state 6] user intent: request_info | previous action name: utter_ask_more
[state 7] user text: Пока | previous action name: action_listen
2025-01-03 09:14:37 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: request_info | previous action name: action_listen
[state 6] user intent: request_info | previous action name: utter_ask_more
[state 7] user intent: goodbye | previous action name: action_listen
2025-01-03 09:14:37 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_goodbye'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_goodbye' based on user intent.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-01-03 09:14:37 DEBUG    rasa.core.processor  - Predicted next action 'utter_goodbye' with confidence 1.00.
2025-01-03 09:14:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x7f9bc14fe620>]
2025-01-03 09:14:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_goodbye rasa_events=[BotUttered('До свидания! Если появятся вопросы по архитектуре ПО, обращайтесь.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_goodbye"}, 1735895677.8224456)]
2025-01-03 09:14:37 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7f9bc1533e20>}, targets: ['select_prediction'] and ExecutionContext(model_id='af32884d7a9942b6ad2c7dcd1294f916', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}]
2025-01-03 09:14:37 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: request_info | previous action name: action_listen
[state 6] user intent: request_info | previous action name: utter_ask_more
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
2025-01-03 09:14:37 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-01-03 09:14:37 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-01-03 09:14:37 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-01-03 09:14:37 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-01-03 09:14:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-01-03 09:14:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-01-03 09:14:37 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-01-03 09:14:37 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
