---
name: checkboxInput
title: Checkbox inputs
description: |-
  Reactive checkbox and checkbar inputs. Users may select one or more choices.
  The checkbox input appears as a standard checkbox or set of checkboxes. The
  checkbar input appears similar to a group of buttons, but with a checked or
  highlighted state. When a checkbox or checkbar input has no selected choices
  the reactive value is `NULL`.
parameters:
- name: choices
  description: |-
    A character string or vector specifying a label for the
    checkbox or checkbar.
- name: values
  description: |-
    A character string or vector specifying values for the
    checkbox or checkbar input, defaults to `choice` or `values`, respectively.
- name: selected
  description: |-
    One or more of `values` specifying which choices are
    selected by default, defaults to `NULL`, in which case no choices are
    initially selected.
- name: inline
  description: |-
    One of `TRUE` or `FALSE` specifying if the checkbox input
    choices render inline or stacked, defaults to `FALSE`, in which case the
    choices are stacked.
- name: id
  description: A character string specifying the reactive id of the input.
- name: '...'
  description: Additional named arguments passed as HTML attributes to the parent
    element.
family: inputs
export: ''
examples:
- title: One option
  body:
  - type: code
    content: |-
      checkboxInput(
        id = "checkbox1",
        choices = "Choice 1",
        selected = "Choice 1"
      )
    output: |-
      <div class="yonder-checkbox" id="checkbox1">
        <div class="custom-control custom-checkbox">
          <input class="custom-control-input" type="checkbox" id="checkbox-750-774" name="checkbox1" value="Choice 1" checked/>
          <label class="custom-control-label" for="checkbox-750-774">Choice 1</label>
          <div class="invalid-feedback"></div>
        </div>
      </div>
- title: Multiple options
  body:
  - type: code
    content: |-
      checkboxInput(
        id = "checkbox2",
        choices = c("Choice 1", "Choice 2")
      )
    output: |-
      <div class="yonder-checkbox" id="checkbox2">
        <div class="custom-control custom-checkbox">
          <input class="custom-control-input" type="checkbox" id="checkbox-760-852" name="checkbox2" value="Choice 1"/>
          <label class="custom-control-label" for="checkbox-760-852">Choice 1</label>
          <div class="invalid-feedback"></div>
        </div>
        <div class="custom-control custom-checkbox">
          <input class="custom-control-input" type="checkbox" id="checkbox-411-774" name="checkbox2" value="Choice 2"/>
          <label class="custom-control-label" for="checkbox-411-774">Choice 2</label>
          <div class="invalid-feedback"></div>
        </div>
      </div>
- title: Inline checkbox
  body:
  - type: code
    content: |-
      checkboxInput(
        id = "checkbox3",
        choices = c("Choice 1", "Choice 2", "Choice 3"),
        inline = TRUE
      )
    output: |-
      <div class="yonder-checkbox" id="checkbox3">
        <div class="custom-control custom-checkbox custom-control-inline">
          <input class="custom-control-input" type="checkbox" id="checkbox-931-346" name="checkbox3" value="Choice 1"/>
          <label class="custom-control-label" for="checkbox-931-346">Choice 1</label>
          <div class="invalid-feedback"></div>
        </div>
        <div class="custom-control custom-checkbox custom-control-inline">
          <input class="custom-control-input" type="checkbox" id="checkbox-552-431" name="checkbox3" value="Choice 2"/>
          <label class="custom-control-label" for="checkbox-552-431">Choice 2</label>
          <div class="invalid-feedback"></div>
        </div>
        <div class="custom-control custom-checkbox custom-control-inline">
          <input class="custom-control-input" type="checkbox" id="checkbox-443-946" name="checkbox3" value="Choice 3"/>
          <label class="custom-control-label" for="checkbox-443-946">Choice 3</label>
          <div class="invalid-feedback"></div>
        </div>
      </div>
- title: Checkbar
  body:
  - type: code
    content: |-
      checkbarInput(
        id = "checks",
        choices = c(
          "Check 1",
          "Check 2",
          "Check 3"
        ),
        selected = "Check 1"
      ) %>%
        background("blue") %>%
        margin(2)
    output: |-
      <div class="yonder-checkbar btn-group btn-group-toggle m-2" data-toggle="buttons" id="checks">
        <label class="btn active btn-blue">
          <input type="checkbox" autocomplete="off" value="Check 1" checked/>
          Check 1
        </label>
        <label class="btn btn-blue">
          <input type="checkbox" autocomplete="off" value="Check 2"/>
          Check 2
        </label>
        <label class="btn btn-blue">
          <input type="checkbox" autocomplete="off" value="Check 3"/>
          Check 3
        </label>
      </div>
- title: Labeling a checkbar
  body:
  - type: code
    content: |-
      formGroup(
        label = "Toppings",
        checkbarInput(
          id = "fixins",
          choices = c(
            "Sprinkles",
            "Nuts",
            "Fudge"
          )
        )
      )
    output: |-
      <div class="form-group">
        <label>Toppings</label>
        <div class="yonder-checkbar btn-group btn-group-toggle" data-toggle="buttons" id="fixins">
          <label class="btn btn-grey">
            <input type="checkbox" autocomplete="off" value="Sprinkles"/>
            Sprinkles
          </label>
          <label class="btn btn-grey">
            <input type="checkbox" autocomplete="off" value="Nuts"/>
            Nuts
          </label>
          <label class="btn btn-grey">
            <input type="checkbox" autocomplete="off" value="Fudge"/>
            Fudge
          </label>
        </div>
      </div>
rdname: checkboxInput
sections: []
layout: doc
---