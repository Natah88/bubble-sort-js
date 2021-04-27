# Bubble-sort-js (tri à bulles)
L' exercice en javascript pour créer un tri à bulles à partir d'un algorithme de tri ou "bubble Sort" : 
 - en utilisant quelques lignes dans l'un des implémentations du tri à bulles ,du source : https://www.geeksforgeeks.org/bubble-sort/
 
## Dans main.js : 
 
                        const chart = document.getElementById('chart');

                        console.log(chart);
                        let array = [];
                        for(let i = 0; i<100; i++){
                            let number = Math.floor(Math.random()*100);
                            array.push(number);
                        }
                            function draw() {
                                chart.innerHTML = '';
                                array.forEach(function (x) {
                                    let div = document.createElement('div');
                                    div.style.height = x+'px';
                                    chart.appendChild(div);
                                })
                            }
                            //draw ();

                            async function bubbleSort() {
                                for (let i = 0; i < array.length; i++) {
                                    for (let j = 0; j < array.length; j++) {
                                        if (array[j] > array[j+1]) {
                                            let temp = array[j];
                                            array[j] = array[j+1];
                                            array[j+1] = temp;    
                                        }
                                        draw();
                                        await sleep(1);
                                    }
                                }
                                function sleep(ms) {
                                    return new Promise(resolve => setTimeout(resolve,ms));
                                }
                            }
                            bubbleSort();


