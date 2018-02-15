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

# EiffelAlertAcknowledgedEvent (AlerA)
The EiffelAlertAcknowledgedEvent is used to declare that an EiffelAlertRaisedEvent has been received & acknowledged by a person or a machine.

## Data Members
### data.acknowledgement
__Type:__ String  
__Required:__ Yes  
__Description:__ The Acknowledgement response.

### data.entity
__Type:__ String  
__Required:__ No  
__Description:__ The identity of the user or entity that acknowledged the alert.

### data.uri
__Type:__ String  
__Required:__ No  
__Description:__ A URI where further information can be obtained, if available.

##Legal Link Types
### ALERT
__Legal targets:__ [EiffelAlertRaisedEvent](https://github.com/Ericsson/eiffel-operations-extension/blob/master/eiffel-vocabulary/EiffelAlertRaisedEvent.md)  
__Multiple allowed:__ No  
__Description:__ Identifies a ALERT which has been acknowledged.