---
title: PSN_SETACTIVE le code de notification (Prsht. h)
description: Avertit une page qu’elle va être activée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- Contrôles Windows de code de notification PSN_SETACTIVE
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942376"
---
# <a name="psn_setactive-notification-code"></a><span data-ttu-id="c1fea-105">\_Code de notification PSN</span><span class="sxs-lookup"><span data-stu-id="c1fea-105">PSN\_SETACTIVE notification code</span></span>

<span data-ttu-id="c1fea-106">Avertit une page qu’elle va être activée.</span><span class="sxs-lookup"><span data-stu-id="c1fea-106">Notifies a page that it is about to be activated.</span></span> <span data-ttu-id="c1fea-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c1fea-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c1fea-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1fea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1fea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1fea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1fea-110">Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="c1fea-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="c1fea-111">Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c1fea-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="c1fea-112">Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.</span><span class="sxs-lookup"><span data-stu-id="c1fea-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1fea-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1fea-113">Return value</span></span>

<span data-ttu-id="c1fea-114">Retourne la valeur zéro pour accepter l’activation, ou-1 pour activer la page suivante ou précédente (selon que l’utilisateur a cliqué sur le bouton **suivant** ou **précédent** ).</span><span class="sxs-lookup"><span data-stu-id="c1fea-114">Returns zero to accept the activation, or -1 to activate the next or the previous page (depending on whether the user clicked the **Next** or **Back** button).</span></span> <span data-ttu-id="c1fea-115">Pour définir l’activation sur une page particulière, retournez l’identificateur de ressource de la page.</span><span class="sxs-lookup"><span data-stu-id="c1fea-115">To set the activation to a particular page, return the resource identifier of the page.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1fea-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c1fea-116">Remarks</span></span>

<span data-ttu-id="c1fea-117">Le \_ Code de notification PSN est envoyé avant que la page ne soit visible.</span><span class="sxs-lookup"><span data-stu-id="c1fea-117">The PSN\_SETACTIVE notification code is sent before the page is visible.</span></span> <span data-ttu-id="c1fea-118">Une application peut utiliser ce code de notification pour initialiser des données dans la page.</span><span class="sxs-lookup"><span data-stu-id="c1fea-118">An application can use this notification code to initialize data in the page.</span></span>

> [!Note]  
> <span data-ttu-id="c1fea-119">La feuille de propriétés se trouve dans le processus de manipulation de la liste de pages lorsque le \_ Code de notification PSN est envoyé.</span><span class="sxs-lookup"><span data-stu-id="c1fea-119">The property sheet is in the process of manipulating the list of pages when the PSN\_SETACTIVE notification code is sent.</span></span> <span data-ttu-id="c1fea-120">N’essayez pas d’ajouter, de supprimer ou d’insérer des pages lors de la gestion de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="c1fea-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="c1fea-121">Vous obtiendrez des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="c1fea-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="c1fea-122">Pour définir la valeur de retour, la procédure de la boîte de dialogue de la page doit utiliser la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur MSGRESULT de la boîte de \_ dialogue, et la procédure de boîte de dialogue doit retourner **true**.</span><span class="sxs-lookup"><span data-stu-id="c1fea-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1fea-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1fea-123">Requirements</span></span>



| <span data-ttu-id="c1fea-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1fea-124">Requirement</span></span> | <span data-ttu-id="c1fea-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1fea-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fea-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1fea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c1fea-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1fea-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c1fea-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1fea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c1fea-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1fea-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c1fea-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1fea-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1fea-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1fea-131"><dt>Prsht.h</dt></span></span> </dl> |



 

