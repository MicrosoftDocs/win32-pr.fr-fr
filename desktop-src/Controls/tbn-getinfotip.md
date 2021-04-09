---
title: TBN_GETINFOTIP le code de notification (commctrl. h)
description: Récupère les informations de l’info-bulle d’un élément de barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- Contrôles Windows de code de notification TBN_GETINFOTIP
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032605"
---
# <a name="tbn_getinfotip-notification-code"></a><span data-ttu-id="35b9f-105">\_Code de notification TBN GETINFOTIP</span><span class="sxs-lookup"><span data-stu-id="35b9f-105">TBN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="35b9f-106">Récupère les informations de l’info-bulle d’un élément de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="35b9f-106">Retrieves infotip information for a toolbar item.</span></span> <span data-ttu-id="35b9f-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="35b9f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="35b9f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35b9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b9f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35b9f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35b9f-110">Pointeur vers une structure [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) qui contient des informations sur les éléments et reçoit des informations sur l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="35b9f-110">Pointer to an [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) structure that contains item information and receives infotip information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35b9f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35b9f-111">Return value</span></span>

<span data-ttu-id="35b9f-112">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="35b9f-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="35b9f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="35b9f-113">Remarks</span></span>

<span data-ttu-id="35b9f-114">La prise en charge de l’info-bulle dans la barre d’outils permet à la barre d’outils d’afficher des info-bulles pour les éléments dont la taille est de INFOTIPSIZE caractères.</span><span class="sxs-lookup"><span data-stu-id="35b9f-114">The infotip support in the toolbar allows the toolbar to display tooltips for items that are as large as INFOTIPSIZE characters.</span></span> <span data-ttu-id="35b9f-115">Si ce code de notification n’est pas traité, la barre d’outils utilise le texte de l’élément pour l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="35b9f-115">If this notification code is not processed, the toolbar will use the item's text for the infotip.</span></span>

## <a name="requirements"></a><span data-ttu-id="35b9f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35b9f-116">Requirements</span></span>



| <span data-ttu-id="35b9f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35b9f-117">Requirement</span></span> | <span data-ttu-id="35b9f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="35b9f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35b9f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35b9f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="35b9f-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35b9f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35b9f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35b9f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="35b9f-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35b9f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35b9f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="35b9f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="35b9f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="35b9f-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="35b9f-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="35b9f-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="35b9f-126">**TBN \_ GETINFOTIPW** (Unicode) et **TBN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="35b9f-126">**TBN\_GETINFOTIPW** (Unicode) and **TBN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





