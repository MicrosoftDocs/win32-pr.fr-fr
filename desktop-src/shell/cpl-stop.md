---
description: Envoyé à la fonction CPlApplet d’une application du panneau de configuration lorsque l’application de contrôle du panneau de configuration se ferme. L’application de contrôle envoie le message une fois pour chaque boîte de dialogue que l’application prend en charge.
title: Message CPL_STOP (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972042"
---
# <a name="cpl_stop-message"></a><span data-ttu-id="2c82f-104">\_Message d’arrêt cpl</span><span class="sxs-lookup"><span data-stu-id="2c82f-104">CPL\_STOP message</span></span>

<span data-ttu-id="2c82f-105">Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration lorsque l’application de contrôle du panneau de configuration se ferme.</span><span class="sxs-lookup"><span data-stu-id="2c82f-105">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the controlling application of the Control Panel closes.</span></span> <span data-ttu-id="2c82f-106">L’application de contrôle envoie le message une fois pour chaque boîte de dialogue que l’application prend en charge.</span><span class="sxs-lookup"><span data-stu-id="2c82f-106">The controlling application sends the message once for each dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c82f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c82f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c82f-108">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="2c82f-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="2c82f-109">Numéro de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2c82f-109">The dialog box number.</span></span>

</dd> <dt>

<span data-ttu-id="2c82f-110">*lData*</span><span class="sxs-lookup"><span data-stu-id="2c82f-110">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="2c82f-111">Valeur que l’application du panneau de configuration a chargée dans le membre **lpData** de la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2c82f-111">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="2c82f-112">L’application charge le membre **lpData** en réponse au message [**Cpl \_ inquire**](cpl-inquire.md) ou [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md) .</span><span class="sxs-lookup"><span data-stu-id="2c82f-112">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c82f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c82f-113">Return value</span></span>

<span data-ttu-id="2c82f-114">Si la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite ce message avec succès, elle doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="2c82f-114">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c82f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2c82f-115">Remarks</span></span>

<span data-ttu-id="2c82f-116">En réponse à ce message, une application du panneau de configuration doit effectuer un nettoyage pour la boîte de dialogue donnée.</span><span class="sxs-lookup"><span data-stu-id="2c82f-116">In response to this message, a Control Panel application must perform cleanup for the given dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c82f-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2c82f-117">Requirements</span></span>



| <span data-ttu-id="2c82f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c82f-118">Requirement</span></span> | <span data-ttu-id="2c82f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c82f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2c82f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c82f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c82f-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c82f-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2c82f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c82f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c82f-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c82f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2c82f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c82f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c82f-125"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c82f-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c82f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c82f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c82f-127">**fermeture de CPL \_**</span><span class="sxs-lookup"><span data-stu-id="2c82f-127">**CPL\_EXIT**</span></span>](cpl-exit.md)
</dt> <dt>

[<span data-ttu-id="2c82f-128">**CPL \_ GETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="2c82f-128">**CPL\_GETCOUNT**</span></span>](cpl-getcount.md)
</dt> </dl>

 

 
