---
title: Élément ButtonText
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Élément ButtonText
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Élément ButtonText Windows Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540715"
---
# <a name="buttontext-element"></a><span data-ttu-id="fcca0-105">Élément ButtonText</span><span class="sxs-lookup"><span data-stu-id="fcca0-105">ButtonText Element</span></span>

> [!Note]  
> <span data-ttu-id="fcca0-106">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="fcca0-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="fcca0-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fcca0-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="fcca0-108">L’élément **ButtonText** spécifie la chaîne de texte que le lecteur Windows Media affiche pour un bouton du volet des tâches.</span><span class="sxs-lookup"><span data-stu-id="fcca0-108">The **ButtonText** element specifies the text string that Windows Media Player displays for a task pane button.</span></span>

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a><span data-ttu-id="fcca0-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="fcca0-109">Attributes</span></span>

<span data-ttu-id="fcca0-110">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="fcca0-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="fcca0-111">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="fcca0-111">Parent/Child Elements</span></span>



| <span data-ttu-id="fcca0-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="fcca0-112">Hierarchy</span></span>       | <span data-ttu-id="fcca0-113">Élément</span><span class="sxs-lookup"><span data-stu-id="fcca0-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="fcca0-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fcca0-114">Parent elements</span></span> | <span data-ttu-id="fcca0-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="fcca0-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="fcca0-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fcca0-116">Child elements</span></span>  | <span data-ttu-id="fcca0-117">Aucune</span><span class="sxs-lookup"><span data-stu-id="fcca0-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="fcca0-118">Notes</span><span class="sxs-lookup"><span data-stu-id="fcca0-118">Remarks</span></span>

<span data-ttu-id="fcca0-119">Cet élément est requis pour chaque instance de **ServiceTask1**, **ServiceTask2** ou **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="fcca0-119">This element is required for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span>

> [!Note]  
> <span data-ttu-id="fcca0-120">Le lecteur Windows Media 10 comporte trois volets de tâches où un magasin en ligne peut afficher ses pages Web.</span><span class="sxs-lookup"><span data-stu-id="fcca0-120">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="fcca0-121">Le magasin en ligne peut choisir d’utiliser un, deux ou les trois volets de tâches.</span><span class="sxs-lookup"><span data-stu-id="fcca0-121">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="fcca0-122">Le lecteur Windows Media 11 n’a qu’un seul volet de tâches, que l’utilisateur peut afficher en cliquant sur l’onglet **magasins en ligne** . le lecteur Windows Media 11 ignore les éléments **ServiceTask2** et **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="fcca0-122">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="fcca0-123">Le lecteur Windows Media peut rogner le texte du bouton pour l’ajuster à l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="fcca0-123">Windows Media Player may crop button text to fit the available space.</span></span> <span data-ttu-id="fcca0-124">Le joueur utilise toujours la police Tahoma gras à 8 points pour ce texte.</span><span class="sxs-lookup"><span data-stu-id="fcca0-124">The Player always uses the Tahoma bold 8-point font for this text.</span></span> <span data-ttu-id="fcca0-125">Il y a deux lignes disponibles pour afficher le texte du bouton, mais le lecteur ne renvoie pas automatiquement le texte de la première ligne à la seconde.</span><span class="sxs-lookup"><span data-stu-id="fcca0-125">There are two lines available to display button text, but the Player does not automatically wrap text from the first line to the second.</span></span> <span data-ttu-id="fcca0-126">Pour spécifier un saut de ligne dans le texte du bouton, insérez la nouvelle séquence d’échappement « \\ n » dans votre chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="fcca0-126">To specify a line break in the button text, insert the new line escape sequence "\\n" in your text string.</span></span>

<span data-ttu-id="fcca0-127">La chaîne de texte s’affiche également dans le menu **atteindre** de l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fcca0-127">The text string is also displayed in the **GoTo** menu in the Windows Media Player user interface.</span></span>

<span data-ttu-id="fcca0-128">Vous devez tester votre magasin en ligne à l’aide de divers paramètres d’affichage pour vous assurer que le texte s’affiche comme prévu.</span><span class="sxs-lookup"><span data-stu-id="fcca0-128">You should test your online store using a variety of display settings to ensure that text displays as you expect.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcca0-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcca0-129">Requirements</span></span>



| <span data-ttu-id="fcca0-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcca0-130">Requirement</span></span> | <span data-ttu-id="fcca0-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcca0-131">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="fcca0-132">Version</span><span class="sxs-lookup"><span data-stu-id="fcca0-132">Version</span></span><br/> | <span data-ttu-id="fcca0-133">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fcca0-133">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fcca0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcca0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcca0-135">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="fcca0-135">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="fcca0-136">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="fcca0-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="fcca0-137">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="fcca0-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





