---
title: Message TTM_ENUMTOOLS (commctrl. h)
description: Récupère les informations qu’un contrôle ToolTip gère à propos de l’outil actuel \ 8212 ; autrement dit, l’outil pour lequel l’info-bulle affiche actuellement du texte.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67f23a145838aa3562c81e78fb82c3ea66320df
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327134"
---
# <a name="ttm_enumtools-message"></a><span data-ttu-id="ffd73-104">\_Message atténuation ENUMTOOLS</span><span class="sxs-lookup"><span data-stu-id="ffd73-104">TTM\_ENUMTOOLS message</span></span>

<span data-ttu-id="ffd73-105">Récupère les informations qu’un contrôle ToolTip gère à propos de l’outil actuel, c’est-à-dire l’outil pour lequel l’info-bulle affiche actuellement du texte.</span><span class="sxs-lookup"><span data-stu-id="ffd73-105">Retrieves the information that a tooltip control maintains about the current tool that is, the tool for which the tooltip is currently displaying text.</span></span>

## <a name="parameters"></a><span data-ttu-id="ffd73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffd73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd73-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ffd73-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffd73-108">Index de base zéro de l’outil pour lequel des informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="ffd73-108">Zero-based index of the tool for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="ffd73-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ffd73-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffd73-110">Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) qui reçoit des informations sur l’outil.</span><span class="sxs-lookup"><span data-stu-id="ffd73-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the tool.</span></span> <span data-ttu-id="ffd73-111">Définissez le membre **cbSize** de cette structure sur sizeof (TOOLINFO) avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="ffd73-111">Set the **cbSize** member of this structure to sizeof(TOOLINFO) before sending this message.</span></span> <span data-ttu-id="ffd73-112">Allouez une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ffd73-112">Allocate a buffer.</span></span> <span data-ttu-id="ffd73-113">Définissez le membre **lpszText** pour qu’il pointe vers la mémoire tampon pour recevoir le texte de l’outil.</span><span class="sxs-lookup"><span data-stu-id="ffd73-113">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span> <span data-ttu-id="ffd73-114">Il n’existe aucun moyen de déterminer la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="ffd73-114">There is no way to determine the required buffer size.</span></span> <span data-ttu-id="ffd73-115">Toutefois, le texte d’outil, tel qu’il est retourné au membre **lpszText** de la structure **TOOLINFO** , a une longueur maximale de 80 **TCHARs**, y compris le caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="ffd73-115">However, tool text, as returned at the **lpszText** member of the **TOOLINFO** structure, has a maximum length of 80 **TCHARs**, including the terminating **NULL**.</span></span> <span data-ttu-id="ffd73-116">Si le texte dépasse cette longueur, il est tronqué.</span><span class="sxs-lookup"><span data-stu-id="ffd73-116">If the text exceeds this length, it is truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffd73-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ffd73-117">Return value</span></span>

<span data-ttu-id="ffd73-118">Retourne la **valeur false** , qu’un outil ait ou non été énuméré.</span><span class="sxs-lookup"><span data-stu-id="ffd73-118">Returns **FALSE** whether or not a tool was enumerated.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd73-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="ffd73-119">Remarks</span></span>

<span data-ttu-id="ffd73-120">**Avertissement de sécurité :** L’utilisation de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="ffd73-120">**Security Warning:** Using this message might compromise the security of your program.</span></span> <span data-ttu-id="ffd73-121">Ce message ne permet pas au destinataire du message de connaître la taille de la mémoire tampon ou de spécifier la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ffd73-121">This message does not provide a way for the message receiver to know the size of the buffer or to specify the size of the buffer.</span></span> <span data-ttu-id="ffd73-122">Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="ffd73-122">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd73-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffd73-123">Requirements</span></span>



| <span data-ttu-id="ffd73-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffd73-124">Requirement</span></span> | <span data-ttu-id="ffd73-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffd73-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd73-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffd73-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd73-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffd73-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ffd73-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffd73-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd73-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffd73-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ffd73-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffd73-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd73-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffd73-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ffd73-132">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="ffd73-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ffd73-133">**Atténuation \_ ENUMTOOLSW** (Unicode) et **atténuation \_ ENUMTOOLSA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ffd73-133">**TTM\_ENUMTOOLSW** (Unicode) and **TTM\_ENUMTOOLSA** (ANSI)</span></span><br/>               |



 

 





