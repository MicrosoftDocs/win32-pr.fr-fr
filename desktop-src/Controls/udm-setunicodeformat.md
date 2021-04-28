---
title: Message UDM_SETUNICODEFORMAT (commctrl. h)
description: 'UDM_SETUNICODEFORMAT message : définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.'
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
ms.openlocfilehash: 09eeb63d5c06a5e64c354c950cd84fc451568d36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116537"
---
# <a name="udm_setunicodeformat-message"></a><span data-ttu-id="ecdb7-105">\_Message SETUNICODEFORMAT UDM</span><span class="sxs-lookup"><span data-stu-id="ecdb7-105">UDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="ecdb7-106">Définit l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="ecdb7-107">Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecdb7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecdb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecdb7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecdb7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecdb7-110">Détermine le jeu de caractères utilisé par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="ecdb7-111">Si cette valeur est **true**, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="ecdb7-112">Si cette valeur est **false**, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="ecdb7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecdb7-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ecdb7-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecdb7-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ecdb7-115">Return value</span></span>

<span data-ttu-id="ecdb7-116">Retourne l’indicateur de format Unicode précédent pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ecdb7-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecdb7-117">Notes </span><span class="sxs-lookup"><span data-stu-id="ecdb7-117">Remarks</span></span>

<span data-ttu-id="ecdb7-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="ecdb7-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecdb7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecdb7-119">Requirements</span></span>



| <span data-ttu-id="ecdb7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecdb7-120">Requirement</span></span> | <span data-ttu-id="ecdb7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecdb7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecdb7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecdb7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ecdb7-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecdb7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ecdb7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecdb7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ecdb7-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecdb7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ecdb7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecdb7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecdb7-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecdb7-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecdb7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecdb7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecdb7-129">**\_GETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="ecdb7-129">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md)
</dt> </dl>

 

 





