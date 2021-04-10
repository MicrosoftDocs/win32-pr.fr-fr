---
title: Message TB_GETBITMAPFLAGS (commctrl. h)
description: Récupère les indicateurs qui décrivent le type de bitmap à utiliser.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- TB_GETBITMAPFLAGS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106603"
---
# <a name="tb_getbitmapflags-message"></a><span data-ttu-id="13cd2-104">TO \_ GETBITMAPFLAGS message</span><span class="sxs-lookup"><span data-stu-id="13cd2-104">TB\_GETBITMAPFLAGS message</span></span>

<span data-ttu-id="13cd2-105">Récupère les indicateurs qui décrivent le type de bitmap à utiliser.</span><span class="sxs-lookup"><span data-stu-id="13cd2-105">Retrieves the flags that describe the type of bitmap to be used.</span></span>

## <a name="parameters"></a><span data-ttu-id="13cd2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13cd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13cd2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13cd2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="13cd2-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="13cd2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="13cd2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13cd2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="13cd2-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="13cd2-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13cd2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13cd2-111">Return value</span></span>

<span data-ttu-id="13cd2-112">Retourne une valeur **DWORD** qui décrit le type de bitmap à utiliser.</span><span class="sxs-lookup"><span data-stu-id="13cd2-112">Returns a **DWORD** value that describes the type of bitmap that should be used.</span></span> <span data-ttu-id="13cd2-113">Si la valeur de retour est définie sur l' \_ indicateur TBBF large, les applications doivent utiliser des bitmaps de grande taille (24 x 24); dans le cas contraire, les applications doivent utiliser de petites bitmaps (16 x 16).</span><span class="sxs-lookup"><span data-stu-id="13cd2-113">If this return value has the TBBF\_LARGE flag set, applications should use large bitmaps (24 x 24); otherwise, applications should use small bitmaps (16 x 16).</span></span> <span data-ttu-id="13cd2-114">Tous les autres bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="13cd2-114">All other bits are reserved.</span></span>

## <a name="remarks"></a><span data-ttu-id="13cd2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="13cd2-115">Remarks</span></span>

<span data-ttu-id="13cd2-116">La valeur retournée par **to \_ GETBITMAPFLAGS** est uniquement consultative.</span><span class="sxs-lookup"><span data-stu-id="13cd2-116">The value returned by **TB\_GETBITMAPFLAGS** is only advisory.</span></span> <span data-ttu-id="13cd2-117">Le contrôle ToolBar recommande des bitmaps de grande taille ou de petite taille selon que l’utilisateur a choisi des polices de grande taille ou de petite taille.</span><span class="sxs-lookup"><span data-stu-id="13cd2-117">The toolbar control recommends large or small bitmaps based upon whether the user has chosen large or small fonts.</span></span>

## <a name="requirements"></a><span data-ttu-id="13cd2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13cd2-118">Requirements</span></span>



| <span data-ttu-id="13cd2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13cd2-119">Requirement</span></span> | <span data-ttu-id="13cd2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="13cd2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13cd2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13cd2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="13cd2-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13cd2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13cd2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13cd2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="13cd2-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13cd2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="13cd2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="13cd2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="13cd2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="13cd2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





