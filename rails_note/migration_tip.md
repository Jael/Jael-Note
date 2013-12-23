#Migration Tip

    create_table :tags_tickets, id: false do |t|
      t.integer :tag_id, :ticket_id
    end

The `id:false` option passed to `create_table` here tells Active Record
to create the table without the `id` field

#User

    email: 用户邮箱 必须存在且唯一
    encrypted_password: 密码
    reset_passwod_token: 重置密码令牌
