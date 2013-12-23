#Migration Tip

    create_table :tags_tickets, id: false do |t|
      t.integer :tag_id, :ticket_id
    end

The `id:false` option passed to `create_table` here tells Active Record
to create the table without the `id` field

#User

    email: (string) 用户邮箱 必填, 唯一
    encrypted_password: (string) 密码
    reset_passwod_token: (string) 重置密码令牌
    reset_password_send_at: (datetime) 重置密码时间
    last_sign_in_at: (datetime) 最后一次登录时间
    curent_sign_in_ip: (string) 当前登录ip
    last_sign_in_ip: (string) 最后一次登录ip
    created_at: (datetime) 创建时间
    updated_at: (datetime) 更新时间
    
#User
字段名 | 类型 |说明
------------ | ------------- | ------------
email | string  | 必填， 唯一
    
