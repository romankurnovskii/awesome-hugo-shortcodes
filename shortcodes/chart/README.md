## chart

display [Chart.js](https://www.chartjs.org/) diagrams/blocks

![chart.js example](https://github.com/shen-yu/hugo-chart/blob/master/screenshots/1.png)

## path

{theme}/layouts/shortcodes/img.html

## Parameters

   | Name   | Type   | Default | Description                                   |
   | ------ | ------ | ------- | --------------------------------------------- |
   | width  | number | 100     | The width of chart, responsive in window (%). |
   | height | number | 300     | The height of chart (px).                     |


## Usage

```
    {{< chart [width] [height] >}}
    // Chartjs options goes here
    {{< /chart >}}
```

```go
{{< chart 90 200 >}}
{
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: 'Bar Chart',
            data: [12, 19, 18, 16, 13, 14],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        maintainAspectRatio: false,
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero: true
                }
            }]
        }
    }
}
{{< /chart >}}
```


Note that Chartjs is responsive as default, in order for the above code to correctly resize the chart height, the `maintainAspectRatio` option must be set to `false`.

## Demo

- https://romankurnovskii.com/en/posts/hugo-shortcode-examples/chart/

## Author

- https://github.com/shen-yu/hugo-chart
