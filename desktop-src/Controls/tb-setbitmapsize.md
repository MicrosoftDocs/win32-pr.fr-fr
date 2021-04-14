---
title: Message TB_SETBITMAPSIZE (commctrl. h)
description: Définit la taille des images bitmap à ajouter à une barre d’outils.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- TB_SETBITMAPSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464255"
---
# <a name="tb_setbitmapsize-message"></a><span data-ttu-id="5411f-104">TO \_ SETBITMAPSIZE message</span><span class="sxs-lookup"><span data-stu-id="5411f-104">TB\_SETBITMAPSIZE message</span></span>

<span data-ttu-id="5411f-105">Définit la taille des images bitmap à ajouter à une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="5411f-105">Sets the size of the bitmapped images to be added to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5411f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5411f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5411f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5411f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5411f-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5411f-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5411f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5411f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5411f-110">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la largeur, en pixels, des images bitmap.</span><span class="sxs-lookup"><span data-stu-id="5411f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the bitmapped images.</span></span> <span data-ttu-id="5411f-111">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la hauteur, en pixels, des images bitmap.</span><span class="sxs-lookup"><span data-stu-id="5411f-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the bitmapped images.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5411f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5411f-112">Return value</span></span>

<span data-ttu-id="5411f-113">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5411f-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5411f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5411f-114">Remarks</span></span>

<span data-ttu-id="5411f-115">La taille ne peut être définie qu’avant l’ajout de bitmaps à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="5411f-115">The size can be set only before adding any bitmaps to the toolbar.</span></span> <span data-ttu-id="5411f-116">Si une application ne définit pas explicitement la taille de la bitmap, la taille par défaut est de 16 par 15 pixels.</span><span class="sxs-lookup"><span data-stu-id="5411f-116">If an application does not explicitly set the bitmap size, the size defaults to 16 by 15 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="5411f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5411f-117">Requirements</span></span>



| <span data-ttu-id="5411f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5411f-118">Requirement</span></span> | <span data-ttu-id="5411f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5411f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5411f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5411f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5411f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5411f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5411f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5411f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5411f-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5411f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5411f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5411f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5411f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5411f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

