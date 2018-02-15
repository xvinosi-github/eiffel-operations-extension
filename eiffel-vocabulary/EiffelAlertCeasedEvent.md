<!---
   Copyright 2018 Ericsson AB.
   For a full list of individual contributors, please see the commit history.

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
--->

# EiffelAlertCeasedEvent (AlerC)
The EiffelAlertCeasedEvent represents, that an incident which was ongoing (e.g an IT Infrastructure failure) has now come to an end and has ceased.
The EiffelAlertCeasedEvent event is typically used to communicate that a previously raised incident (using a EiffelAlertRaisedEvent) has been resolved and is not longer ongoing.
This information can then be favorably displayed in visualization and dashboard applications.

## Data Members
### data.entity
__Type:__ String  
__Required:__ No  
__Description:__ The identity of the user or entity that ceased the alert.

### data.uri
__Type:__ String  
__Required:__ No  
__Description:__ A URI where further information can be obtained, if available.

##Legal Link Types
### ALERT
__Legal targets:__ [EiffelAlertRaisedEvent](https://github.com/Ericsson/eiffel-operations-extension/blob/master/eiffel-vocabulary/EiffelAlertRaisedEvent.md)  
__Multiple allowed:__ No  
__Description:__ Identifies a ALERT which has been ceased.