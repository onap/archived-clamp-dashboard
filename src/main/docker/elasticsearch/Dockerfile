### 
# ============LICENSE_START======================================================= 
# ONAP CLAMP 
# ================================================================================ 
# Copyright (C) 2020 AT&T Intellectual Property. All rights 
#                             reserved. 
# ================================================================================ 
# Licensed under the Apache License, Version 2.0 (the "License"); 
# you may not use this file except in compliance with the License. 
# You may obtain a copy of the License at 
# 
# http://www.apache.org/licenses/LICENSE-2.0 
# 
# Unless required by applicable law or agreed to in writing, software 
# distributed under the License is distributed on an "AS IS" BASIS, 
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. 
# See the License for the specific language governing permissions and 
# limitations under the License. 
# ============LICENSE_END============================================ 
# =================================================================== 
#
###

FROM amazon/opendistro-for-elasticsearch:1.3.0

# Default clamp certificates for ES communication
COPY config/ca-certs.pem /usr/share/elasticsearch/config/root-ca.pem
COPY config/clamp.pem /usr/share/elasticsearch/config/esnode.pem
COPY config/clamp-key.pem /usr/share/elasticsearch/config/esnode-key.pem
COPY config/clamp.pem /usr/share/elasticsearch/config/kirk.pem
COPY config/clamp-key.pem /usr/share/elasticsearch/config/kirk-key.pem

# replace default elasticsearch.yml conf file
COPY config/elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml

# replace default security roles and initial users
COPY securityconfig/roles.yml /usr/share/elasticsearch/plugins/opendistro_security/securityconfig/roles.yml
COPY securityconfig/internal_users.yml /usr/share/elasticsearch/plugins/opendistro_security/securityconfig/internal_users.yml


