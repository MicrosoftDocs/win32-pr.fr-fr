---
title: Élément Task (DefinitionType)
description: Définit un événement spécifique à la tâche que votre fournisseur peut journaliser. | Élément Task (DefinitionType)
ms.assetid: 0e880720-1896-43cf-b702-cabca8ab1430
keywords:
- élément Task EventLog
topic_type:
- apiref
api_name:
- task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35fe629c17b8ede4064de3fb11d05c8e8c84f202
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106527069"
---
# <a name="task-definitiontype-element"></a><span data-ttu-id="a1053-105">Élément Task (DefinitionType)</span><span class="sxs-lookup"><span data-stu-id="a1053-105">task (DefinitionType) Element</span></span>

<span data-ttu-id="a1053-106">\[À partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, cet élément n’est plus disponible.\]</span><span class="sxs-lookup"><span data-stu-id="a1053-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="a1053-107">Définit un événement spécifique à la tâche que votre fournisseur peut journaliser.</span><span class="sxs-lookup"><span data-stu-id="a1053-107">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:element name="task"
    type="TaskEventDefinitionType"
 />
```

<span data-ttu-id="a1053-108">L’élément **Task** est défini par le type complexe [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a1053-108">The **task** element is defined by the [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1053-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1053-109">Requirements</span></span>



| <span data-ttu-id="a1053-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1053-110">Requirement</span></span> | <span data-ttu-id="a1053-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1053-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1053-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1053-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a1053-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1053-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1053-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1053-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a1053-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1053-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1053-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1053-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1053-117">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="a1053-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="a1053-118">**événements (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="a1053-118">**events (ProviderType)**</span></span>](eventmanifestschema-events-providertype-element.md)
</dt> </dl>

 

 





