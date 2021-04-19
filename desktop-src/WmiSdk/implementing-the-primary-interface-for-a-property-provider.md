---
description: Un fournisseur de propriétés utilise les méthodes IWbemPropertyProvider comme interface principale de WMI. Avec IWbemPropertyProvider, vous pouvez implémenter le code pour récupérer et modifier des propriétés de classe et d’instance.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Implémentation de l’interface principale pour un fournisseur de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530116"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a><span data-ttu-id="03f4d-104">Implémentation de l’interface principale pour un fournisseur de propriétés</span><span class="sxs-lookup"><span data-stu-id="03f4d-104">Implementing the Primary Interface for a Property Provider</span></span>

<span data-ttu-id="03f4d-105">Un fournisseur de propriétés utilise les méthodes [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) comme interface principale de WMI.</span><span class="sxs-lookup"><span data-stu-id="03f4d-105">A property provider uses the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods as the primary interface to WMI.</span></span> <span data-ttu-id="03f4d-106">Avec **IWbemPropertyProvider**, vous pouvez implémenter le code pour récupérer et modifier des propriétés de classe et d’instance.</span><span class="sxs-lookup"><span data-stu-id="03f4d-106">With **IWbemPropertyProvider**, you can implement the code to retrieve and modify class and instance properties.</span></span>

<span data-ttu-id="03f4d-107">Le tableau suivant répertorie les méthodes [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) que vous pouvez implémenter pour un fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="03f4d-107">The following table lists the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods that you can implement for a property provider.</span></span>



