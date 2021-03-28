---
description: Envoyé à une application qui a initié une carte d’apprentissage avec l’aide de Windows.
title: Message WM_TCARD (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202766"
---
# <a name="wm_tcard-message"></a><span data-ttu-id="cb99c-103">\_Message WM TCARD</span><span class="sxs-lookup"><span data-stu-id="cb99c-103">WM\_TCARD message</span></span>

<span data-ttu-id="cb99c-104">Envoyé à une application qui a initié une carte d’apprentissage avec l’aide de Windows.</span><span class="sxs-lookup"><span data-stu-id="cb99c-104">Sent to an application that has initiated a training card with Windows Help.</span></span> <span data-ttu-id="cb99c-105">Le message informe l’application lorsque l’utilisateur clique sur un bouton autorisé.</span><span class="sxs-lookup"><span data-stu-id="cb99c-105">The message informs the application when the user clicks an authorable button.</span></span> <span data-ttu-id="cb99c-106">Une application initie une carte d’apprentissage en spécifiant la \_ commande help TCARD dans un appel à la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .</span><span class="sxs-lookup"><span data-stu-id="cb99c-106">An application initiates a training card by specifying the HELP\_TCARD command in a call to the [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb99c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb99c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb99c-108">*idAction*</span><span class="sxs-lookup"><span data-stu-id="cb99c-108">*idAction*</span></span> 
</dt> <dd>

<span data-ttu-id="cb99c-109">Valeur qui indique l’action effectuée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb99c-109">A value that indicates the action the user has taken.</span></span> <span data-ttu-id="cb99c-110">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb99c-110">This can be one of the following values.</span></span>

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span data-ttu-id="cb99c-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span><span class="sxs-lookup"><span data-stu-id="cb99c-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-112">L’utilisateur a cliqué sur un bouton d' **annulation** autorisé.</span><span class="sxs-lookup"><span data-stu-id="cb99c-112">The user clicked an authorable **Abort** button.</span></span>

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span data-ttu-id="cb99c-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="cb99c-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-114">L’utilisateur a cliqué sur un bouton d' **annulation** autorisé.</span><span class="sxs-lookup"><span data-stu-id="cb99c-114">The user clicked an authorable **Cancel** button.</span></span>

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span data-ttu-id="cb99c-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span><span class="sxs-lookup"><span data-stu-id="cb99c-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-116">L’utilisateur a fermé la carte de formation.</span><span class="sxs-lookup"><span data-stu-id="cb99c-116">The user closed the training card.</span></span>

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span data-ttu-id="cb99c-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span><span class="sxs-lookup"><span data-stu-id="cb99c-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-118">L’utilisateur a cliqué sur un bouton **d’aide** Windows autorisé.</span><span class="sxs-lookup"><span data-stu-id="cb99c-118">The user clicked an authorable Windows **Help** button.</span></span>

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span data-ttu-id="cb99c-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span><span class="sxs-lookup"><span data-stu-id="cb99c-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-120">L’utilisateur a cliqué sur un bouton de l’autorisation autoriser **Ignorer** .</span><span class="sxs-lookup"><span data-stu-id="cb99c-120">The user clicked an authorable **Ignore** button.</span></span>

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span data-ttu-id="cb99c-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span><span class="sxs-lookup"><span data-stu-id="cb99c-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-122">L’utilisateur a cliqué sur un bouton autorisé **OK** .</span><span class="sxs-lookup"><span data-stu-id="cb99c-122">The user clicked an authorable **OK** button.</span></span>

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span data-ttu-id="cb99c-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span><span class="sxs-lookup"><span data-stu-id="cb99c-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-124">L’utilisateur a cliqué sur un bouton **sans** autorisation.</span><span class="sxs-lookup"><span data-stu-id="cb99c-124">The user clicked an authorable **No** button.</span></span>

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span data-ttu-id="cb99c-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span><span class="sxs-lookup"><span data-stu-id="cb99c-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-126">L’utilisateur a cliqué sur un bouton de **nouvelle tentative** autorisé.</span><span class="sxs-lookup"><span data-stu-id="cb99c-126">The user clicked an authorable **Retry** button.</span></span>

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span data-ttu-id="cb99c-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**AIDE sur les \_ \_ données TCARD**</span><span class="sxs-lookup"><span data-stu-id="cb99c-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**HELP\_TCARD\_DATA**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-128">L’utilisateur a cliqué sur un bouton autorisé.</span><span class="sxs-lookup"><span data-stu-id="cb99c-128">The user clicked an authorable button.</span></span> <span data-ttu-id="cb99c-129">Le paramètre *dwActionData* contient un entier long spécifié par l’auteur de l’aide.</span><span class="sxs-lookup"><span data-stu-id="cb99c-129">The *dwActionData* parameter contains a long integer specified by the Help author.</span></span>

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span data-ttu-id="cb99c-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**AIDE \_ TCARD \_ autre \_ appelant**</span><span class="sxs-lookup"><span data-stu-id="cb99c-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**HELP\_TCARD\_OTHER\_CALLER**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-131">Une autre application a demandé des cartes de formation.</span><span class="sxs-lookup"><span data-stu-id="cb99c-131">Another application has requested training cards.</span></span>

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span data-ttu-id="cb99c-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span><span class="sxs-lookup"><span data-stu-id="cb99c-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span></span>


</dt> <dd>

<span data-ttu-id="cb99c-133">L’utilisateur a cliqué sur un bouton autoriser **Oui** .</span><span class="sxs-lookup"><span data-stu-id="cb99c-133">The user clicked an authorable **Yes** button.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cb99c-134">*dwActionData*</span><span class="sxs-lookup"><span data-stu-id="cb99c-134">*dwActionData*</span></span> 
</dt> <dd>

<span data-ttu-id="cb99c-135">Si *idAction* spécifie Help \_ TCARD \_ Data, ce paramètre est une **valeur de type long** spécifiée par l’auteur de l’aide.</span><span class="sxs-lookup"><span data-stu-id="cb99c-135">If *idAction* specifies HELP\_TCARD\_DATA, this parameter is a **long** specified by the Help author.</span></span> <span data-ttu-id="cb99c-136">Dans le cas contraire, ce paramètre est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cb99c-136">Otherwise, this parameter is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb99c-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb99c-137">Return value</span></span>

<span data-ttu-id="cb99c-138">La valeur de retour est ignorée ; utilisez zéro.</span><span class="sxs-lookup"><span data-stu-id="cb99c-138">The return value is ignored; use zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb99c-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cb99c-139">Requirements</span></span>



| <span data-ttu-id="cb99c-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb99c-140">Requirement</span></span> | <span data-ttu-id="cb99c-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb99c-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb99c-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb99c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="cb99c-143">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb99c-143">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cb99c-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb99c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="cb99c-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb99c-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cb99c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb99c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb99c-147"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb99c-147"><dt>Winuser.h</dt></span></span> </dl> |



 

 




