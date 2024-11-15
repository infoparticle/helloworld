* General Syntax:
#+BEGIN_SRC
opr-assign <CONNECTION_INFO> -create_assignment_by_template <-name <Policy Name> -node_list <Node List> | -node_group <Node Group>> [-parameter_value <Parameter=<Value>>]* [-output <Path to the output file>] [-format <Valid values: xml, json, text>] [-verbose]
#+END_SRC

* Examples:

** Create a simple assignment of a policy to a node:
#+BEGIN_SRC bash
opr-assign -create_assignment_by_template -name MyPolicy -node_list MyNode
#+END_SRC
This creates an assignment for the policy `MyPolicy` to the node `MyNode`.

** Create an assignment with specific parameter values:
#+BEGIN_SRC bash
opr-assign -create_assignment_by_template -name MyPolicy -node_list MyNode -parameter_value para1=value1 -parameter_value para2=value2
#+END_SRC
This assigns the policy `MyPolicy` to `MyNode` while setting the parameters `para1` and `para2` to `value1` and `value2`, respectively.

** Create an assignment for a policy to all nodes in a group:
#+BEGIN_SRC bash
opr-assign -create_assignment_by_template -name MyPolicy -node_group MyNodeGroup
#+END_SRC
This assigns the policy `MyPolicy` to all nodes in the group `MyNodeGroup`.

** Create an assignment and save output in JSON format:
#+BEGIN_SRC bash
opr-assign -create_assignment_by_template -name MyPolicy -node_list MyNode -format json -output /path/to/output.json
#+END_SRC
This creates the assignment and outputs the results in JSON format to the specified file.

** Create an assignment using a draft XML file:
#+BEGIN_SRC bash
opr-assign -create_assignment -input /path/to/draft.xml
#+END_SRC
This creates the assignment from a pre-prepared draft file, often used for complex configurations.

** Enable verbose output for debugging:
#+BEGIN_SRC bash
opr-assign -create_assignment_by_template -name MyPolicy -node_list MyNode -verbose
#+END_SRC
This provides detailed output about the operation for troubleshooting.

Let me know if you need assistance with a specific customization or additional examples!
