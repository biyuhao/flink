---
title: "Test Dependencies"
weight: 6
type: docs
---
<!--
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->

# Dependencies for Testing 

Flink provides utilities for testing your job that you can add as dependencies.

## DataStream API Test Dependencies

You need to add the following dependencies if you want to develop tests for a job built with the 
DataStream API:

{{< artifact flink-test-utils withTestScope >}}
{{< artifact flink-runtime withTestScope >}}

For more information on how to use these utilities, check out the section on [DataStream API testing]({{< ref "docs/dev/datastream/testing" >}})

## Table Program Test Dependencies

If you want to test the Table API & SQL programs locally within your IDE, you can add the following 
dependency:

{{< artifact flink-table-test-utils withTestScope >}}

This will automatically bring in the query planner and the runtime, required respectively to plan 
and execute the queries.
