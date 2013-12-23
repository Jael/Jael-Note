#Migration Tip

    create_table :tags_tickets, id: false do |t|
      t.integer :tag_id, :ticket_id
    end

The `id:false` option passed to `create_table` here tells Active Record
to create the table without the `id` field

#User

    email: 邮箱
