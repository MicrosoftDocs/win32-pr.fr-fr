---
title: Élément ButtonTip
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Élément ButtonTip
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Élément ButtonTip lecteur Windows Media
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530285"
---
# <a name="buttontip-element"></a><span data-ttu-id="8a7f1-105">Élément ButtonTip</span><span class="sxs-lookup"><span data-stu-id="8a7f1-105">ButtonTip Element</span></span>

> [!Note]  
> <span data-ttu-id="8a7f1-106">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8a7f1-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8a7f1-108">L’élément **ButtonTip** spécifie la chaîne de texte qui s’affiche lorsque l’utilisateur pointe sur un bouton du volet des tâches.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-108">The **ButtonTip** element specifies the text string that is displayed when the user points to a task pane button.</span></span>

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a><span data-ttu-id="8a7f1-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="8a7f1-109">Attributes</span></span>

<span data-ttu-id="8a7f1-110">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="8a7f1-111">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="8a7f1-111">Parent/Child Elements</span></span>



| <span data-ttu-id="8a7f1-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="8a7f1-112">Hierarchy</span></span>       | <span data-ttu-id="8a7f1-113">Élément</span><span class="sxs-lookup"><span data-stu-id="8a7f1-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="8a7f1-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8a7f1-114">Parent elements</span></span> | <span data-ttu-id="8a7f1-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="8a7f1-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="8a7f1-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8a7f1-116">Child elements</span></span>  | <span data-ttu-id="8a7f1-117">Aucune</span><span class="sxs-lookup"><span data-stu-id="8a7f1-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="8a7f1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8a7f1-118">Remarks</span></span>

<span data-ttu-id="8a7f1-119">Cet élément est facultatif pour chaque instance de **ServiceTask1**, **ServiceTask2** ou **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-119">This element is optional for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span> <span data-ttu-id="8a7f1-120">Si cet élément n’est pas fourni, le lecteur Windows Media utilise le texte du bouton comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-120">If this element is not supplied, Windows Media Player uses the button text as the default value.</span></span>

> [!Note]  
> <span data-ttu-id="8a7f1-121">Le lecteur Windows Media 10 comporte trois volets de tâches où un magasin en ligne peut afficher ses pages Web.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-121">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="8a7f1-122">Le magasin en ligne peut choisir d’utiliser un, deux ou les trois volets de tâches.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-122">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="8a7f1-123">Le lecteur Windows Media 11 n’a qu’un seul volet de tâches, que l’utilisateur peut afficher en cliquant sur l’onglet **magasins en ligne** . le lecteur Windows Media 11 ignore les éléments **ServiceTask2** et **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="8a7f1-123">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8a7f1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a7f1-124">Requirements</span></span>



| <span data-ttu-id="8a7f1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a7f1-125">Requirement</span></span> | <span data-ttu-id="8a7f1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a7f1-126">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="8a7f1-127">Version</span><span class="sxs-lookup"><span data-stu-id="8a7f1-127">Version</span></span><br/> | <span data-ttu-id="8a7f1-128">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8a7f1-128">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a7f1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a7f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a7f1-130">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="8a7f1-130">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="8a7f1-131">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="8a7f1-131">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="8a7f1-132">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="8a7f1-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





