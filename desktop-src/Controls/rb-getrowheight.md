---
title: Message RB_GETROWHEIGHT (commctrl. h)
description: Récupère la hauteur d’une ligne spécifiée dans un contrôle rebar.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- RB_GETROWHEIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843885"
---
# <a name="rb_getrowheight-message"></a><span data-ttu-id="301ba-104">\_Message GETROWHEIGHT RB</span><span class="sxs-lookup"><span data-stu-id="301ba-104">RB\_GETROWHEIGHT message</span></span>

<span data-ttu-id="301ba-105">Récupère la hauteur d’une ligne spécifiée dans un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="301ba-105">Retrieves the height of a specified row in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="301ba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="301ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="301ba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="301ba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="301ba-108">Index de base zéro d’une bande.</span><span class="sxs-lookup"><span data-stu-id="301ba-108">Zero-based index of a band.</span></span> <span data-ttu-id="301ba-109">La hauteur de la ligne qui contient la bande spécifiée est récupérée.</span><span class="sxs-lookup"><span data-stu-id="301ba-109">The height of the row that contains the specified band will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="301ba-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="301ba-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="301ba-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="301ba-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="301ba-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="301ba-112">Return value</span></span>

<span data-ttu-id="301ba-113">Retourne une valeur **uint** qui représente la hauteur de ligne, en pixels.</span><span class="sxs-lookup"><span data-stu-id="301ba-113">Returns a **UINT** value that represents the row height, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="301ba-114">Notes</span><span class="sxs-lookup"><span data-stu-id="301ba-114">Remarks</span></span>

<span data-ttu-id="301ba-115">Pour récupérer le nombre de lignes dans un contrôle rebar, utilisez le message [**RB \_ GETROWCOUNT**](rb-getrowcount.md) .</span><span class="sxs-lookup"><span data-stu-id="301ba-115">To retrieve the number of rows in a rebar control, use the [**RB\_GETROWCOUNT**](rb-getrowcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="301ba-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="301ba-116">Requirements</span></span>



| <span data-ttu-id="301ba-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="301ba-117">Requirement</span></span> | <span data-ttu-id="301ba-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="301ba-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="301ba-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="301ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="301ba-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="301ba-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="301ba-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="301ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="301ba-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="301ba-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="301ba-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="301ba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="301ba-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="301ba-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





