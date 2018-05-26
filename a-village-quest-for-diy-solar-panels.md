# A village quest for DIY solar panels

{% tabs %}
{% tab title="The village" %}
A small village in the center of Italy needs to build a dozen of small solar panels to make some experiments and try to enhance their self-sufficiency in energy.   
After some preliminary discussions, some villagers make a call for an operative assembly, to define work plan, create a list of needed resources and allocate a budget.

The village has a common multi-sig wallet, managed by 5 person that rotate every month. In order to perform operations on the wallet, 3 of 5 signers has to unlock the wallet. Of course the wallet movements list is public and visible to all the villagers. The wallet manages the _**Eco**_, a social currency used only among villagers to enhance internal economy, _**FairCoin**_ - a crypto currency - to perform exchange inside a bigger cooperative network of villages, local nodes and organisation spread across the whole globe and a reserve of _**Euro**_, to be used when none of the other alternatives are available.

The budget approved for the solar panel plan is ~ 200 eco.
{% endtab %}

{% tab title="Data" %}
```javascript
{
  type: "Agent",
  id: "503",
  name: "CaiMercati",
  classification: "Organisation",
  image: "https://picsum.photos/200/300",
  ownedEconomicResources: [
    ...,
    {
      type: 'EconomicResource',
      resourceClassifiedAs: {
        name: 'ECO'
        category: 'currency'
      },
      trackingIdentifier: 'Eco social currency',
      currentQuantity: {
        quantity: 450,
        unit: 'Each'
      },
      note: '',
    },
    {
      type: 'EconomicResource',
      resourceClassifiedAs: {
        name: 'FairCoin'
        category: 'currency'
      },
      trackingIdentifier: 'FairCoin crypto currency',
      currentQuantity: {
        quantity: 899,
        unit: 'Each'
      },
      note: '',
    },
    {
      type: 'EconomicResource',
      resourceClassifiedAs: {
        name: 'Euro'
        category: 'currency'
      },
      trackingIdentifier: 'Euro fiat currency',
      currentQuantity: {
        quantity: 310,
        unit: 'Each'
      },
      note: '',
    }
  ],
  agentRelationships: [
    ...,
    {
      name: 'Alice',
      ...
    },
    {
      name: 'Aurora',
      ...
    },
    {
      name: 'Bob',
      ...
    },
    {
      name: 'Christian',
      ...
    },
    {
      name: 'Mario',
      ...
    },
    {
      name: 'Diego',
      ...
    }
  ]
}
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="The village Inventory" %}
At the end of the assembly, the list of needed resources is drawn up. Aurora performed a query on the inventory database, and luckily almost all items were already available

* [x] Wooden containers
* [x] Silicon
* [x] Wood glue
* [x] Wire cutters, welder, pond and other common equipments
* [ ] Solar cells
{% endtab %}

{% tab title="Data" %}
```javascript
[
  {
    type: 'EconomicResource',
    resourceClassifiedAs: {
      name: 'Silicon'
      category: 'gear'
    },
    trackingIdentifier: 'Dap 08641 Clear Silicone Sealant 9.8-Ounce',
    currentQuantity: {
      quantity: 4,
      unit: 'Each'
    },
    note: '',
  },
  {
    type: 'EconomicResource',
    resourceClassifiedAs: {
      name: 'Wood glue'
      category: 'gear'
    },
    trackingIdentifier: 'Elmers, Wood Glue Max',
    currentQuantity: {
      quantity: 1,
      unit: 'Each'
    },
    note: '',
  },
  {
    type: 'EconomicResource',
    resourceClassifiedAs: {
      name: 'wire cutter'
      category: 'electronics'
    },
    trackingIdentifier: 'IRWIN VISE-GRIP 2078300 Self-Adjusting Wire Stripper, 8"',
    currentQuantity: {
      quantity: 1,
      unit: 'Each'!
    },
    note: '',
  },
  {
    type: 'EconomicResource',
    resourceClassifiedAs: {
      name: 'welder'
      category: 'electronics'
    },
    trackingIdentifier: 'Forney Easy Weld 298 Arc Welder 100ST, 120-Volt, 90-Amp',
    currentQuantity: {
      quantity: 2,
      unit: 'each'
    },
    note: '',
  }
]
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="The work plan creation" %}
Shortly after the assembly, Bob - the assembly facilitator - inserts the work plan details on the platform. Its not too complex, the plan is made of 3 steps - or accordingly the platform vocabulary: 3 processes.

1. _The first process is to build 8 wooden containers of the right measure._
2. _Then, the following process is to cable together the solar cells._
3. _Last, the solar cells have to be applied to the wooden containers._

Once Bob publishes the work plan, all the villagers inside the network can look at the open works and commit to some of them.  
The platform furthermore sends a notification email to those users that share some skills with the ones requested from the work plan.
{% endtab %}

