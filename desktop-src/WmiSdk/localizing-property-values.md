---
description: Le modèle de localisation du schéma CIM fournit un mécanisme de localisation des qualificateurs. Elle ne prend pas en charge la localisation directe des valeurs de propriété.
ms.assetid: a88bd873-7132-45b6-831e-64f9bb254c6e
ms.tgt_platform: multiple
title: Localiser des valeurs de propriété
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ccec714557934ca32a878e21fb2a75d24a211a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318934"
---
# <a name="localizing-property-values"></a>Localiser des valeurs de propriété

Le modèle de localisation du schéma CIM fournit un mécanisme de localisation des qualificateurs. Elle ne prend pas en charge la localisation directe des valeurs de propriété.

Dans certains cas, toutefois, les valeurs des propriétés de chaîne dans les instances statiques peuvent être remplacées par un type entier énuméré et un mappage de valeur peut être défini pour la propriété dans la définition de classe. Dans ce cas, le qualificateur **values** doit être localisé. L’utilisation de qualificateurs d’énumération est le mécanisme principal pour la localisation des valeurs de propriété. Toutes les autres formes de localisation de valeurs de propriété ne sont pas prises en charge.

L’exemple suivant montre comment les propriétés statiques peuvent être localisées à l’aide de mappages de valeurs partielles avec des expressions régulières. Dans cet exemple, le sous-ensemble prédéfini de valeurs est initialisé dans le schéma à l’aide d’instances statiques. Les autres valeurs sont fournies dynamiquement.

``` syntax
[abstract]
class DataGroup
{
   [key] string GUID;
   [Description("data group display name"): Amended,
                     ValueMap{"Logical Disk",
                     "CPU Utilization", ".+"}]
                     string GroupDisplayName;
   [ValueMap{"Monitors percentage of disk free space",
                  "Monitors percentage CPU utilization", ".+"}] 
                   string GroupDescription;
};

[static, Description ("pre-configured parameters") :amended]
class InitialGroup : DataGroup {
};

[dynamic, provider("HMProvider"),
    Description ("user-defined parameters") :amended]
class UserDefionedGroup : DataGroup {
};

instance of InitialGroup {
   GUID = "abc";
   GroupDisplayName = "Logical Disk";
   GroupDescription = "Monitors percentage of disk free space";
};

instance of InitialGroup {
   GUID = "def";
   GroupDisplayName = "CPU Utilization";
   GroupDescription = "Monitors percentage CPU utilization";
};
```

Pour plus d’informations, consultez [localisation de propriétés statiques](localizing-static-properties.md).

 

 



