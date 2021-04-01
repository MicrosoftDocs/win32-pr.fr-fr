---
description: Envoyé une fois à la fonction CPlApplet d’une application du panneau de configuration avant la publication de la DLL contenant l’application du panneau de configuration.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: Message CPL_EXIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201273"
---
# <a name="cpl_exit-message"></a><span data-ttu-id="07a82-103">\_Message de sortie cpl</span><span class="sxs-lookup"><span data-stu-id="07a82-103">CPL\_EXIT message</span></span>

<span data-ttu-id="07a82-104">Envoyé une fois à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration avant la publication de la dll contenant l’application du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="07a82-104">Sent once to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application before the DLL containing the Control Panel application is released.</span></span>

## <a name="parameters"></a><span data-ttu-id="07a82-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07a82-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07a82-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07a82-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="07a82-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="07a82-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="07a82-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07a82-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="07a82-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="07a82-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07a82-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07a82-110">Return value</span></span>

<span data-ttu-id="07a82-111">Si la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite ce message avec succès, elle doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="07a82-111">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="07a82-112">Notes</span><span class="sxs-lookup"><span data-stu-id="07a82-112">Remarks</span></span>

<span data-ttu-id="07a82-113">Ce message est envoyé après l’envoi du dernier message d' [**\_ arrêt de cpl**](cpl-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="07a82-113">This message is sent after the last [**CPL\_STOP**](cpl-stop.md) message is sent.</span></span>

<span data-ttu-id="07a82-114">En réponse à ce message, une application du panneau de configuration doit libérer toute la mémoire qu’elle a allouée et effectuer un nettoyage au niveau global.</span><span class="sxs-lookup"><span data-stu-id="07a82-114">In response to this message, a Control Panel application must free any memory that it has allocated and perform global-level cleanup.</span></span>

## <a name="requirements"></a><span data-ttu-id="07a82-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="07a82-115">Requirements</span></span>



| <span data-ttu-id="07a82-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07a82-116">Requirement</span></span> | <span data-ttu-id="07a82-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="07a82-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="07a82-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07a82-118">Minimum supported client</span></span><br/> | <span data-ttu-id="07a82-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07a82-119">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="07a82-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07a82-120">Minimum supported server</span></span><br/> | <span data-ttu-id="07a82-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07a82-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="07a82-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="07a82-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="07a82-123"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="07a82-123"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07a82-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07a82-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a82-125">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="07a82-125">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
