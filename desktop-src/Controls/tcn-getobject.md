---
title: TCN_GETOBJECT le code de notification (commctrl. h)
description: Envoyé par un contrôle onglet lorsqu’il a le \_ \_ style étendu TCS ex REGISTERDROP et qu’un objet est glissé sur un élément d’onglet dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- Contrôles Windows de code de notification TCN_GETOBJECT
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510114"
---
# <a name="tcn_getobject-notification-code"></a><span data-ttu-id="a11be-105">\_Code de notification TCN GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="a11be-105">TCN\_GETOBJECT notification code</span></span>

<span data-ttu-id="a11be-106">Envoyé par un contrôle onglet lorsqu’il a le style étendu [**TCS \_ ex \_ REGISTERDROP**](tab-control-extended-styles.md) et qu’un objet est glissé sur un élément d’onglet dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="a11be-106">Sent by a tab control when it has the [**TCS\_EX\_REGISTERDROP**](tab-control-extended-styles.md) extended style and an object is dragged over a tab item in the control.</span></span> <span data-ttu-id="a11be-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a11be-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a11be-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a11be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a11be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a11be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a11be-110">Pointeur vers une structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) qui contient des informations sur l’élément d’onglet sur lequel l’objet est glissé et reçoit les données retournées par l’application en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="a11be-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the tab item the object is dragged over and receives data the application returns in response to this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a11be-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a11be-111">Return value</span></span>

<span data-ttu-id="a11be-112">L’application traitant ce code de notification doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="a11be-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a11be-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a11be-113">Requirements</span></span>



| <span data-ttu-id="a11be-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a11be-114">Requirement</span></span> | <span data-ttu-id="a11be-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a11be-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a11be-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a11be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a11be-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a11be-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a11be-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a11be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a11be-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a11be-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a11be-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a11be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a11be-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a11be-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





