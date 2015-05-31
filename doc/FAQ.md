FAQ
===

Less commonly known current limitations of the BC XML Template Override Conditions solution

# Use only the match conditions you require and not more

When editing your override.ini rules to use the new match conditions provided by this kernel class override extension ... only use the match conditions you require.


# Object match condition more accurate than Node match condition

Warning: Due to limitations at the time of creation of this solution. While making this solution we used main_node instead of the actual current node since we did not know of a way to get the actual node used when rendering an object (re: multi location objects), we used the object's main node to provide the node match condition.

Obtaining a node used from a content object alone is possibly unknowable in our experience and objects can be rendered by object alone.

Therefore using the 'object' match condition is a little more accurate (across all possible usecases) than 'node' match condition usage.


# Template override rule match conditions added

This solution provides the following ezxmltags template override rule match conditions you can use in your override.ini settings:

* Provided by default in eZ Publish:

    * attribute_identifier

* Added by bcxmltemplateoverrideconditions:

    *  object
    *  class
    *  class_identifier
    *  remote_id
    *  node
    *  node_remote_id
    *  depth
    *  url_alias
    *  parent_node
    *  parent_node_remote_id
    *  parent_object_remote_id
    *  parent_class
    *  parent_class_identifier

**Note**: Additional match conditions can be added by patching the kernel override class and documentation. We support with this solution nearly all possible match conditions (minus state and some other more obscure and rarely used conditions).


# Origin

Based on a kernel patch created by Brookins Consulting: https://gist.github.com/brookinsconsulting/77df6f70fedf7755628b

