# opencart-cache-module
Just a simple cache delete button in your admin to ease in development


## Getting Started

Step 1: Copy the files from the "upload" and paste them into the root folder on your opencart installation. 
Step 2: Copy the following code and add it to your "/admin/controller/common/column_left.php" just after where "tool/log" is mentioned ref. the image.  
```
	if ($this->user->hasPermission('access', 'tool/cache')) {
		$maintenance[] = array(
			'name'	   => $this->language->get('text_cache'),
			'href'     => $this->url->link('tool/cache', 'user_token=' . $this->session->data['user_token'], true),
			'children' => array()		
		);
	}
```


### Prerequisites

Need a working opencart 3.0.2.0 installation. 


## Built With

* [Opencart](https://github.com/opencart/) - Opencart 3.0.2.0
* [Sublime Text](https://github.com/SublimeText) - Sublime Text

## Authors

* **Ankur Singh** - *Initial work* - [ankursinghagra](https://github.com/ankursingagra)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

