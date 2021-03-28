---
description: Envoyé à la fonction CPlApplet d’une application du panneau de configuration pour récupérer le nombre de boîtes de dialogue prises en charge par l’application.
title: Message CPL_GETCOUNT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525390"
---
# <a name="cpl_getcount-message"></a><span data-ttu-id="42282-103">\_Message Cpl GETCOUNT</span><span class="sxs-lookup"><span data-stu-id="42282-103">CPL\_GETCOUNT message</span></span>

<span data-ttu-id="42282-104">Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration pour récupérer le nombre de boîtes de dialogue prises en charge par l’application.</span><span class="sxs-lookup"><span data-stu-id="42282-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to retrieve the number of dialog boxes supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="42282-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42282-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42282-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42282-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="42282-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="42282-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="42282-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42282-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="42282-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="42282-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42282-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42282-110">Return value</span></span>

<span data-ttu-id="42282-111">La fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) retourne le nombre de boîtes de dialogue que l’application du panneau de configuration prend en charge.</span><span class="sxs-lookup"><span data-stu-id="42282-111">The [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function returns the number of dialog boxes that the Control Panel application supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="42282-112">Notes</span><span class="sxs-lookup"><span data-stu-id="42282-112">Remarks</span></span>

<span data-ttu-id="42282-113">Ce message est envoyé immédiatement après le message d' [**\_ initialisation de cpl**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="42282-113">This message is sent immediately after the [**CPL\_INIT**](cpl-init.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="42282-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="42282-114">Requirements</span></span>



| <span data-ttu-id="42282-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42282-115">Requirement</span></span> | <span data-ttu-id="42282-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="42282-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="42282-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42282-117">Minimum supported client</span></span><br/> | <span data-ttu-id="42282-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42282-118">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="42282-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42282-119">Minimum supported server</span></span><br/> | <span data-ttu-id="42282-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42282-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="42282-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="42282-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="42282-122"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42282-122"><dt>Cpl.h</dt></span></span> </dl> |



 

 
