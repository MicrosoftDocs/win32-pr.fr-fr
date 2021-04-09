---
title: Message UDM_SETUNICODEFORMAT (commctrl. h)
description: Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.
ms.assetid: abe882db-bf32-40b0-a1c0-3e89cdc93fe7
keywords:
- UDM_SETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3f9dbc1e19fdb43aa0b7d5e6de6fdddd308eb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032914"
---
# <a name="udm_setunicodeformat-message"></a><span data-ttu-id="3a593-105">\_Message SETUNICODEFORMAT UDM</span><span class="sxs-lookup"><span data-stu-id="3a593-105">UDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="3a593-106">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="3a593-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="3a593-107">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="3a593-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a593-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a593-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a593-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a593-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a593-110">Détermine le jeu de caractères utilisé par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="3a593-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="3a593-111">Si cette valeur est **true**, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="3a593-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="3a593-112">Si cette valeur est **false**, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="3a593-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="3a593-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a593-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3a593-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3a593-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a593-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a593-115">Return value</span></span>

<span data-ttu-id="3a593-116">Retourne l’indicateur de format Unicode précédent pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="3a593-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a593-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3a593-117">Remarks</span></span>

<span data-ttu-id="3a593-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="3a593-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a593-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a593-119">Requirements</span></span>



| <span data-ttu-id="3a593-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a593-120">Requirement</span></span> | <span data-ttu-id="3a593-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a593-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a593-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a593-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3a593-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a593-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a593-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a593-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3a593-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a593-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a593-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a593-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a593-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a593-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a593-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a593-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a593-129">**\_GETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="3a593-129">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md)
</dt> </dl>

 

 





