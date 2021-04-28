---
description: CPL_INQUIRE message-envoyé à la fonction CPlApplet d’une application du panneau de configuration pour demander des informations sur une boîte de dialogue que l’application prend en charge.
title: Message CPL_INQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f9962ff94e8bf80041d7b61ecf97220d573131fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104467"
---
# <a name="cpl_inquire-message"></a><span data-ttu-id="f187f-103">\_Message de recherche cpl</span><span class="sxs-lookup"><span data-stu-id="f187f-103">CPL\_INQUIRE message</span></span>

<span data-ttu-id="f187f-104">Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration pour demander des informations sur une boîte de dialogue que l’application prend en charge.</span><span class="sxs-lookup"><span data-stu-id="f187f-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="f187f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f187f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f187f-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="f187f-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="f187f-107">Numéro de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f187f-107">The dialog box number.</span></span> <span data-ttu-id="f187f-108">Ce nombre doit être compris entre zéro et une valeur inférieure à la valeur renvoyée en réponse au message [**Cpl \_ GETCOUNT**](cpl-getcount.md) (CPL \_ GetCount – 1).</span><span class="sxs-lookup"><span data-stu-id="f187f-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="f187f-109">*lpcpli*</span><span class="sxs-lookup"><span data-stu-id="f187f-109">*lpcpli*</span></span> 
</dt> <dd>

<span data-ttu-id="f187f-110">Adresse d’une structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) .</span><span class="sxs-lookup"><span data-stu-id="f187f-110">The address of a [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure.</span></span> <span data-ttu-id="f187f-111">L’application doit remplir cette structure avec des identificateurs de ressource pour l’icône, le nom abrégé, la description et toute valeur définie par l’utilisateur associée à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f187f-111">The application must fill this structure with resource identifiers for the icon, short name, description, and any user-defined value associated with the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f187f-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f187f-112">Return value</span></span>

<span data-ttu-id="f187f-113">Si la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite ce message avec succès, elle doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="f187f-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f187f-114">Notes </span><span class="sxs-lookup"><span data-stu-id="f187f-114">Remarks</span></span>

<span data-ttu-id="f187f-115">Le panneau de configuration envoie le message de **\_ recherche Cpl** une fois pour chaque boîte de dialogue prise en charge par votre application.</span><span class="sxs-lookup"><span data-stu-id="f187f-115">The Control Panel sends the **CPL\_INQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="f187f-116">Le panneau de configuration envoie également un message [**\_ NEWINQUIRE Cpl**](cpl-newinquire.md) pour chaque boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f187f-116">The Control Panel also sends a [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message for each dialog box.</span></span> <span data-ttu-id="f187f-117">Ces messages sont envoyés immédiatement après le message [**Cpl \_ GETCOUNT**](cpl-getcount.md) .</span><span class="sxs-lookup"><span data-stu-id="f187f-117">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="f187f-118">Toutefois, le système ne garantit **pas l’ordre \_** dans lequel les messages **\_ NEWINQUIRE et Cpl** sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="f187f-118">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="f187f-119">Vous pouvez procéder à l’initialisation de la boîte de dialogue lorsque vous recevez l' **\_ enquête Cpl**.</span><span class="sxs-lookup"><span data-stu-id="f187f-119">You can perform initialization for the dialog box when you receive **CPL\_INQUIRE**.</span></span> <span data-ttu-id="f187f-120">Si vous devez allouer de la mémoire, faites-le en réponse au message d' [**\_ initialisation de cpl**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="f187f-120">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="f187f-121">Le [**message \_ NEWINQUIRE de cpl**](cpl-newinquire.md) retourne des informations dans un format que le système ne peut pas mettre en cache.</span><span class="sxs-lookup"><span data-stu-id="f187f-121">The [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="f187f-122">Pour cette raison, la plupart des fonctions [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) doivent traiter le **panneau de \_ recherche** et ignorer **Cpl \_ NEWINQUIRE**.</span><span class="sxs-lookup"><span data-stu-id="f187f-122">For this reason, most [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) functions should process **CPL\_INQUIRE** and ignore **CPL\_NEWINQUIRE**.</span></span>

<span data-ttu-id="f187f-123">Les seules applications qui doivent utiliser [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md) sont celles qui ont besoin de modifier leur icône ou d’afficher des chaînes en fonction de l’état de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f187f-123">The only applications that should use [**CPL\_NEWINQUIRE**](cpl-newinquire.md) are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="f187f-124">Dans ce cas, votre gestionnaire de **\_ recherche de cpl** doit spécifier la \_ \_ valeur res dynamique CPL pour les membres **idIcon**, **idName** ou **idInfo** de la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , plutôt que de spécifier un identificateur de ressource valide.</span><span class="sxs-lookup"><span data-stu-id="f187f-124">In this case, your **CPL\_INQUIRE** handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="f187f-125">Cela amène le panneau de configuration à envoyer le message **\_ NEWINQUIRE Cpl** chaque fois qu’il a besoin de l’icône et des chaînes d’affichage, ce qui vous permet de spécifier des informations en fonction de l’état actuel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f187f-125">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="f187f-126">Cela est beaucoup plus lent que d’utiliser les informations mises en cache.</span><span class="sxs-lookup"><span data-stu-id="f187f-126">This is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f187f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f187f-127">Requirements</span></span>



| <span data-ttu-id="f187f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f187f-128">Requirement</span></span> | <span data-ttu-id="f187f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f187f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f187f-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f187f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f187f-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f187f-131">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f187f-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f187f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f187f-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f187f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f187f-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="f187f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f187f-135"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f187f-135"><dt>Cpl.h</dt></span></span> </dl> |



 

 
