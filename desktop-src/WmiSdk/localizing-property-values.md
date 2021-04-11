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
# <a name="localizing-property-values"></a><span data-ttu-id="ea10f-104">Localiser des valeurs de propriété</span><span class="sxs-lookup"><span data-stu-id="ea10f-104">Localizing Property Values</span></span>

<span data-ttu-id="ea10f-105">Le modèle de localisation du schéma CIM fournit un mécanisme de localisation des qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="ea10f-105">The CIM schema localization model provides a mechanism for localizing qualifiers.</span></span> <span data-ttu-id="ea10f-106">Elle ne prend pas en charge la localisation directe des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="ea10f-106">It does not support direct localization of property values.</span></span>

<span data-ttu-id="ea10f-107">Dans certains cas, toutefois, les valeurs des propriétés de chaîne dans les instances statiques peuvent être remplacées par un type entier énuméré et un mappage de valeur peut être défini pour la propriété dans la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="ea10f-107">In some cases, however, the string properties values in the static instances can be replaced by an enumerated integer type and a value map can be defined for the property in the class definition.</span></span> <span data-ttu-id="ea10f-108">Dans ce cas, le qualificateur **values** doit être localisé.</span><span class="sxs-lookup"><span data-stu-id="ea10f-108">In these cases, the **Values** qualifier should be localized.</span></span> <span data-ttu-id="ea10f-109">L’utilisation de qualificateurs d’énumération est le mécanisme principal pour la localisation des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="ea10f-109">Using enumeration qualifiers is the primary mechanism for localizing property values.</span></span> <span data-ttu-id="ea10f-110">Toutes les autres formes de localisation de valeurs de propriété ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ea10f-110">Any other forms of property value localization are not supported.</span></span>

<span data-ttu-id="ea10f-111">L’exemple suivant montre comment les propriétés statiques peuvent être localisées à l’aide de mappages de valeurs partielles avec des expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="ea10f-111">The following example shows how static properties can be localized using partial value maps with regular expressions.</span></span> <span data-ttu-id="ea10f-112">Dans cet exemple, le sous-ensemble prédéfini de valeurs est initialisé dans le schéma à l’aide d’instances statiques.</span><span class="sxs-lookup"><span data-stu-id="ea10f-112">In this example, the predefined subset of values is initialized in the schema using static instances.</span></span> <span data-ttu-id="ea10f-113">Les autres valeurs sont fournies dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="ea10f-113">The rest of the values are provided dynamically.</span></span>

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

<span data-ttu-id="ea10f-114">Pour plus d’informations, consultez [localisation de propriétés statiques](localizing-static-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ea10f-114">For more information, see [Localizing Static Properties](localizing-static-properties.md).</span></span>

 

 



