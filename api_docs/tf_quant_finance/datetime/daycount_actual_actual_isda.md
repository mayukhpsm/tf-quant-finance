<!--
This file is generated by a tool. Do not edit directly.
For open-source contributions the docs will be updated automatically.
-->

*Last updated: 2020-07-01.*

<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf_quant_finance.datetime.daycount_actual_actual_isda" />
<meta itemprop="path" content="Stable" />
</div>

# tf_quant_finance.datetime.daycount_actual_actual_isda

<!-- Insert buttons and diff -->

<table class="tfo-notebook-buttons tfo-api" align="left">
</table>

<a target="_blank" href="https://github.com/google/tf-quant-finance/blob/master/tf_quant_finance/datetime/daycounts.py">View source</a>



Computes the year fraction between the specified dates.

```python
tf_quant_finance.datetime.daycount_actual_actual_isda(
    *, start_date, end_date, schedule_info=None, dtype=None, name=None
)
```



<!-- Placeholder for "Used in" -->

Computes the year fraction between the dates by dividing the actual number of
days in a leap year by 366 and the actual number of days in a standard year by
365.

When determining whether a leap day is contained in the date range,
'start_date' is excluded and 'end_date' is included.

Note that the schedule info is not needed for this convention and is ignored
if supplied.

https://en.wikipedia.org/wiki/Day_count_convention#Actual/Actual_ISDA

#### Args:


* <b>`start_date`</b>: A `DateTensor` object of any shape.
* <b>`end_date`</b>: A `DateTensor` object of compatible shape with `start_date`.
* <b>`schedule_info`</b>: The schedule info. Ignored for this convention.
* <b>`dtype`</b>: The dtype of the result. Either `tf.float32` or `tf.float64`. If not
  supplied, `tf.float32` is returned.
* <b>`name`</b>: Python `str` name prefixed to ops created by this function. If not
  supplied, `actual_actual_isda` is used.


#### Returns:

A real `Tensor` of supplied `dtype` and shape of `start_date`. The year
fraction between the start and end date as computed by Actual/Actual ISDA
convention.