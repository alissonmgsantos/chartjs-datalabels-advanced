# chartjs-datalabels-advanced
Estrutura da utilização do plugin datalabels chartjs



options: {
          plugins: {
          datalabels: {
             display: function(context) {
							return context.dataset.data[context.dataIndex] > 0;
						},
            color: 'black',
            borderColor: 'white',
            backgroundColor: '#e0e0e087',
            borderRadius: 10,
            anchor: "end",
            align: "right",
            font: {
              weight: "bold"
            },
            formatter: Math.round
          }
        },
          scales: {
            yAxes: [{
              ticks: {
                beginAtZero: true,
              },
              barPercentage: 0.5,
              gridLines: {
                display: true
              }
            }],
            xAxes: [ {
              barPercentage: 0.5,
              gridLines: {
                display: true
              }
            }]
          },
           title: { display: true, text: 'title' },
          legend: { display: false, labels: { usePointStyle: true } },
          responsive: true,
          maintainAspectRatio: false
        }