{% tab title="Data" %}
```javascript
{
  type: 'Plan',
  name: 'Solar panels DIY',
  note: 'We are going to build 8 solars panel of 100W each',
  due: '2017-09-05',
  planProcesses: [
    {
      type: 'Process',
      name: 'Build 8 wooden containers',
      note: 'Each wooden container has to be 60x80x4cm',
      plannedStart: '2017-01-05',
      plannedDuration: '2017-03-05',
      isFinished: false,
      scope: {
        type: 'Agent',
        id: '503',
        name: 'CaiMercati',
        classification: 'Organisation',
        image: "https://picsum.photos/200/300"
      }
    },
    {
      type: 'Process',
      name: 'cable together the solar cells',
      note: '',
      plannedStart: '2017-02-05',
      plannedDuration: '2017-04-05',
      isFinished: false,
      scope: {
        type: 'Agent',
        id: '503',
        name: 'CaiMercati',
        classification: 'Organisation',
        image: "https://picsum.photos/200/300"
      }
    },
    {
      type: 'Process',
      name: 'Paste the solar cells on the wooden containers',
      note: 'Paste and refine the wooden container',
      plannedStart: '2017-04-05',
      plannedDuration: '2017-07-05',
      isFinished: false,
      scope: {
        type: 'Agent',
        id: '503',
        name: 'CaiMercati',
        classification: 'Organisation',
        image: "https://picsum.photos/200/300"
      }
    }
  ]
}
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="The villagers commit to work" %}
Once received the email, Diego - a carpenter - commits to build the 8 wooden containers.   
Regards the solar cells, Alice publishes a request on the offers/needs exchange network. After some days, a close village answer to the request, offering a set of solar cells never used for 100FairCoin.  
After agreed on assembly, they use the common wallet to buy those solar cells.   
Aurora commits to work, together with Christian, on the second process.   
After 2 days of hard work, all the solar cells are cabled accordingly to the specifics. Aurora and Chris log their work on the platform and set their process as complete.   
For the last process, Mario with some silicon will paste the solar cells to the wood, paying attention to respect the decided layout.   
As the carpenter, Aurora and Christian did, also Mario logs his work on the platform and set the process as completed.   
After some minor adjustments, the 8 solar panels are finished and ready to be installed.
{% endtab %}

{% tab title="Data" %}
```javascript
{
  type:  'EconomicEvent',
  provider: {
    type: "Agent",
    id: "281",
    name: "Diego",
    classification: "Person",
    image: "https://picsum.photos/200/300"
  },
  action:  "work",
  affectedQuantity: {
    quantity: 12,
    unit: "Hour"
  },
  date: "2017-09-05",
  resourceClassifiedAs: {
    type: 'ResourceClassification',
    name: 'Wooden container',
    parent: ''
  },
  note: "crafted the 8 wooden containers, accordingly to the specs",
  scope: {
    type: "Agent",
    id: "503",
    name: "CaiMercati",
    classification: "Organisation",
    image: "https://picsum.photos/200/300",
  }
},
{
  type:  'EconomicEvent',
  provider: {
    type: "Agent",
    id: "282",
    name: "Aurora",
    classification: "Person",
    image: "https://picsum.photos/200/300"
  },
  action:  "work",
  affectedQuantity: {
    quantity: 4,
    unit: "Hour"
  },
  date: "2017-09-05",
  resourceClassifiedAs: {
    type: 'ResourceClassification',
    name: 'solar cells',
    parent: ''
  },
  note: "cabled half of solar cells",
  scope: {
    type: "Agent",
    id: "503",
    name: "CaiMercati",
    classification: "Organisation",
    image: "https://picsum.photos/200/300",
  }
},
{
  type:  'EconomicEvent',
  provider: {
    type: "Agent",
    id: "282",
    name: "Christian",
    classification: "Person",
    image: "https://picsum.photos/200/300"
  },
  action:  "work",
  affectedQuantity: {
    quantity: 4,
    unit: "Hour"
  },
  date: "2017-09-05",
  resourceClassifiedAs: {
    type: 'ResourceClassification',
    name: 'solar cells',
    parent: ''
  },
  note: "cabled other half of solar cells",
  scope: {
    type: "Agent",
    id: "503",
    name: "CaiMercati",
    classification: "Organisation",
    image: "https://picsum.photos/200/300",
  }
},
{
  type:  'EconomicEvent',
  provider: {
    type: "Agent",
    id: "282",
    name: "Mario",
    classification: "Person",
    image: "https://picsum.photos/200/300"
  },
  action:  "work",
  affectedQuantity: {
    quantity: 6,
    unit: "Hour"
  },
  date: "2017-09-05",
  resourceClassifiedAs: {
    type: 'ResourceClassification',
    name: 'solar panels',
    parent: ''
  },
  note: "Pasted and refined solar panels",
  scope: {
    type: "Agent",
    id: "503",
    name: "CaiMercati",
    classification: "Organisation",
    image: "https://picsum.photos/200/300",
  }
},
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="New items on the village common inventory" %}
Automatically, the platform adds 8 solar panels to the village inventory.
{% endtab %}

{% tab title="Data" %}
```javascript
[
  ...,
  {
    type: 'EconomicResource',
    resourceClassifiedAs: {
      name: 'Solar panel'
      category: 'electricity'
    },
    trackingIdentifier: 'DIY Solar panel 100W 60x80x4cm',
    currentQuantity: {
      quantity: 8,
      unit: 'Each'
    },
    note: 'Be carefull when you use it ;)',
  }
]
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="The budget distribution" %}
The platform contains data related to each work contributions.Accordingly to a formula agreed in assembly, the software calculate the income to distribute to the carpenter, aurora, Chris, Mario end Bob.  
Once read and accepted the budget distribution, the common wallet send the payment to each contributor wallet.
{% endtab %}

{% tab title="Data" %}
```javascript
{
  type: 'transfer',
  ...
},
{
  type: 'transfer',
  ...
},
{
  type: 'transfer',
  ...
},{
  type: 'transfer',
  ...
}
```
{% endtab %}
{% endtabs %}

All the data produced during the whole activity, was stored and publicly accessible by all the member of the village, that could check works done by other members, inventory, transaction movements, balances and so on.  
All those data can be re-assembled and mixed by statistical tools to provide insight about village management and enhance their quest for self-autonomy.  


