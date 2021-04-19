---
description: Appareils mobiles Windows prend en charge les propriétés de messagerie suivantes.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Propriétés de l’e-mail (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539704"
---
# <a name="email-properties"></a><span data-ttu-id="64af7-103">Propriétés de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="64af7-103">Email Properties</span></span>

<span data-ttu-id="64af7-104">Appareils mobiles Windows prend en charge les propriétés de messagerie suivantes.</span><span class="sxs-lookup"><span data-stu-id="64af7-104">Windows Portable Devices supports the following email properties.</span></span>



| <span data-ttu-id="64af7-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="64af7-105">Property</span></span>                         | <span data-ttu-id="64af7-106">VarType</span><span class="sxs-lookup"><span data-stu-id="64af7-106">VarType</span></span>        | <span data-ttu-id="64af7-107">Description</span><span class="sxs-lookup"><span data-stu-id="64af7-107">Description</span></span>                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64af7-108">**\_ \_ ligne CCI d’e-mail wpd \_**</span><span class="sxs-lookup"><span data-stu-id="64af7-108">**WPD\_EMAIL\_BCC\_LINE**</span></span>        | <span data-ttu-id="64af7-109">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="64af7-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="64af7-110">Destinataires CCI du message électronique.</span><span class="sxs-lookup"><span data-stu-id="64af7-110">The BCC recipients of the e-mail message.</span></span> <span data-ttu-id="64af7-111">Les destinataires CCI reçoivent une copie du message, mais leurs noms ne sont pas affichés en tant que destinataires.</span><span class="sxs-lookup"><span data-stu-id="64af7-111">BCC recipients receive a copy of the e-mail, but their names are not displayed as recipients.</span></span>   |
| <span data-ttu-id="64af7-112">**\_ \_ ligne CC de l’e-mail wpd \_**</span><span class="sxs-lookup"><span data-stu-id="64af7-112">**WPD\_EMAIL\_CC\_LINE**</span></span>         | <span data-ttu-id="64af7-113">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="64af7-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="64af7-114">Destinataires CC du message électronique.</span><span class="sxs-lookup"><span data-stu-id="64af7-114">The CC recipients of the e-mail message.</span></span> <span data-ttu-id="64af7-115">Les destinataires CC reçoivent une copie du message électronique et leurs noms sont affichés en tant que destinataires.</span><span class="sxs-lookup"><span data-stu-id="64af7-115">CC recipients receive a copy of the e-mail message, and their names are displayed as recipients.</span></span> |
| <span data-ttu-id="64af7-116">**l' \_ E-mail wpd \_ contient des \_ pièces jointes**</span><span class="sxs-lookup"><span data-stu-id="64af7-116">**WPD\_EMAIL\_HAS\_ATTACHMENTS**</span></span> | <span data-ttu-id="64af7-117">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="64af7-117">**VT\_BOOL**</span></span>   | <span data-ttu-id="64af7-118">Valeur booléenne qui spécifie si ce message électronique contient des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="64af7-118">A Boolean value that specifies whether this e-mail message has attachments.</span></span>                                                               |
| <span data-ttu-id="64af7-119">**l' \_ E-mail wpd \_ a \_ été \_ lu**</span><span class="sxs-lookup"><span data-stu-id="64af7-119">**WPD\_EMAIL\_HAS\_BEEN\_READ**</span></span>  | <span data-ttu-id="64af7-120">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="64af7-120">**VT\_BOOL**</span></span>   | <span data-ttu-id="64af7-121">Valeur booléenne qui spécifie si ce message électronique a été lu.</span><span class="sxs-lookup"><span data-stu-id="64af7-121">A Boolean value that specifies whether this e-mail message has been read.</span></span>                                                                 |
| <span data-ttu-id="64af7-122">**heure de réception de l' \_ E-mail wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64af7-122">**WPD\_EMAIL\_RECEIVED\_TIME**</span></span>   | <span data-ttu-id="64af7-123">**\_Date VT**</span><span class="sxs-lookup"><span data-stu-id="64af7-123">**VT\_DATE**</span></span>   | <span data-ttu-id="64af7-124">Valeur qui spécifie à quel moment le message électronique a été reçu.</span><span class="sxs-lookup"><span data-stu-id="64af7-124">A value that specifies when the e-mail message was received.</span></span>                                                                              |
| <span data-ttu-id="64af7-125">**adresse d’expéditeur de l' \_ E-mail wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64af7-125">**WPD\_EMAIL\_SENDER\_ADDRESS**</span></span>  | <span data-ttu-id="64af7-126">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="64af7-126">**VT\_LPWSTR**</span></span> | <span data-ttu-id="64af7-127">Adresse électronique de l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="64af7-127">The e-mail address of the sender.</span></span>                                                                                                         |
| <span data-ttu-id="64af7-128">**\_E-mail wpd \_ à la \_ ligne**</span><span class="sxs-lookup"><span data-stu-id="64af7-128">**WPD\_EMAIL\_TO\_LINE**</span></span>         | <span data-ttu-id="64af7-129">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="64af7-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="64af7-130">Destinataires principaux du message électronique.</span><span class="sxs-lookup"><span data-stu-id="64af7-130">The main recipients of the e-mail message.</span></span>                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="64af7-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64af7-131">Requirements</span></span>



| <span data-ttu-id="64af7-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64af7-132">Requirement</span></span> | <span data-ttu-id="64af7-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="64af7-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="64af7-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="64af7-134">Header</span></span><br/> | <dl> <span data-ttu-id="64af7-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="64af7-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64af7-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64af7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64af7-137">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="64af7-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




