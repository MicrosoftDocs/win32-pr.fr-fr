---
title: Message TVM_SETUNICODEFORMAT (commctrl. h)
description: Définit l’indicateur de format de caractère Unicode pour le contrôle.
ms.assetid: e4b58ae5-6217-4a2e-80e5-3ba9e578859a
keywords:
- TVM_SETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25082347710a40f592cfd4087b19916b56cf0d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942873"
---
# <a name="tvm_setunicodeformat-message"></a><span data-ttu-id="af1a2-104">TVM \_ SETUNICODEFORMAT message</span><span class="sxs-lookup"><span data-stu-id="af1a2-104">TVM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="af1a2-105">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="af1a2-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="af1a2-106">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="af1a2-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="af1a2-107">Vous pouvez envoyer ce message explicitement ou utiliser la [**macro \_ SetUnicodeFormat TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="af1a2-107">You can send this message explicitly or use the [**TreeView\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="af1a2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af1a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af1a2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af1a2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af1a2-110">Détermine le jeu de caractères utilisé par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="af1a2-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="af1a2-111">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="af1a2-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="af1a2-112">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="af1a2-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="af1a2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af1a2-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="af1a2-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="af1a2-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af1a2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af1a2-115">Return value</span></span>

<span data-ttu-id="af1a2-116">Retourne l’indicateur de format Unicode précédent pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="af1a2-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="af1a2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="af1a2-117">Remarks</span></span>

<span data-ttu-id="af1a2-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="af1a2-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="af1a2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af1a2-119">Requirements</span></span>



| <span data-ttu-id="af1a2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af1a2-120">Requirement</span></span> | <span data-ttu-id="af1a2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="af1a2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af1a2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af1a2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af1a2-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af1a2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af1a2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af1a2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af1a2-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af1a2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af1a2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="af1a2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="af1a2-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="af1a2-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af1a2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af1a2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af1a2-129">**TVM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="af1a2-129">**TVM\_GETUNICODEFORMAT**</span></span>](tvm-getunicodeformat.md)
</dt> </dl>

 

 





