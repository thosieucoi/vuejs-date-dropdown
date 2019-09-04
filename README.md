# Vue Date Dropdown

> A Vue date dropdown component

## Contents

 - [Installing](https://github.com/thosieucoi/vuejs-date-dropdown#installing)
 - [Examples](https://github.com/thosieucoi/vuejs-date-dropdown#examples)
 - [API](https://github.com/thosieucoi/vuejs-date-dropdown#api)

## Installing

```bash
npm install vue-date-dropdown --save

yarn add vue-date-dropdown
```

```js
import DateDropdown from 'vue-date-dropdown'

export default {
	...
	components: {
		DateDropdown
	},
	data () {
		return {
			selectedDate: '',
			...
		}
	}
	...
}
```
Or if you are using CDN version

```js
<script src="vue-date-dropdown.min.js"></script>

<script>
Vue.use(DateDropdown)

new Vue({
	...
	data() {
		return {
			selectedDate: '',
			...
		}
	}
	...
});
<script>
```

## Examples

See the demo in the [example](https://github.com/thosieucoi/vuejs-date-dropdown/tree/master/example) folder.

Setting a default date

```html
<date-dropdown default="1990-12-25" v-model="selectedDate" />
```

Setting a min date

```html
<date-dropdown min="1960" v-model="selectedDate" />
```

Setting a max date

```html
<date-dropdown max="2020" v-model="selectedDate" />
```

Setting a range of dates

```html
<date-dropdown min="1960" max="2020" v-model="selectedDate" />
```

Setting Russian names of months

```html
<date-dropdown
	v-model="selectedDate" 
	months-names="一, 二, 三, 四, 五, 六, 七, 八, 九, 十, 十一, 十二">
<date-dropdown>
```

## API

### Props

| Name         | Type     | Description                                      |
| :------------| :------- | :------------------------------------------------|
| default      | String   | Set default date.                                |
| min          | String   | Limits the year to a minimum specified value.    |
| max          | String   | Limits the year to a maximum specified value.    |
| months-names | String   | The alternative names of month.                  |