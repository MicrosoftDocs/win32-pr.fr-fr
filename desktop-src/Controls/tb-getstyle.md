---
title: Message TB_GETSTYLE (commctrl. h)
description: Récupère les styles en cours d’utilisation pour un contrôle ToolBar.
ms.assetid: 6fbe8733-79df-462e-acb6-6568105e5058
keywords:
- TB_GETSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8de0addae729a4a8c641d21fd1771137d8c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466322"
---
# <a name="tb_getstyle-message"></a><span data-ttu-id="3603b-104">TO \_ GETSTYLE message</span><span class="sxs-lookup"><span data-stu-id="3603b-104">TB\_GETSTYLE message</span></span>

<span data-ttu-id="3603b-105">Récupère les styles en cours d’utilisation pour un contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="3603b-105">Retrieves the styles currently in use for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3603b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3603b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3603b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3603b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3603b-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3603b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3603b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3603b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3603b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3603b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3603b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3603b-111">Return value</span></span>

<span data-ttu-id="3603b-112">Retourne une valeur **DWORD** qui est une combinaison de [styles de contrôle de barre d’outils](toolbar-control-and-button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="3603b-112">Returns a **DWORD** value that is a combination of [toolbar control styles](toolbar-control-and-button-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3603b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3603b-113">Requirements</span></span>



| <span data-ttu-id="3603b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3603b-114">Requirement</span></span> | <span data-ttu-id="3603b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3603b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3603b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3603b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3603b-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3603b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3603b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3603b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3603b-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3603b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3603b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3603b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3603b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3603b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





