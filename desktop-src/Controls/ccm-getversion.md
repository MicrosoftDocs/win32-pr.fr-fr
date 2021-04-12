---
title: Message CCM_GETVERSION (commctrl. h)
description: Obtient le numéro de version d’un contrôle défini par le message CCM SETVERSION le plus récent \_ .
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- CCM_GETVERSION les contrôles de message Windows
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104512"
---
# <a name="ccm_getversion-message"></a><span data-ttu-id="83826-104">Message de l’outil CCM. \_</span><span class="sxs-lookup"><span data-stu-id="83826-104">CCM\_GETVERSION message</span></span>

<span data-ttu-id="83826-105">Obtient le numéro de version d’un contrôle défini par le message [**CCM \_ SETVERSION**](ccm-setversion.md) le plus récent.</span><span class="sxs-lookup"><span data-stu-id="83826-105">Gets the version number for a control set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="83826-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83826-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83826-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83826-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="83826-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="83826-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="83826-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83826-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="83826-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="83826-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83826-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83826-111">Return value</span></span>

<span data-ttu-id="83826-112">Retourne le numéro de version défini par le dernier message [**CCM \_ SETVERSION**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="83826-112">Returns the version number set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="83826-113">Si aucun message de ce type n’a été envoyé, elle retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="83826-113">If no such message has been sent, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="83826-114">Notes</span><span class="sxs-lookup"><span data-stu-id="83826-114">Remarks</span></span>

<span data-ttu-id="83826-115">Ce message ne retourne pas la version de la DLL.</span><span class="sxs-lookup"><span data-stu-id="83826-115">This message does not return the DLL version.</span></span> <span data-ttu-id="83826-116">Pour plus d’informations sur l’utilisation de [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) pour récupérer la version actuelle de la dll, consultez [versions de Shell](common-control-versions.md) .</span><span class="sxs-lookup"><span data-stu-id="83826-116">See [Shell Versions](common-control-versions.md) for a discussion of how to use [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) to retrieve the current DLL version.</span></span>

> [!Note]  
> <span data-ttu-id="83826-117">Le numéro de version est défini sur un contrôle en fonction du contrôle et peut ne pas être le même pour tous les contrôles.</span><span class="sxs-lookup"><span data-stu-id="83826-117">The version number is set on a control by control basis, and may not be the same for all controls.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="83826-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83826-118">Requirements</span></span>



| <span data-ttu-id="83826-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83826-119">Requirement</span></span> | <span data-ttu-id="83826-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="83826-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83826-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83826-121">Minimum supported client</span></span><br/> | <span data-ttu-id="83826-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83826-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83826-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83826-123">Minimum supported server</span></span><br/> | <span data-ttu-id="83826-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83826-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83826-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="83826-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="83826-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83826-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

