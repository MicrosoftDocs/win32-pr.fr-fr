---
title: Message TB_INSERTMARKHITTEST (commctrl. h)
description: Récupère les informations sur les marques d’insertion pour un point dans une barre d’outils.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- TB_INSERTMARKHITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032684"
---
# <a name="tb_insertmarkhittest-message"></a><span data-ttu-id="86508-104">TO \_ INSERTMARKHITTEST message</span><span class="sxs-lookup"><span data-stu-id="86508-104">TB\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="86508-105">Récupère les informations sur les marques d’insertion pour un point dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="86508-105">Retrieves the insertion mark information for a point in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="86508-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86508-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86508-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86508-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86508-108">Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui contient les coordonnées de test de positionnement par rapport à la zone cliente de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="86508-108">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the hit test coordinates, relative to the client area of the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="86508-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86508-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86508-110">Pointeur vers une structure [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) qui reçoit les informations sur les marques d’insertion.</span><span class="sxs-lookup"><span data-stu-id="86508-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86508-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86508-111">Return value</span></span>

<span data-ttu-id="86508-112">Retourne une valeur différente de zéro si le point est une marque d’insertion, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="86508-112">Returns nonzero if the point is an insertion mark, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="86508-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86508-113">Requirements</span></span>



| <span data-ttu-id="86508-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86508-114">Requirement</span></span> | <span data-ttu-id="86508-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="86508-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86508-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86508-116">Minimum supported client</span></span><br/> | <span data-ttu-id="86508-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86508-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86508-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86508-118">Minimum supported server</span></span><br/> | <span data-ttu-id="86508-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86508-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86508-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="86508-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="86508-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86508-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

