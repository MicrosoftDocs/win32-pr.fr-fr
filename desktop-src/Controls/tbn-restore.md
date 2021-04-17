---
title: TBN_RESTORE le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils qu’une barre d’outils est en cours de restauration. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- Contrôles Windows de code de notification TBN_RESTORE
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466219"
---
# <a name="tbn_restore-notification-code"></a><span data-ttu-id="78fba-105">TBN le \_ Code de notification de restauration</span><span class="sxs-lookup"><span data-stu-id="78fba-105">TBN\_RESTORE notification code</span></span>

<span data-ttu-id="78fba-106">Avertit la fenêtre parente d’une barre d’outils qu’une barre d’outils est en cours de restauration.</span><span class="sxs-lookup"><span data-stu-id="78fba-106">Notifies a toolbar's parent window that a toolbar is in the process of being restored.</span></span> <span data-ttu-id="78fba-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="78fba-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="78fba-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78fba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78fba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78fba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78fba-110">Pointeur vers une structure [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) .</span><span class="sxs-lookup"><span data-stu-id="78fba-110">Pointer to an [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78fba-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78fba-111">Return value</span></span>

<span data-ttu-id="78fba-112">L’application doit retourner zéro en réponse au premier code de notification de **\_ restauration TBN** reçu au début du processus de restauration pour continuer à restaurer les informations du bouton.</span><span class="sxs-lookup"><span data-stu-id="78fba-112">The application should return zero in response to the first **TBN\_RESTORE** notification code received at the start of the restore process to continue restoring the button information.</span></span> <span data-ttu-id="78fba-113">Si l’application retourne une valeur différente de zéro, le processus de restauration est annulé.</span><span class="sxs-lookup"><span data-stu-id="78fba-113">If the application returns a nonzero value, the restore process is canceled.</span></span>

## <a name="remarks"></a><span data-ttu-id="78fba-114">Notes</span><span class="sxs-lookup"><span data-stu-id="78fba-114">Remarks</span></span>

<span data-ttu-id="78fba-115">L’application recevra ce code de notification une fois au démarrage du processus de restauration et une fois pour chaque bouton.</span><span class="sxs-lookup"><span data-stu-id="78fba-115">The application will receive this notification code once at the start of the restore process and once for each button.</span></span> <span data-ttu-id="78fba-116">Ce code de notification vous donne la possibilité d’extraire les informations du flux de données que vous avez enregistré précédemment.</span><span class="sxs-lookup"><span data-stu-id="78fba-116">This notification code gives you an opportunity to extract the information from the data stream that you saved previously.</span></span> <span data-ttu-id="78fba-117">Si vous n’avez enregistré aucune information, ignorez le code de notification.</span><span class="sxs-lookup"><span data-stu-id="78fba-117">If you haven't saved any information, ignore the notification code.</span></span> <span data-ttu-id="78fba-118">Pour plus d’informations sur la façon de gérer **TBN \_ Restore**, consultez Personnalisation de la [barre d’outils](toolbar-controls-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="78fba-118">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle **TBN\_RESTORE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="78fba-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78fba-119">Requirements</span></span>



| <span data-ttu-id="78fba-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78fba-120">Requirement</span></span> | <span data-ttu-id="78fba-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="78fba-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78fba-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78fba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="78fba-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78fba-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78fba-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78fba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="78fba-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78fba-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78fba-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="78fba-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="78fba-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="78fba-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





