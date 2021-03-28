---
description: Envoyé à la fonction CPlApplet d’une application du panneau de configuration lorsque l’utilisateur double-clique sur l’icône d’une boîte de dialogue prise en charge par l’application.
title: Message CPL_DBLCLK (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991085"
---
# <a name="cpl_dblclk-message"></a><span data-ttu-id="715a1-103">\_Message DBLCLK cpl</span><span class="sxs-lookup"><span data-stu-id="715a1-103">CPL\_DBLCLK message</span></span>

<span data-ttu-id="715a1-104">Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration lorsque l’utilisateur double-clique sur l’icône d’une boîte de dialogue prise en charge par l’application.</span><span class="sxs-lookup"><span data-stu-id="715a1-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the user double-clicks the icon of a dialog box supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="715a1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="715a1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="715a1-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="715a1-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="715a1-107">Numéro de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="715a1-107">The dialog box number.</span></span> <span data-ttu-id="715a1-108">Ce nombre doit être compris entre zéro et une valeur inférieure à la valeur renvoyée en réponse au message [**Cpl \_ GETCOUNT**](cpl-getcount.md) (CPL \_ GetCount – 1).</span><span class="sxs-lookup"><span data-stu-id="715a1-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="715a1-109">*lData*</span><span class="sxs-lookup"><span data-stu-id="715a1-109">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="715a1-110">Valeur que l’application du panneau de configuration a chargée dans le membre **lpData** de la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="715a1-110">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="715a1-111">L’application charge le membre **lpData** en réponse au message [**Cpl \_ inquire**](cpl-inquire.md) ou [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md) .</span><span class="sxs-lookup"><span data-stu-id="715a1-111">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="715a1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="715a1-112">Return value</span></span>

<span data-ttu-id="715a1-113">Si la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite ce message avec succès, la valeur de retour est zéro ; dans le cas contraire, il est différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="715a1-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, the return value is zero; otherwise, it is nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="715a1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="715a1-114">Remarks</span></span>

<span data-ttu-id="715a1-115">En réponse à ce message, une application du panneau de configuration doit afficher la boîte de dialogue correspondante.</span><span class="sxs-lookup"><span data-stu-id="715a1-115">In response to this message, a Control Panel application must display the corresponding dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="715a1-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="715a1-116">Requirements</span></span>



| <span data-ttu-id="715a1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="715a1-117">Requirement</span></span> | <span data-ttu-id="715a1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="715a1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="715a1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="715a1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="715a1-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="715a1-120">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="715a1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="715a1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="715a1-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="715a1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="715a1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="715a1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="715a1-124"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="715a1-124"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="715a1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="715a1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="715a1-126">**CPL \_ Sélectionner**</span><span class="sxs-lookup"><span data-stu-id="715a1-126">**CPL\_SELECT**</span></span>](cpl-select.md)
</dt> </dl>

 

 
