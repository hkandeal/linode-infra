#
# Copyright (c) 2023 The Emirates Group. All Rights Reserved.
# The information specified here is confidential and remains property of the Emirates Group.
# groupId     - com.emirates.kong
# artifactId  - kong image
# name        - Kong image
# description - Image for Kong Gateway
# 2023
#
 
FROM kong:3.4
USER root
ENV KONG_DATABASE off
RUN luarocks install xml2lua
RUN luarocks install lua-resty-openidc
RUN luarocks install kong-oidc
 
USER kong