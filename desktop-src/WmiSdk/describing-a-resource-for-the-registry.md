---
description: Le registre système contient des données relatives aux ressources.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Description d’une ressource pour le registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411565"
---
# <a name="describing-a-resource-for-the-registry"></a>Description d’une ressource pour le registre

Le registre système contient des données relatives aux ressources. Ces données se trouvent sous la clé de Registre suivante et sont conservées dans un type de données de registre spécial nommé **reg \_ Resource \_ List**. Les applications peuvent obtenir les données relatives aux ressources par le biais du fournisseur de Registre système. Vous pouvez ajouter et modifier des ressources système dans le registre.

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

La procédure suivante décrit comment stocker des informations relatives aux ressources dans le registre système.

**Pour stocker les informations relatives aux ressources dans le registre système**

1.  Créez une chaîne qui contient les champs suivants.

    

    <table>
    <thead>
    <tr class="header">
    <th>Champ</th>
    <th>Contient</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Type d'interface</td>
    <td>Une des valeurs suivantes :<br/> <dl> Interne<br />
    ISA<br />
    EISA<br />
    MICROCANAL<br />
    TurboChannel<br />
    PCIBus<br />
    VMEBus<br />
    NuBus<br />
    PCMCIABus<br />
    CBus<br />
    MPIBus<br />
    MPSABus<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Numéro de bus</td>
    <td>Entier spécifiant le numéro de bus.</td>
    </tr>
    <tr class="odd">
    <td>Numéro de descripteur partiel</td>
    <td>Entier spécifiant le numéro du descripteur.</td>
    </tr>
    <tr class="even">
    <td>Type de décalage ou d’Union</td>
    <td>Une des valeurs suivantes :<br/> <dl> Port. Start<br />
    Port. PhysicalAddress<br />
    Port. Length<br />
    Interrupt. niveau<br />
    Interrupt. Vector<br />
    Interrupt. Affinity<br />
    Memory. Start<br />
    Memory. PhysicalAddress<br />
    Memory. Length<br />
    DMA. Channel<br />
    DMA. port<br />
    DMA. Reserved1<br />
    DeviceSpecificData. DataSize<br />
    DeviceSpecificData. Reserved1<br />
    DeviceSpecificData. Reserved2<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Placez la chaîne dans la clé appropriée sous la clé de registre.

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

L’exemple de code suivant décrit un descripteur de ressource valide.

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

L’exemple de code suivant montre une syntaxe MOF valide pour la récupération d’un descripteur de ressource.

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




