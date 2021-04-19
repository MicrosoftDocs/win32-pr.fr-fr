---
description: La propriété ConfigurableItems en lecture seule de l’objet Merge retourne une collection ConfigurableItem objets, chacun représentant une ligne unique de la table ModuleConfiguration.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.Configpropriété urableItems (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542546"
---
# <a name="mergeconfigurableitems-property"></a><span data-ttu-id="a0530-103">Merge.Configpropriété urableItems</span><span class="sxs-lookup"><span data-stu-id="a0530-103">Merge.ConfigurableItems property</span></span>

<span data-ttu-id="a0530-104">La propriété **ConfigurableItems** en lecture seule de l’objet [**Merge**](merge-object.md) retourne une collection [**ConfigurableItem**](configurableitem-object.md) objets, chacun représentant une ligne unique de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="a0530-104">The read-only **ConfigurableItems** property of the [**Merge**](merge-object.md) object returns a collection [**ConfigurableItem**](configurableitem-object.md) objects, each of which represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="a0530-105">Sémantiquement, chaque interface de l’énumérateur représente un élément qui peut être configuré par le consommateur de module.</span><span class="sxs-lookup"><span data-stu-id="a0530-105">Semantically, each interface in the enumerator represents an item that can be configured by the module consumer.</span></span> <span data-ttu-id="a0530-106">La collection est une collection en lecture seule et implémente les interfaces de collection en lecture seule standard de Item (), Count () et \_ NewEnum ().</span><span class="sxs-lookup"><span data-stu-id="a0530-106">The collection is a read-only collection and implements the standard read-only collection interfaces of Item(), Count() and \_NewEnum().</span></span> <span data-ttu-id="a0530-107">L’énumérateur **IEnumMsmConfigItems** implémente Next (), Skip (), Reset () et Clone () avec la sémantique standard.</span><span class="sxs-lookup"><span data-stu-id="a0530-107">The **IEnumMsmConfigItems** enumerator implements Next(), Skip(), Reset(), and Clone() with the standard semantics.</span></span>

<span data-ttu-id="a0530-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a0530-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0530-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0530-109">Syntax</span></span>


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a><span data-ttu-id="a0530-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a0530-110">Property value</span></span>

## <a name="c"></a><span data-ttu-id="a0530-111">C++</span><span class="sxs-lookup"><span data-stu-id="a0530-111">C++</span></span>

<span data-ttu-id="a0530-112">Consultez la fonction [**obtenir \_ ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) .</span><span class="sxs-lookup"><span data-stu-id="a0530-112">See [**get\_ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0530-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0530-113">Requirements</span></span>



| <span data-ttu-id="a0530-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0530-114">Requirement</span></span> | <span data-ttu-id="a0530-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0530-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0530-116">Version</span><span class="sxs-lookup"><span data-stu-id="a0530-116">Version</span></span><br/> | <span data-ttu-id="a0530-117">Mergemod.dll 2,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a0530-117">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="a0530-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0530-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a0530-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0530-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0530-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a0530-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a0530-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0530-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




