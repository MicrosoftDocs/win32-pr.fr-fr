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
ms.openlocfilehash: 64fc701843438b4d173b1914ed2ac86214fe685e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541220"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a><span data-ttu-id="ec275-103">Utiliser le fournisseur de Registre système comme fournisseur de propriétés</span><span class="sxs-lookup"><span data-stu-id="ec275-103">Use the System Registry Provider as a Property Provider</span></span>

<span data-ttu-id="ec275-104">Vous pouvez utiliser le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) comme une instance ou un fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ec275-104">You can use the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) as either an instance or a property provider.</span></span>

<span data-ttu-id="ec275-105">Si vous choisissez d’accéder aux interfaces du fournisseur de propriétés, vous devez marquer vos classes WMI pour indiquer votre intention.</span><span class="sxs-lookup"><span data-stu-id="ec275-105">If you choose to access the property provider interfaces, you must mark your WMI classes to indicate your intention.</span></span>

<span data-ttu-id="ec275-106">**Pour utiliser le fournisseur de Registre système en tant que fournisseur de propriétés**</span><span class="sxs-lookup"><span data-stu-id="ec275-106">**To use the system registry provider as a property provider**</span></span>

-   <span data-ttu-id="ec275-107">Définissez votre classe WMI avec les qualificateurs standard **DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)et **PropertyContext** .</span><span class="sxs-lookup"><span data-stu-id="ec275-107">Define your WMI class with the **DynProps**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** standard qualifiers.</span></span>

    <span data-ttu-id="ec275-108">Le qualificateur **DynProps** identifie une classe comme ayant des propriétés gérées par le fournisseur de propriétés identifié par le qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="ec275-108">The **DynProps** qualifier identifies a class as having properties that are maintained by the property provider identified by the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span> <span data-ttu-id="ec275-109">Le qualificateur **PropertyContext** spécifie le nom de la valeur de Registre à stocker par la propriété.</span><span class="sxs-lookup"><span data-stu-id="ec275-109">The **PropertyContext** qualifier specifies the name of the registry value to be stored by the property.</span></span> <span data-ttu-id="ec275-110">Le format du qualificateur **PropertyContext** est le même que celui du qualificateur **ClassContext** avec les valeurs *valueName* et *expression* supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ec275-110">The format of the **PropertyContext** qualifier is the same as the format of the **ClassContext** qualifier with additional *valuename* and *expression* values.</span></span>

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    <span data-ttu-id="ec275-111">*ValueName* et *expression* sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="ec275-111">Both *valuename* and *expression* are optional.</span></span> <span data-ttu-id="ec275-112">Le paramètre *valueName* est utilisé uniquement si la valeur de registre a un nom.</span><span class="sxs-lookup"><span data-stu-id="ec275-112">The *valuename* setting is only used if the registry value has a name.</span></span> <span data-ttu-id="ec275-113">L' *expression* est également facultative et utilisée pour les données du descripteur de ressource.</span><span class="sxs-lookup"><span data-stu-id="ec275-113">The *expression* is also optional and is used for resource descriptor data.</span></span> <span data-ttu-id="ec275-114">Pour plus d’informations, consultez [Description d’une ressource pour le registre](describing-a-resource-for-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="ec275-114">For more information, see [Describing a Resource for the Registry](describing-a-resource-for-the-registry.md).</span></span>

    <span data-ttu-id="ec275-115">L’exemple de code suivant montre comment la classe utilise le fournisseur de Registre système comme fournisseur de propriétés pour gérer ses propriétés non-clés.</span><span class="sxs-lookup"><span data-stu-id="ec275-115">The following code example shows how the class uses the System Registry provider as a property provider to maintain its nonkey properties.</span></span>

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

 

 
