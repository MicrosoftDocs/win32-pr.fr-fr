---
title: External. SelectedTaskPane
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété SelectedTaskPane spécifie ou récupère le volet des tâches actuellement sélectionné.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- External. SelectedTaskPane Windows Media Player
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532725"
---
# <a name="externalselectedtaskpane"></a><span data-ttu-id="b5bbd-106">External. SelectedTaskPane</span><span class="sxs-lookup"><span data-stu-id="b5bbd-106">External.SelectedTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="b5bbd-107">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="b5bbd-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b5bbd-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b5bbd-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b5bbd-109">La propriété **SelectedTaskPane** spécifie ou récupère le volet des tâches actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b5bbd-109">The **SelectedTaskPane** property specifies or retrieves the currently selected task pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5bbd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5bbd-110">Syntax</span></span>

<span data-ttu-id="b5bbd-111">Window. external. SelectedTaskPane = *servicetask*</span><span class="sxs-lookup"><span data-stu-id="b5bbd-111">window.external.SelectedTaskPane = *servicetask*</span></span>

## <a name="possible-values"></a><span data-ttu-id="b5bbd-112">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b5bbd-112">Possible Values</span></span>

<span data-ttu-id="b5bbd-113">Cette propriété est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b5bbd-113">This property is a read/write **String**.</span></span> <span data-ttu-id="b5bbd-114">Les valeurs possibles sont « ServiceTask1 », « ServiceTask2 » et « ServiceTask3 ».</span><span class="sxs-lookup"><span data-stu-id="b5bbd-114">Possible values are "ServiceTask1", "ServiceTask2", and "ServiceTask3".</span></span>

## <a name="remarks"></a><span data-ttu-id="b5bbd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b5bbd-115">Remarks</span></span>

<span data-ttu-id="b5bbd-116">Si vous spécifiez une valeur pour cette propriété, le bouton correspondant à ce volet est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="b5bbd-116">Specifying a value for this property highlights the button for that pane.</span></span> <span data-ttu-id="b5bbd-117">Elle ne rend pas le volet de tâches spécifié actif.</span><span class="sxs-lookup"><span data-stu-id="b5bbd-117">It does not make the specified task pane active.</span></span> <span data-ttu-id="b5bbd-118">Vous devez spécifier une valeur pour cette propriété afin de définir le bouton du volet de tâches actuel pour votre page Web lors du chargement de la page pour vous assurer que le bouton de volet de tâches correct est actif.</span><span class="sxs-lookup"><span data-stu-id="b5bbd-118">You should specify a value for this property to set the current task pane button for your webpage when the page loads to ensure that the correct task pane button is active.</span></span>

<span data-ttu-id="b5bbd-119">Pour rendre un volet de tâches particulier actif, utilisez la méthode **NavigateTaskPaneURL** .</span><span class="sxs-lookup"><span data-stu-id="b5bbd-119">To make a particular task pane the active one, use the **NavigateTaskPaneURL** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5bbd-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5bbd-120">Requirements</span></span>



| <span data-ttu-id="b5bbd-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5bbd-121">Requirement</span></span> | <span data-ttu-id="b5bbd-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5bbd-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5bbd-123">Version</span><span class="sxs-lookup"><span data-stu-id="b5bbd-123">Version</span></span><br/> | <span data-ttu-id="b5bbd-124">Lecteur Windows Media 10 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b5bbd-124">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="b5bbd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b5bbd-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5bbd-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5bbd-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5bbd-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5bbd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5bbd-128">**Objet externe pour les magasins de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="b5bbd-128">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b5bbd-129">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="b5bbd-129">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





