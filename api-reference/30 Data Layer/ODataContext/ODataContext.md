---
module: data/odata/context
export: default
type: Object
---
---
##### lib
dx.mobile.js, dx.web.js, dx.viz.js, dx.viz-web.js, dx.all.js

##### shortDescription
The **ODataContent** is an object that provides access to an entire OData service.

---
This object creates several [ODataStore](/api-reference/30%20Data%20Layer/ODataStore '/Documentation/ApiReference/Data_Layer/ODataStore/') instances. Each instance accesses an individual entity collection.

---
##### jQuery  

    <!--JavaScript-->
    var context = new DevExpress.data.ODataContext({
        url: "http://www.example.com/Northwind.svc",
        entities: {
            Categories: {
                key: "CategoryID",
                keyType: "Int32"
            },
            // An entity collection alias
            Clients: {
                name: "Customers",
                key: "CustomerID",
                keyType: "String"
            },
            Products: {
                // A composite key
                key: ["ProductID", "ProductCode"],
                keyType: {
                    ProductID: "Guid",
                    ProductCode: "Int32" 
                }
            }
        }
    });

##### Angular  

    <!--TypeScript-->
    import ODataContext from "devextreme/data/odata/context";
    // ...
    export class AppComponent {
        context: ODataContext;
        constructor () {
            this.context = new ODataContext({
                url: "http://www.example.com/Northwind.svc",
                entities: {
                    Categories: {
                        key: "CategoryID",
                        keyType: "Int32"
                    },
                    // An entity collection alias
                    Clients: {
                        name: "Customers",
                        key: "CustomerID",
                        keyType: "String"
                    },
                    Products: {
                        // A composite key
                        key: ["ProductID", "ProductCode"],
                        keyType: {
                            ProductID: "Guid",
                            ProductCode: "Int32" 
                        }
                    }
                }
            });
        }
    }

##### AngularJS  

    <!--JavaScript-->
    angular.module('DemoApp', ['dx'])
        .controller('DemoController', function DemoController($scope) {
            $scope.context = new DevExpress.data.ODataContext({
                url: "http://www.example.com/Northwind.svc",
                entities: {
                    Categories: {
                        key: "CategoryID",
                        keyType: "Int32"
                    },
                    // An entity collection alias
                    Clients: {
                        name: "Customers",
                        key: "CustomerID",
                        keyType: "String"
                    },
                    Products: {
                        // A composite key
                        key: ["ProductID", "ProductCode"],
                        keyType: {
                            ProductID: "Guid",
                            ProductCode: "Int32" 
                        }
                    }
                }
            })
        });

##### Knockout  

    <!--JavaScript-->  
    var viewModel = {
        context: new DevExpress.data.ODataContext({
            url: "http://www.example.com/Northwind.svc",
            entities: {
                Categories: {
                    key: "CategoryID",
                    keyType: "Int32"
                },
                // An entity collection alias
                Clients: {
                    name: "Customers",
                    key: "CustomerID",
                    keyType: "String"
                },
                Products: {
                    // A composite key
                    key: ["ProductID", "ProductCode"],
                    keyType: {
                        ProductID: "Guid",
                        ProductCode: "Int32" 
                    }
                }
            }
        })
    };

    ko.applyBindings(viewModel);

---

#####See Also#####
- [DataSource Examples - OData](/concepts/30%20Data%20Layer/51%20Data%20Source%20Examples/2%20OData '/Documentation/Guide/Data_Layer/Data_Source_Examples/#OData')