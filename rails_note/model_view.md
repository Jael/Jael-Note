#多个tags的建立
当在view里写了下面这个表单

    <%=label_tag :tags%>
    <%=text_field_tag :tags, params[:tags]%>

* this field will be sent through to TicketsController as
  `params[:tags]` rather than the kind of attributes you're used to, such as
`params[:ticket][title]`
* By specifying `params[:tags]` as the second argument to text_field_tag,
  you can re-populate this field when the ticket cannot be created due
to it failing validation.

当想获得并保存这个tag时，可在ticket model 里定义如下方法：

    def tag!(tags)
      tags = tags.split(" ").map{|name| Tag.find_or_create_by_name(name)}
      self.tags << tags
    end
