---
description: Vous pouvez utiliser le fournisseur de Registre système comme une instance ou un fournisseur de propriétés.
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: Utiliser le fournisseur de Registre système comme fournisseur de propriétés
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1b9b23be76845512df76bc0327543d463fd5eec6a816d57871f959b53229aecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107449"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a>Utiliser le fournisseur de Registre système comme fournisseur de propriétés

Vous pouvez utiliser le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) comme une instance ou un fournisseur de propriétés.

Si vous choisissez d’accéder aux interfaces du fournisseur de propriétés, vous devez marquer vos classes WMI pour indiquer votre intention.

**Pour utiliser le fournisseur de Registre système en tant que fournisseur de propriétés**

-   Définissez votre classe WMI avec les qualificateurs standard **DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)et **PropertyContext** .

    Le qualificateur **DynProps** identifie une classe comme ayant des propriétés gérées par le fournisseur de propriétés identifié par le qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) . Le qualificateur **PropertyContext** spécifie le nom de la valeur de Registre à stocker par la propriété. Le format du qualificateur **PropertyContext** est le même que celui du qualificateur **ClassContext** avec les valeurs *valueName* et *expression* supplémentaires.

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    *ValueName* et *expression* sont facultatives. Le paramètre *valueName* est utilisé uniquement si la valeur de registre a un nom. L' *expression* est également facultative et utilisée pour les données du descripteur de ressource. Pour plus d’informations, consultez [Description d’une ressource pour le registre](describing-a-resource-for-the-registry.md).

    L’exemple de code suivant montre comment la classe utilise le fournisseur de Registre système comme fournisseur de propriétés pour gérer ses propriétés non-clés.

    ``` syntax
    [DYNPROPS]
    class PropReg {

        [KEY]  STRING  MyKey;
        STRING Logging;
        STRING Events;
        uint32 Resource1;
    };

    [DYNPROPS]
    instance of PropReg
    {
      MyKey = "a";

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|Logging"), Dynamic, Provider("RegPropProv")]  Logging;

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|EnableEvents"), Dynamic, Provider("RegPropProv")]
       Events;

      [PropertyContext("local|hkey_local_Machine\\hardware\\
       ResourceMap\\Hardware Abstraction Layer\\PC Compatible Eisa/isa 
       hal|.raw(\"Internal\")(0)(0)(\"interrupt.vector\")"), Dynamic, 
       Provider("RegPropProv")]  Resource1;
    };
    ```

 

 
