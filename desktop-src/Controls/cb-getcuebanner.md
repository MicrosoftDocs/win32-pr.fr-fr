---
title: Message CB_GETCUEBANNER (winuser. h)
description: Obtient le texte de bannière de signal affiché dans le contrôle d’édition d’une zone de liste déroulante. Envoyez ce message explicitement ou à l’aide de la \_ macro ComboBox GetCueBannerText.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- CB_GETCUEBANNER les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843822"
---
# <a name="cb_getcuebanner-message"></a><span data-ttu-id="899c6-105">\_Message GETCUEBANNER CB</span><span class="sxs-lookup"><span data-stu-id="899c6-105">CB\_GETCUEBANNER message</span></span>

<span data-ttu-id="899c6-106">Obtient le texte de bannière de signal affiché dans le contrôle d’édition d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="899c6-106">Gets the cue banner text displayed in the edit control of a combo box.</span></span> <span data-ttu-id="899c6-107">Envoyez ce message explicitement ou à l’aide de la macro [**ComboBox \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) .</span><span class="sxs-lookup"><span data-stu-id="899c6-107">Send this message explicitly or by using the [**ComboBox\_GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="899c6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="899c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="899c6-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="899c6-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="899c6-110">Pointeur vers une mémoire tampon de chaîne Unicode qui reçoit le texte de bannière de signal.</span><span class="sxs-lookup"><span data-stu-id="899c6-110">A pointer to a Unicode string buffer that receives the cue banner text.</span></span> <span data-ttu-id="899c6-111">L’application appelante est chargée d’allouer la mémoire pour la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="899c6-111">The calling application is responsible for allocating the memory for the buffer.</span></span> <span data-ttu-id="899c6-112">La taille de la mémoire tampon doit être égale à la longueur de la chaîne de bannière de signal dans **WCHARs**, plus 1 pour le paramètre de fin **null** **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="899c6-112">The buffer size must be equal to the length of the cue banner string in **WCHARs**, plus 1 for the terminating **NULL** **WCHAR**.</span></span>

</dd> <dt>

<span data-ttu-id="899c6-113">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="899c6-113">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="899c6-114">Taille de la mémoire tampon vers laquelle pointe *lpcwText* dans **WCHARs**.</span><span class="sxs-lookup"><span data-stu-id="899c6-114">The size of the buffer pointed to by *lpcwText* in **WCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="899c6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="899c6-115">Return value</span></span>

<span data-ttu-id="899c6-116">Retourne 1 en cas de réussite, ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="899c6-116">Returns 1 if successful, or an error value otherwise.</span></span>

<span data-ttu-id="899c6-117">S’il n’y a aucun texte de bannière de signal à obtenir, la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="899c6-117">If there is no cue banner text to get, the return value is 0.</span></span> <span data-ttu-id="899c6-118">Si l’application appelante ne parvient pas à allouer une mémoire tampon, ou à définir *lParam* avant d’envoyer ce message, un comportement non défini peut se produire et la valeur de retour peut ne pas être fiable.</span><span class="sxs-lookup"><span data-stu-id="899c6-118">If the calling application fails to allocate a buffer, or set *lParam* before sending this message, undefined behavior may result and the return value may not be reliable.</span></span>

## <a name="requirements"></a><span data-ttu-id="899c6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="899c6-119">Requirements</span></span>



| <span data-ttu-id="899c6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="899c6-120">Requirement</span></span> | <span data-ttu-id="899c6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="899c6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="899c6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="899c6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="899c6-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="899c6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="899c6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="899c6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="899c6-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="899c6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="899c6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="899c6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="899c6-127"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="899c6-127"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="899c6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="899c6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="899c6-129">Fonctionnalités de zone de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="899c6-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





