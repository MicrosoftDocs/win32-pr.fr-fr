---
description: CPL_NEWINQUIRE message-envoyé à la fonction CPlApplet d’une application du panneau de configuration pour demander des informations sur une boîte de dialogue que l’application prend en charge.
title: Message CPL_NEWINQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104437"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="f5f50-103">\_Message NEWINQUIRE cpl</span><span class="sxs-lookup"><span data-stu-id="f5f50-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="f5f50-104">Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration pour demander des informations sur une boîte de dialogue que l’application prend en charge.</span><span class="sxs-lookup"><span data-stu-id="f5f50-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5f50-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5f50-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5f50-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="f5f50-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f50-107">Numéro de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f5f50-107">The dialog box number.</span></span> <span data-ttu-id="f5f50-108">Ce nombre doit être compris entre zéro et une valeur inférieure à la valeur renvoyée en réponse au message [**Cpl \_ GETCOUNT**](cpl-getcount.md) (CPL \_ GetCount – 1).</span><span class="sxs-lookup"><span data-stu-id="f5f50-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="f5f50-109">*lpncpli*</span><span class="sxs-lookup"><span data-stu-id="f5f50-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f50-110">Adresse d’une structure [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f5f50-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="f5f50-111">L’application du panneau de configuration doit remplir cette structure avec des informations sur la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f5f50-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5f50-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f5f50-112">Return value</span></span>

<span data-ttu-id="f5f50-113">Si la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite ce message avec succès, elle doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="f5f50-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5f50-114">Notes </span><span class="sxs-lookup"><span data-stu-id="f5f50-114">Remarks</span></span>

<span data-ttu-id="f5f50-115">Pour de meilleures performances, la plupart des applications doivent ignorer **Cpl \_ NEWINQUIRE** et traiter le message de [**\_ recherche de cpl**](cpl-inquire.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="f5f50-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="f5f50-116">Le panneau de configuration envoie le message **\_ NEWINQUIRE Cpl** une fois pour chaque boîte de dialogue prise en charge par votre application.</span><span class="sxs-lookup"><span data-stu-id="f5f50-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="f5f50-117">Le panneau de configuration envoie également un message de [**\_ recherche de cpl**](cpl-inquire.md) pour chaque boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f5f50-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="f5f50-118">Ces messages sont envoyés immédiatement après le message [**Cpl \_ GETCOUNT**](cpl-getcount.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f50-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="f5f50-119">Toutefois, le système ne garantit **pas l’ordre \_** dans lequel les messages **\_ NEWINQUIRE et Cpl** sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="f5f50-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="f5f50-120">Vous pouvez procéder à l’initialisation de la boîte de dialogue lorsque vous recevez l' [**\_ enquête Cpl**](cpl-inquire.md).</span><span class="sxs-lookup"><span data-stu-id="f5f50-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="f5f50-121">Si vous devez allouer de la mémoire, faites-le en réponse au message d' [**\_ initialisation de cpl**](cpl-init.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f50-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="f5f50-122">[**Cpl \_ L’interrogation**](cpl-inquire.md) est le message par défaut.</span><span class="sxs-lookup"><span data-stu-id="f5f50-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="f5f50-123">Cela est dû au fait que **Cpl \_ NEWINQUIRE** retourne des informations dans un format que le système ne peut pas mettre en cache.</span><span class="sxs-lookup"><span data-stu-id="f5f50-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="f5f50-124">Par conséquent, les applications qui traitent le tableau de bord **\_ NEWINQUIRE** doivent être chargées chaque fois que le panneau de configuration a besoin des informations, ce qui réduit considérablement les performances.</span><span class="sxs-lookup"><span data-stu-id="f5f50-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="f5f50-125">Les seules applications qui doivent utiliser **Cpl \_ NEWINQUIRE** sont celles qui ont besoin de modifier leur icône ou d’afficher des chaînes en fonction de l’état de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f5f50-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="f5f50-126">Dans ce cas, votre gestionnaire de [**\_ recherche de cpl**](cpl-inquire.md) doit spécifier la \_ \_ valeur res dynamique CPL pour les membres **idIcon**, **idName** ou **idInfo** de la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , plutôt que de spécifier un identificateur de ressource valide.</span><span class="sxs-lookup"><span data-stu-id="f5f50-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="f5f50-127">Cela amène le panneau de configuration à envoyer le message **\_ NEWINQUIRE Cpl** chaque fois qu’il a besoin de l’icône et des chaînes d’affichage, ce qui vous permet de spécifier des informations en fonction de l’état actuel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f5f50-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="f5f50-128">Bien entendu, cela est beaucoup plus lent que d’utiliser les informations mises en cache.</span><span class="sxs-lookup"><span data-stu-id="f5f50-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f50-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5f50-129">Requirements</span></span>



| <span data-ttu-id="f5f50-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5f50-130">Requirement</span></span> | <span data-ttu-id="f5f50-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f50-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f5f50-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5f50-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f50-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f5f50-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5f50-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f50-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5f50-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f5f50-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5f50-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5f50-137"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5f50-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
