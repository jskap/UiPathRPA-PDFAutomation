# UiPathRPA-PDFAutomation
Consider a native PDF document with dynamic information like the one attached. Use anchor base automation to get the DATE 
and the name from the BILL TO values from the invoice.

In UiPath Studio, create a new project and perform the following steps:

Attach to the PDF Reader window using an Attach Window activity.

  --  Drag an Anchor Base container inside the Do block:

      --  on the left side, we’ll drag a Find Element activity to select our anchor.

          --  we click Indicate on screen.

          -- we click the DATE label next to the actual date we are trying to get.

      --  on the right side, we’ll drag a Get Text activity to read the value we want.

          --  we click Indicate on screen.

          --  we click the actual date field we are trying to get (e.g. 6/6/20##).

          --  note that the selector only contains a tag with a type attribute.

          --  in the Output property, create a new variable to hold the read value.

      --  in the properties of the Anchor Base container, set the AnchorPosition to Left or Auto.

For the second anchor-based reading, we use a similar method.

 -- we drag an Anchor Base container inside the Do block.

      --  on the left side, drag a Find Element activity to select our anchor.

          --  we click Indicate on screen.

          --  we click the BILL TO label on top of the address we are trying to get.

      --  on the right side, drag a Get Text activity to read the value we want.

          --  we click Indicate on screen.

          --  we click the name we are trying to get (e.g. IDES AG Frankfurt).

          -- note that the selector only contains a tag with a role attribute.

          --  in the Output property, create a new variable to hold the read value.
          
      --  in the Anchor Base container, set the AnchorPosition property to Top or Auto.