| <span data-ttu-id="03f4d-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="03f4d-108">Method</span></span>                                                   | <span data-ttu-id="03f4d-109">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="03f4d-109">Feature</span></span>      |
|----------------------------------------------------------|--------------|
| [<span data-ttu-id="03f4d-110">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="03f4d-110">**GetProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | <span data-ttu-id="03f4d-111">Récupération</span><span class="sxs-lookup"><span data-stu-id="03f4d-111">Retrieval</span></span>    |
| [<span data-ttu-id="03f4d-112">**PutProperty**</span><span class="sxs-lookup"><span data-stu-id="03f4d-112">**PutProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | <span data-ttu-id="03f4d-113">Modification</span><span class="sxs-lookup"><span data-stu-id="03f4d-113">Modification</span></span> |



 

> [!Note]  
> <span data-ttu-id="03f4d-114">Vous devez implémenter un fournisseur de propriétés en tant que fournisseur in-process.</span><span class="sxs-lookup"><span data-stu-id="03f4d-114">You must implement a property provider as an in-process provider.</span></span> <span data-ttu-id="03f4d-115">WMI initialise les fournisseurs de propriétés écrits comme des services ou des fichiers exécutables, mais n’appelle jamais leurs méthodes [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) et [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) .</span><span class="sxs-lookup"><span data-stu-id="03f4d-115">WMI will initialize property providers written as services or executable files but will never call their [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) methods.</span></span>

 

<span data-ttu-id="03f4d-116">Si vous choisissez de ne pas prendre en charge l’une de ces méthodes, votre fournisseur peut fournir une implémentation de stub qui retourne le **\_ fournisseur E WBEM \_ \_ non \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="03f4d-116">If you choose not to support one of these methods, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span>

<span data-ttu-id="03f4d-117">Un fournisseur de propriétés identifie une classe ou une instance managée par un ensemble de trois qualificateurs : **PropertyContext**, **InstanceContext** et **ClassContext**.</span><span class="sxs-lookup"><span data-stu-id="03f4d-117">A property provider identifies a managed class or instance by a set of three qualifiers: **PropertyContext**, **InstanceContext**, and **ClassContext**.</span></span> <span data-ttu-id="03f4d-118">WMI passera des constantes de chaîne décrivant ces trois qualificateurs à votre fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="03f4d-118">WMI will pass in string constants describing these three qualifiers to your property provider.</span></span>

<span data-ttu-id="03f4d-119">Votre fournisseur de propriétés doit être prêt à gérer les types de qualificateurs de contexte suivants :</span><span class="sxs-lookup"><span data-stu-id="03f4d-119">Your property provider must be prepared to handle the following types of context qualifiers:</span></span>

-   <span data-ttu-id="03f4d-120">Le qualificateur **InstanceContext** est attaché à une instance et contient des informations qui s’appliquent à chaque propriété de l’instance.</span><span class="sxs-lookup"><span data-stu-id="03f4d-120">The **InstanceContext** qualifier is attached to an instance and contains information that applies to every property in the instance.</span></span>
-   <span data-ttu-id="03f4d-121">Le qualificateur **ClassContext** est attaché à une classe et contient des informations qui s’appliquent à chaque instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="03f4d-121">The **ClassContext** qualifier is attached to a class and contains information that applies to every instance in the class.</span></span> <span data-ttu-id="03f4d-122">Par exemple, dans une classe utilisée pour stocker les données fournies par le fournisseur de Registre, **ClassContext** peut être le chemin d’accès à la clé de Registre qui contient les propriétés à signaler.</span><span class="sxs-lookup"><span data-stu-id="03f4d-122">For example, in a class used to store data supplied by the Registry provider, **ClassContext** can be the path to the registry key that contains the properties to be reported.</span></span>
-   <span data-ttu-id="03f4d-123">Le qualificateur **PropertyContext** spécifie les informations spécifiques au contexte qui se rapportent à la propriété.</span><span class="sxs-lookup"><span data-stu-id="03f4d-123">The **PropertyContext** qualifier specifies context-specific information that pertains to the property.</span></span> <span data-ttu-id="03f4d-124">Par exemple, dans une classe utilisée pour stocker les données fournies par le fournisseur de Registre, **PropertyContext** spécifie le nom de la valeur de Registre à stocker par la propriété.</span><span class="sxs-lookup"><span data-stu-id="03f4d-124">For example, in a class used to store data supplied by the Registry provider, **PropertyContext** specifies the name of the registry value to be stored by the property.</span></span>

<span data-ttu-id="03f4d-125">Ces qualificateurs peuvent fonctionner ensemble.</span><span class="sxs-lookup"><span data-stu-id="03f4d-125">These qualifiers can work together.</span></span> <span data-ttu-id="03f4d-126">Vous pouvez désigner une valeur **InstanceContext** et **PropertyContext** pour indiquer au fournisseur comment traiter des types particuliers d’instances.</span><span class="sxs-lookup"><span data-stu-id="03f4d-126">You can designate both an **InstanceContext** and **PropertyContext** value to tell the provider how to treat particular types of instances.</span></span> <span data-ttu-id="03f4d-127">Par exemple, vous pouvez marquer les instances que le fournisseur reconnaît comme étant lisibles, mais n’a qu’une seule propriété accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="03f4d-127">For example, you might want to mark instances the provider will recognize as readable but having only one writeable property.</span></span>

<span data-ttu-id="03f4d-128">Le qualificateur le plus courant utilisé est **PropertyContext**.</span><span class="sxs-lookup"><span data-stu-id="03f4d-128">The most common qualifier used is **PropertyContext**.</span></span> <span data-ttu-id="03f4d-129">Par conséquent, WMI fournit le qualificateur **DynProps** comme raccourci.</span><span class="sxs-lookup"><span data-stu-id="03f4d-129">Therefore, WMI provides the **DynProps** qualifier as a shortcut.</span></span> <span data-ttu-id="03f4d-130">WMI considère que chaque propriété d’une instance marquée avec **DynProps** a également les qualificateurs **dynamiques**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)et **PropertyContext** .</span><span class="sxs-lookup"><span data-stu-id="03f4d-130">WMI considers each property in an instance marked with **DynProps** to also have the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** qualifiers.</span></span>

 

 



