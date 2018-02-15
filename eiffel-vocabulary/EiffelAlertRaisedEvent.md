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

# EiffelAlertRaisedEvent (AlerR)
The EiffelAlertRaisedEvent represents an incident that has occurred, technically regarding any topic,
but typically used to communicate any incident or status update regarding the continuous integration 
and delivery pipeline and the systems (e.g IT Monitoring Systems) supporting the pipeline. 
This information can then be favorably displayed in visualization and dashboard applications or used to trigger self healing activities.

## Data Members
### data.heading
__Type:__ String  
__Required:__ Yes  
__Description:__ The heading of the incident.

### data.body
__Type:__ String  
__Required:__ Yes  
__Description:__ The body of the incident.

### data.uri
__Type:__ String  
__Required:__ No  
__Description:__ A URI where further information can be obtained, if available.

### data.entity
__Type:__ String  
__Required:__ No  
__Description:__ The identity of the user or entity that raised the alert.

### data.severity
__Type:__ String  
__Required:__ Yes  
__Legal values:__ MINOR, MAJOR, CRITICAL, BLOCKER, CANCELED
__Description:__ The severity of the incident.The CANCELED value SHOULD only be used when following up a 
previous Alert raised event which should be linked with MODIFIED_ALERT.

##Legal Link Types
### CAUSE
__Legal targets:__ Any  
__Multiple allowed:__ Yes  
__Description:__ Identifies a cause of the event occurring. SHOULD not be used in conjunction with __CONTEXT__: individual events providing __CAUSE__ within a larger context gives rise to ambiguity. It is instead recommended to let the root event of the context declare __CAUSE__.  

### MODIFIED_ALERT
__Legal targets:__ [EiffelAlertRaisedEvent](https://github.com/Ericsson/eiffel-operations-extension/blob/master/eiffel-vocabulary/EiffelAlertRaisedEvent.md)  
__Multiple allowed:__ No  
__Description:__ Identifies a ALERT modified. Should be used only when severity is CANCELED.