---
title: HTMLInputElement
slug: Web/API/HTMLInputElement
---

{{ APIRef("HTML DOM") }}

Интерфейс **`HTMLInputElement`** предоставляет специальные свойства и методы (расширяющие интерфейс {{domxref("HTMLElement")}} который также доступен через наследование) для управления размещением и отображением элементов input.

## Properties

_Наследует свойства своего родителя,_ _{{domxref("HTMLElement")}}._

<table class="standard-table">
  <tbody>
    <tr>
      <th>Название</th>
      <th>Тип</th>
      <th>Описание</th>
    </tr>
    <tr>
      <td><code>accept</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#accept"><code>accept</code></a> HTML
        attribute, containing comma-separated list of file types accepted by the
        server when <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> is
        <code>file</code>.
      </td>
    </tr>
    <tr>
      <td><code>accessKey</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>A single character that switches input focus to the control.</td>
    </tr>
    <tr>
      <td><code>align</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>Alignment of the element.</td>
    </tr>
    <tr>
      <td><code>alt</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#alt"><code>alt</code></a> HTML
        attribute, containing alternative text to use when
        <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> is <code>image.</code>
      </td>
    </tr>
    <tr>
      <td><code>autocapitalize</code> {{experimental_inline}}</td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Defines capitalization behavior for user input. Valid values are
        <code>none</code>, <code>off</code>, <code>characters</code>,
        <code>words</code>, or <code>sentences</code>.
      </td>
    </tr>
    <tr>
      <td><code>autocomplete</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#autocomplete"><code>autocomplete</code></a>
        HTML attribute, indicating whether the value of the control can be
        automatically completed by the browser. Ignored if the value of the
        <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> attribute is hidden,
        checkbox, radio, file, or a button type (button, submit, reset, image).
        Possible values are:
        <ul>
          <li>
            off: The user must explicitly enter a value into this field for
            every use, or the document provides its own auto-completion method;
            the browser does not automatically complete the entry.
          </li>
          <li>
            on: Браузер может автоматически подставить значение основываясь на
            том, что ранее пользователь вводил в данном в предыдущий раз
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><code>autofocus</code></td>
      <td>{{domxref("Boolean")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#autofocus"><code>autofocus</code></a> HTML
        attribute, which specifies that a form control should have input focus
        when the page loads, unless the user overrides it, for example by typing
        in a different control. Only one form element in a document can have the
        <a href="/ru/docs/Web/HTML/Element/input#autofocus"><code>autofocus</code></a> attribute. It cannot be
        applied if the <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> attribute is
        set to <code>hidden</code> (that is, you cannot automatically set focus
        to a hidden control).
      </td>
    </tr>
    <tr>
      <td><code>checked</code></td>
      <td>{{domxref("Boolean")}}</td>
      <td>
        The current state of the element when
        <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> is <code>checkbox</code> or
        <code>radio</code>.
      </td>
    </tr>
    <tr>
      <td><code>defaultChecked</code></td>
      <td>{{domxref("Boolean")}}</td>
      <td>
        The default state of a radio button or checkbox as originally specified
        in HTML that created this object.
      </td>
    </tr>
    <tr>
      <td><code>defaultValue</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        The default value as originally specified in HTML that created this
        object.
      </td>
    </tr>
    <tr>
      <td><code>dirName</code></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td><code>disabled</code></td>
      <td>{{domxref("Boolean")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#disabled"><code>disabled</code></a> HTML
        attribute, indicating that the control is not available for interaction.
        The input values will not be submitted with the form. See also
        <a href="/ru/docs/Web/HTML/Element/input#readonly"><code>readonly</code></a>
      </td>
    </tr>
    <tr>
      <td><code>files</code> {{readonlyInline}}</td>
      <td>{{domxref("FileList")}}</td>
      <td>A list of selected files.</td>
    </tr>
    <tr>
      <td><code>form</code> {{readonlyInline}}</td>
      <td>{{domxref("HTMLFormElement")}}</td>
      <td>
        The containing form element, if this element is in a form. If this
        element is not contained in a form element:
        <ul>
          <li>
            this can be the
            <a href="/ru/docs/Web/HTML/Element/form#id"><code>id</code></a> attribute of any
            {{ HTMLElement("form") }} element in the same document. Even
            if the attribute is set on {{ HTMLElement("input") }},
            this property will be <code>null</code>, if it isn't the id of a
            {{ HTMLElement("form") }} element.
          </li>
          <li>
            this must be <code>null</code>.
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><code>formAction</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#formaction"><code>formaction</code></a>
        HTML attribute, containing the URI of a program that processes
        information submitted by the element. If specified, this attribute
        overrides the <a href="/ru/docs/Web/HTML/Element/form#action"><code>action</code></a> attribute
        of the {{ HTMLElement("form") }} element that owns this element.
      </td>
    </tr>
    <tr>
      <td><code>formEncType</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#formenctype"><code>formenctype</code></a>
        HTML attribute, containing the type of content that is used to submit
        the form to the server. If specified, this attribute overrides the
        <a href="/ru/docs/Web/HTML/Element/form#enctype"><code>enctype</code></a> attribute of the
        {{ HTMLElement("form") }} element that owns this element.
      </td>
    </tr>
    <tr>
      <td><code>formMethod</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#formmethod"><code>formmethod</code></a>
        HTML attribute, containing the HTTP method that the browser uses to
        submit the form. If specified, this attribute overrides the
        <a href="/ru/docs/Web/HTML/Element/form#method"><code>method</code></a> attribute of the
        {{ HTMLElement("form") }} element that owns this element.
      </td>
    </tr>
    <tr>
      <td><code>formNoValidate</code></td>
      <td>{{domxref("Boolean")}}</td>
      <td>
        Reflects the
        <a href="/ru/docs/Web/HTML/Element/input#formnovalidate"><code>formnovalidate</code></a> HTML
        attribute, indicating that the form is not to be validated when it is
        submitted. If specified, this attribute overrides the
        <a href="/ru/docs/Web/HTML/Element/form#novalidate"><code>novalidate</code></a> attribute of the
        {{ HTMLElement("form") }} element that owns this element.
      </td>
    </tr>
    <tr>
      <td><code>formTarget</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#formtarget"><code>formtarget</code></a>
        HTML attribute, containing a name or keyword indicating where to display
        the response that is received after submitting the form. If specified,
        this attribute overrides the
        <a href="/ru/docs/Web/HTML/Element/form#target"><code>target</code></a> attribute of the
        {{ HTMLElement("form") }} element that owns this element.
      </td>
    </tr>
    <tr>
      <td><code>height</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#height"><code>height</code></a> HTML
        attribute, which defines the height of the image displayed for the
        button, if the value of <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> is
        image.
      </td>
    </tr>
    <tr>
      <td><code>indeterminate</code></td>
      <td>{{domxref("Boolean")}}</td>
      <td>Indicates that a checkbox is neither on nor off.</td>
    </tr>
    <tr>
      <td><code>labels</code> {{readonlyInline}}</td>
      <td>{{domxref("NodeList")}}</td>
      <td>
        A list of {{ HTMLElement("label") }} elements that are labels
        for this element.
      </td>
    </tr>
    <tr>
      <td><code>list</code></td>
      <td>{{domxref("HTMLElement")}}</td>
      <td>
        Identifies a list of pre-defined options to suggest to the user. The
        value must be the <strong>id</strong> of a
        {{HTMLElement("datalist")}} element in the same document. The
        browser displays only options that are valid values for this input
        element. This attribute is ignored when the
        <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> attribute's value is
        hidden, checkbox, radio, file, or a button type.
      </td>
    </tr>
    <tr>
      <td><code>max</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#max"><code>max</code></a> HTML
        attribute, containing the maximum (numeric or date-time) value for this
        item, which must not be less than its minimum (<strong>min</strong>
        attribute) value.
      </td>
    </tr>
    <tr>
      <td><code>maxLength</code></td>
      <td><code>long</code></td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#maxlength"><code>maxlength</code></a> HTML
        attribute, containing the maximum length of text (in Unicode code
        points) that the value can be changed to. The constraint is evaluated
        only when the value is changed
        <div class="note">
          <strong>Note:</strong> If you set <code>maxLength</code> to a negative
          value programmatically, an exception will be thrown.
        </div>
      </td>
    </tr>
    <tr>
      <td><code>min</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#min"><code>min</code></a> HTML
        attribute, containing the minimum (numeric or date-time) value for this
        item, which must not be greater than its maximum
        (<a href="/ru/docs/Web/HTML/Element/input#max"><code>max</code></a> attribute) value.
      </td>
    </tr>
    <tr>
      <td><code>multiple</code></td>
      <td></td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#multiple"><code>multiple</code></a> HTML
        attribute, indicating whether more than one value is possible (e.g.,
        multiple files).
      </td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#name"><code>name</code></a> HTML
        attribute, containing a name that identifies the element when submitting
        the form.
      </td>
    </tr>
    <tr>
      <td><code>pattern</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#pattern"><code>pattern</code></a> HTML
        attribute, containing a regular expression that the control's value is
        checked against. The pattern must match the entire value, not just some
        subset. Use the <a href="/ru/docs/Web/HTML/Element/input#title"><code>title</code></a> attribute
        to describe the pattern to help the user. This attribute applies when
        the value of the <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> attribute
        is text, search, tel, url or email; otherwise it is ignored.
      </td>
    </tr>
    <tr>
      <td><code>placeholder</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#placeholder"><code>placeholder</code></a>
        HTML attribute, containing a hint to the user of what can be entered in
        the control. The placeholder text must not contain carriage returns or
        line-feeds. This attribute applies when the value of the
        <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> attribute is text, search,
        tel, url or email; otherwise it is ignored.
      </td>
    </tr>
    <tr>
      <td><code>readOnly</code></td>
      <td>{{domxref("Boolean")}}</td>
      <td>
        <p>
          Reflects the <a href="/ru/docs/Web/HTML/Element/input#readonly"><code>readonly</code></a> HTML
          attribute, indicating that the user cannot modify the value of the
          control.<br />This is ignored if the
          value of the <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> attribute is
          hidden, range, color, checkbox, radio, file, or a button type.
        </p>
      </td>
    </tr>
    <tr>
      <td><code>required</code></td>
      <td>{{domxref("Boolean")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#required"><code>required</code></a> HTML
        attribute, indicating that the user must fill in a value before
        submitting a form.
      </td>
    </tr>
    <tr>
      <td><code>selectionDirection</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        The direction in which selection occurred. This is
        <code>"forward"</code> if selection was performed in the start-to-end
        direction of the current locale, or <code>"backward"</code> for the
        opposite direction. This can also be <code>"none"</code> if the
        direction is unknown."
      </td>
    </tr>
    <tr>
      <td><code>selectionEnd</code></td>
      <td><code>unsigned long</code></td>
      <td>The index of the end of selected text.</td>
    </tr>
    <tr>
      <td><code>selectionStart</code></td>
      <td><code>unsigned long</code></td>
      <td>
        The index of the beginning of selected text. When nothing is selected,
        this is also the caret position inside of the
        <code>&#x3C;input></code> element.
      </td>
    </tr>
    <tr>
      <td><code>size</code></td>
      <td><code>unsigned long</code></td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#size"><code>size</code></a> HTML
        attribute, containing size of the control. This value is in pixels
        unless the value of <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> is text
        or password, in which case, it is an integer number of characters.
        Applies only when
        <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> is set to text, search,
        tel, url, email, or password; otherwise it is ignored.
      </td>
    </tr>
    <tr>
      <td><code>src</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#src"><code>src</code></a> HTML
        attribute, which specifies a URI for the location of an image to display
        on the graphical submit button, if the value of
        <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> is image; otherwise it is
        ignored.
      </td>
    </tr>
    <tr>
      <td><code>step</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#step"><code>step</code></a> HTML
        attribute, which works with<strong
        > </strong><a href="/ru/docs/Web/HTML/Element/input#min"><code>min</code></a> and
        <a href="/ru/docs/Web/HTML/Element/input#max"><code>max</code></a> to limit the increments at
        which a numeric or date-time value can be set. It can be the string any
        or a positive floating point number. If this is not set to any, the
        control accepts only values at multiples of the step value greater than
        the minimum.
      </td>
    </tr>
    <tr>
      <td><code>tabIndex</code></td>
      <td>long</td>
      <td>
        The position of the element in the tabbing navigation order for the
        current document.
      </td>
    </tr>
    <tr>
      <td><code>type</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> HTML
        attribute, indicating the type of control to display. See
        <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> attribute of
        {{ HTMLElement("input") }} for possible values.
      </td>
    </tr>
    <tr>
      <td><code>useMap</code> </td>
      <td>{{domxref("DOMString")}}</td>
      <td>A client-side image map.</td>
    </tr>
    <tr>
      <td><code>validationMessage</code> {{readonlyInline}}</td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        A localized message that describes the validation constraints that the
        control does not satisfy (if any). This is the empty string if the
        control is not a candidate for constraint validation
        (<a href="/ru/docs/Web/HTML/Element/input#willvalidate"><code>willvalidate</code></a> is
        <code>false</code>), or it satisfies its constraints.
      </td>
    </tr>
    <tr>
      <td><code>validity</code> {{readonlyInline}}</td>
      <td>{{domxref("ValidityState")}}</td>
      <td>The validity state that this element is in.</td>
    </tr>
    <tr>
      <td><code>value</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        <p>Current value in the control.</p>
        <div class="note">
          <p>
            <strong>Note: </strong>for certain input types the returned value
            might not match the value the user has entered. For example, if the
            user enters a non-numeric value into an &#x3C;input type="number">,
            the returned value might be an empty string instead.
          </p>
        </div>
      </td>
    </tr>
    <tr>
      <td><code>valueAsDate</code></td>
      <td>{{domxref("Date")}}</td>
      <td>
        The value of the element, interpreted as a date, or <code>null</code> if
        conversion is not possible.
      </td>
    </tr>
    <tr>
      <td><code>valueAsNumber</code></td>
      <td><code>double</code></td>
      <td>
        The value of the element, interpreted as one of the following in order:
        <ol>
          <li>a time value</li>
          <li>a number</li>
          <li><code>NaN</code> if conversion is not possible</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td><code>width</code></td>
      <td>{{domxref("DOMString")}}</td>
      <td>
        Reflects the <a href="/ru/docs/Web/HTML/Element/input#width"><code>width</code></a> HTML
        attribute, which defines the width of the image displayed for the
        button, if the value of <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> is
        image.
      </td>
    </tr>
    <tr>
      <td><code>willValidate</code></td>
      <td>{{domxref("Boolean")}}</td>
      <td>
        Indicates whether the element is a candidate for constraint validation.
        It is <code>false</code> if any conditions bar it from constraint
        validation.
      </td>
    </tr>
  </tbody>
</table>

## Methods

_Inherits methods from its parent,_ _{{domxref("HTMLElement")}}._

<table class="standard-table">
  <tbody>
    <tr>
      <th>Name &#x26; Arguments</th>
      <th>Return</th>
      <th>Description</th>
    </tr>
    <tr>
      <td><code>blur()</code></td>
      <td><code>void</code></td>
      <td>
        Removes focus from input; keystrokes will subsequently go nowhere.
      </td>
    </tr>
    <tr>
      <td><code>checkValidity</code>()</td>
      <td>{{domxref("Boolean")}}</td>
      <td>
        Returns false if the element is a candidate for constraint validation,
        and it does not satisfy its constraints. In this case, it also fires an
        {{event("invalid")}} event at the element. It returns true if
        the element is not a candidate for constraint validation, or if it
        satisfies its constraints.
      </td>
    </tr>
    <tr>
      <td><code>click()</code></td>
      <td><code>void</code></td>
      <td>Simulates a click on the element.</td>
    </tr>
    <tr>
      <td><code>focus()</code></td>
      <td><code>void</code></td>
      <td>Focus on input; keystrokes will subsequently go to this element.</td>
    </tr>
    <tr>
      <td>
        <code>mozSetFileArray(files)</code>{{non-standard_inline}}
      </td>
      <td><code>void</code></td>
      <td>
        Sets the files selected on the input to the given array of
        <code><a href="/ru/docs/Web/API/File">File</a></code> objects. This
        is an alternative to <code>mozSetFileNameArray</code> which can be used
        in frame scripts: a chrome script can
        <a href="/ru/docs/Extensions/Using_the_DOM_File_API_in_chrome_code"
          >open files as <code>File</code> objects</a
        >
        and send them via
        <a href="/en-US/Firefox/Multiprocess_Firefox/The_message_manager"
          >message manager</a
        >.
      </td>
    </tr>
    <tr>
      <td>
        <code
          ><a
            href="/en/DOM/Input.mozGetFileNameArray"
            title="en/DOM/Input.mozGetFileNameArray"
            >mozGetFileNameArray</a
          >(length, filenames)</code
        >{{non-standard_inline}}
      </td>
      <td><code>void</code></td>
      <td>Returns an array of all the file names from the input.</td>
    </tr>
    <tr>
      <td>
        <code
          ><a
            href="/en/DOM/Input.mozSetFileNameArray"
            title="en/DOM/Input.mozSetFileNameArray"
            >mozSetFileNameArray</a
          >(filenames, length)</code
        >{{non-standard_inline}}
      </td>
      <td><code>void</code></td>
      <td>
        Sets the filenames for the files selected on the input. Not for use in
        <a
          href="/en-US/Firefox/Multiprocess_Firefox/Limitations_of_frame_scripts"
          >frame scripts</a
        >, because it accesses the filesystem.
      </td>
    </tr>
    <tr>
      <td>
        <code
          ><a href="/en/DOM/Input.select" title="en/DOM/Input.select">select</a
          >()</code
        >
      </td>
      <td><code>void</code></td>
      <td>
        Selects the input text in the element, and focuses it so the user can
        subsequently replace the whole entry.
      </td>
    </tr>
    <tr>
      <td><code>setCustomValidity(error)</code></td>
      <td><code>void</code></td>
      <td>
        Sets a custom validity message for the element. If this message is not
        the empty string, then the element is suffering from a custom validity
        error, and does not validate.
      </td>
    </tr>
    <tr>
      <td>
        <code
          ><a
            href="/en/DOM/Input.setSelectionRange"
            title="en/DOM/Input.setSelectionRange"
            >setSelectionRange</a
          >(selectionStart, selectionEnd, [optional] selectionDirection)</code
        >
      </td>
      <td><code>void</code></td>
      <td>
        Selects a range of text in the element (but does not focus it). The
        optional <code>selectionDirection</code> parameter may be
        <code>"forward"</code> or <code>"backward"</code> to establish the
        direction in which selection was set, or <code>"none"</code> if the
        direction is unknown or not relevant. The default is
        <code>"none"</code>. Specifying a
        <code>selectionDirection</code> parameter sets the value of the
        <code>selectionDirection</code> property.
      </td>
    </tr>
    <tr>
      <td>
        <code
          >setRangeText(replacement, [optional] start, [optional] end,
          [optional] selectMode)</code
        >
      </td>
      <td><code>void</code></td>
      <td>
        Replaces a range of text with the new text. Supported input types:
        <code>text</code>, <code>search</code>, <code>url</code>,
        <code>tel</code>, <code>password.</code>
      </td>
    </tr>
    <tr>
      <td><code>stepDown(n)</code></td>
      <td><code>void</code></td>
      <td>
        Decrements the <a href="/ru/docs/Web/HTML/Element/input#value"><code>value</code></a> by
        (<a href="/ru/docs/Web/HTML/Element/input#step"><code>step</code></a> * <code>n</code>), where
        <code>n</code> defaults to <code>1</code> if not specified. Throws an
        <code>INVALID_STATE_ERR</code> exception:
        <ul>
          <li>
            if the method is not applicable to for the current
            <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> value.
          </li>
          <li>
            if the element has no <a href="/ru/docs/Web/HTML/Element/input#step"><code>step</code></a>
            value.
          </li>
          <li>
            if the <a href="/ru/docs/Web/HTML/Element/input#value"><code>value</code></a> cannot be
            converted to a number.
          </li>
          <li>
            if the resulting value is above the
            <a href="/ru/docs/Web/HTML/Element/input#max"><code>max</code></a> or below the
            <a href="/ru/docs/Web/HTML/Element/input#min"><code>min</code></a>.
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td><code>stepUp(n)</code></td>
      <td><code>void</code></td>
      <td>
        Increments the <a href="/ru/docs/Web/HTML/Element/input#value"><code>value</code></a> by
        (<a href="/ru/docs/Web/HTML/Element/input#step"><code>step</code></a> * <code>n</code>), where
        <code>n</code> defaults to <code>1</code> if not specified. Throws an
        <code>INVALID_STATE_ERR</code> exception:
        <ul>
          <li>
            if the method is not applicable to for the current
            <a href="/ru/docs/Web/HTML/Element/input#type"><code>type</code></a> value.
          </li>
          <li>
            if the element has no <a href="/ru/docs/Web/HTML/Element/input#step"><code>step</code></a>
            value.
          </li>
          <li>
            if the <a href="/ru/docs/Web/HTML/Element/input#value"><code>value</code></a> cannot be
            converted to a number.
          </li>
          <li>
            if the resulting value is above the
            <a href="/ru/docs/Web/HTML/Element/input#max"><code>max</code></a> or below the
            <a href="/ru/docs/Web/HTML/Element/input#min"><code>min</code></a>.
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- HTML element implementing this interface: {{ HTMLElement("input") }}.
