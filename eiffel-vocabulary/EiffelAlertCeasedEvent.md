s<!---
   Copyright 2017 Ericsson AB.
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
### data.heading
__Type:__ String  
__Required:__ Yes  
__Description:__ The heading of the ceased incident.

### data.body
__Type:__ String  
__Required:__ No  
__Description:__ The body of the ceased incident.

### data.entity
__Type:__ String  
__Required:__ No  
__Description:__ The identity of the entity that ceased the incident.

### data.uri
__Type:__ String  
__Required:__ No  
__Description:__ A URI where further information can be obtained, if available.

##Legal Link Types
### CAUSE
__Legal targets:__ Any  
__Multiple allowed:__ Yes  
__Description:__ Identifies a cause of the event occurring. SHOULD not be used in conjunction with __CONTEXT__: individual events providing __CAUSE__ within a larger context gives rise to ambiguity. It is instead recommended to let the root event of the context declare __CAUSE__.  