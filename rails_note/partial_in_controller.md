#rendering partial in controller

    def new  
      asset = Asset.new  
      render partial: 'files/form', locals: {asset: asset}  
    end

> "Here you must pass the name of the partial using the `:partial` oprion
so the controller will attempt to render a partial. if you left it
without the option, the controllerwould instead try to render the
template at app/views/files/form.html.erb,which doesn't not exist"
