# Creating a redundancy group template

To create a redundancy group template:

1. Right-click the view in the Surveyor where you want to create the new redundancy group template and select *New \> Redundancy group template.*

2. On the first tab page, enter a name. Optionally, you can also add a description, and select the DMA that has to host the redundancy group template.

3. On the *Configuration* tab page, in the *Protocol* section, select the protocol and a protocol version for the elements that will be added to the redundancy group template.

4. If you wish to use software redundancy:

    1. In the *Redundancy mode* section, click the underlined section and select *intervene in the switching (software redundancy)*.

    2. On the same line, click the underlined section to the right of *redundancy mode* and specify the redundancy mode.

        > [!NOTE]
        > For more information on the different redundancy modes and on how to switch between redundancy modes after the redundancy group has been created, see [Changing the redundancy mode](Changing_the_redundancy_mode.md).

    3. If you want the conditions of the switching logic to also be checked when a user does a manual switch, in the *Redundancy mode* section, select *On manual switchover to a backup, also check the conditions from the switching logic*.

    4. In the *Switching logic* section, click add and select *Add switching logic*. A first empty switching condition will then be displayed.

    5. Configure the switching condition by clicking the underlined fields and selecting the appropriate values, and add more conditions with the *Add* field below the condition if necessary:

        - The switchover and switchback actions can be triggered by an alarm, an element state or a parameter value. If connectivity has been configured on the DMA, they can also be triggered based on whether an element is in the active connectivity chain.

            > [!TIP]
            > See also:
            > [Defining connectivity chains in XML files](../../part_3/DCF/Defining_connectivity_chains_in_XML_files.md)

            > [!NOTE]
            > Prior to DataMiner 9.5.5, the connectivity path is only calculated starting from an internal connection, so that a connectivity chain path with only external connections cannot cause a redundancy group to switch. From DataMiner 9.5.5 onwards, this restriction no longer applies.

        - With the last field of a condition, you can indicate whether the condition has to persist for a certain time or not before its result is triggered.

        - Next to *by executing*, you can configure what should happen during a switch: a parameter set or an Automation script execution.

5. In the *Switching Detection* section, specify when a switchover or switchback operation will be considered finished:

    1. Click *Add* and select *Add switching detection* to create a pair of conditions for switchover and switchback.

    2. Configure the conditions by clicking the underlined fields and selecting the appropriate values. The conditions can check whether an alarm exists, whether an element is in a particular state or whether a parameter has a particular value.

    3. If more conditions are necessary, click *Add* and configure the new conditions as described above.

6. On the *Views* tab page, specify the view(s) where the redundancy group template should be created.

7. Click the *Create* button in the lower right corner.