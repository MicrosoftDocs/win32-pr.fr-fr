---
title: Message EM_SETLANGOPTIONS (RichEdit. h)
description: Définit les options de l’éditeur de méthode d’entrée (IME) et de la prise en charge des langues asiatiques dans un contrôle RichEdit.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- EM_SETLANGOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942026"
---
# <a name="em_setlangoptions-message"></a><span data-ttu-id="724f9-104">\_Message SETLANGOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="724f9-104">EM\_SETLANGOPTIONS message</span></span>

<span data-ttu-id="724f9-105">Définit les options de l’éditeur de méthode d’entrée (IME) et de la prise en charge des langues asiatiques dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="724f9-105">Sets options for Input Method Editor (IME) and Asian language support in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="724f9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="724f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="724f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="724f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="724f9-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="724f9-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="724f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="724f9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="724f9-110">Spécifie les options de langue.</span><span class="sxs-lookup"><span data-stu-id="724f9-110">Specifies the language options.</span></span> <span data-ttu-id="724f9-111">Pour obtenir la liste des valeurs possibles, consultez [**em \_ GETLANGOPTIONS**](em-getlangoptions.md).</span><span class="sxs-lookup"><span data-stu-id="724f9-111">For a list of possible values, see [**EM\_GETLANGOPTIONS**](em-getlangoptions.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="724f9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="724f9-112">Return value</span></span>

<span data-ttu-id="724f9-113">Ce message retourne la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="724f9-113">This message returns a value of 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="724f9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="724f9-114">Remarks</span></span>

<span data-ttu-id="724f9-115">Le message **em \_ SETLANGOPTIONS** contrôle les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="724f9-115">The **EM\_SETLANGOPTIONS** message controls the following:</span></span>

-   <span data-ttu-id="724f9-116">Liaison de police automatique.</span><span class="sxs-lookup"><span data-stu-id="724f9-116">Automatic font binding.</span></span>
-   <span data-ttu-id="724f9-117">Basculement automatique du clavier.</span><span class="sxs-lookup"><span data-stu-id="724f9-117">Automatic keyboard switching.</span></span>
-   <span data-ttu-id="724f9-118">Ajustement automatique de la taille de la police.</span><span class="sxs-lookup"><span data-stu-id="724f9-118">Automatic font size adjustment.</span></span>
-   <span data-ttu-id="724f9-119">Utilisation des polices par défaut de l’interface utilisateur au lieu des polices par défaut du document.</span><span class="sxs-lookup"><span data-stu-id="724f9-119">Use of user-interface default fonts instead of document default fonts.</span></span>
-   <span data-ttu-id="724f9-120">Notifications au client lors de la composition de l’IME.</span><span class="sxs-lookup"><span data-stu-id="724f9-120">Notifications to client during IME composition.</span></span>
-   <span data-ttu-id="724f9-121">Abandon du mode de composition par l’IME.</span><span class="sxs-lookup"><span data-stu-id="724f9-121">How IME aborts composition mode.</span></span>
-   <span data-ttu-id="724f9-122">Vérification de l’orthographe, correction automatique et prédiction du clavier tactile.</span><span class="sxs-lookup"><span data-stu-id="724f9-122">Spell checking, autocorrect, and touch keyboard prediction.</span></span>

<span data-ttu-id="724f9-123">Ce message définit les valeurs de tous les indicateurs d’option de langage.</span><span class="sxs-lookup"><span data-stu-id="724f9-123">This message sets the values of all language option flags.</span></span> <span data-ttu-id="724f9-124">Pour modifier un sous-ensemble des indicateurs, envoyez le message [**em \_ GETLANGOPTIONS**](em-getlangoptions.md) pour obtenir les indicateurs d’option actuels, modifiez les indicateurs que vous devez modifier, puis envoyez le **message \_ SETLANGOPTIONS em** avec le résultat.</span><span class="sxs-lookup"><span data-stu-id="724f9-124">To change a subset of the flags, send the [**EM\_GETLANGOPTIONS**](em-getlangoptions.md) message to get the current option flags, change the flags that you need to change, and then send the **EM\_SETLANGOPTIONS** message with the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="724f9-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="724f9-125">Requirements</span></span>



| <span data-ttu-id="724f9-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="724f9-126">Requirement</span></span> | <span data-ttu-id="724f9-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="724f9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="724f9-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="724f9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="724f9-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="724f9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="724f9-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="724f9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="724f9-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="724f9-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="724f9-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="724f9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="724f9-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="724f9-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="724f9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="724f9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="724f9-135">**\_GETLANGOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="724f9-135">**EM\_GETLANGOPTIONS**</span></span>](em-getlangoptions.md)
</dt> </dl>

 

 





