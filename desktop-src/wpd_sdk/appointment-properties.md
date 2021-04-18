---
description: Appareils mobiles Windows prend en charge les propriétés de rendez-vous suivantes.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Propriétés du rendez-vous (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 542029f9eb698c8093c43cbb8ee309b3d1f9da6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526416"
---
# <a name="appointment-properties"></a><span data-ttu-id="a3440-103">Propriétés du rendez-vous</span><span class="sxs-lookup"><span data-stu-id="a3440-103">Appointment Properties</span></span>

<span data-ttu-id="a3440-104">Appareils mobiles Windows prend en charge les propriétés de rendez-vous suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3440-104">Windows Portable Devices supports the following appointment properties.</span></span>



| <span data-ttu-id="a3440-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="a3440-105">Property</span></span>                                   | <span data-ttu-id="a3440-106">VarType</span><span class="sxs-lookup"><span data-stu-id="a3440-106">VarType</span></span>        | <span data-ttu-id="a3440-107">Description</span><span class="sxs-lookup"><span data-stu-id="a3440-107">Description</span></span>                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a3440-108">**participants à un \_ rendez-vous \_ accepté par wpd \_**</span><span class="sxs-lookup"><span data-stu-id="a3440-108">**WPD\_APPOINTMENT\_ACCEPTED\_ATTENDEES**</span></span>  | <span data-ttu-id="a3440-109">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="a3440-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="a3440-110">Liste délimitée par des points-virgules des participants qui ont accepté le rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3440-110">Semicolon-delimited list of attendees who have accepted the appointment.</span></span>             |
| <span data-ttu-id="a3440-111">**\_rendez-vous \_ refusé aux \_ participants**</span><span class="sxs-lookup"><span data-stu-id="a3440-111">**WPD\_APPOINTMENT\_DECLINED\_ATTENDEES**</span></span>  | <span data-ttu-id="a3440-112">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="a3440-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="a3440-113">Liste délimitée par des points-virgules des participants ayant refusé le rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3440-113">Semicolon-delimited list of attendees who have declined the appointment.</span></span>             |
| <span data-ttu-id="a3440-114">**\_emplacement du rendez-vous wpd \_**</span><span class="sxs-lookup"><span data-stu-id="a3440-114">**WPD\_APPOINTMENT\_LOCATION**</span></span>             | <span data-ttu-id="a3440-115">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="a3440-115">VT\_LPWSTR</span></span>     | <span data-ttu-id="a3440-116">Emplacement convivial du lecteur du rendez-vous, par exemple, « bâtiment 5, salle 7 ».</span><span class="sxs-lookup"><span data-stu-id="a3440-116">A reader-friendly location of the appointment, for example, "Building 5, Room 7".</span></span>    |
| <span data-ttu-id="a3440-117">**\_ \_ participants facultatifs RENDus wpd \_**</span><span class="sxs-lookup"><span data-stu-id="a3440-117">**WPD\_APPOINTMENT\_OPTIONAL\_ATTENDEES**</span></span>  | <span data-ttu-id="a3440-118">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="a3440-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="a3440-119">Liste délimitée par des points-virgules des participants facultatifs au rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3440-119">Semicolon-delimited list of optional attendees for the appointment.</span></span>                  |
| <span data-ttu-id="a3440-120">**participants obligatoires à un \_ rendez-vous \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a3440-120">**WPD\_APPOINTMENT\_REQUIRED\_ATTENDEES**</span></span>  | <span data-ttu-id="a3440-121">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="a3440-121">**VT\_LPWSTR**</span></span> | <span data-ttu-id="a3440-122">Liste délimitée par des points-virgules des participants obligatoires au rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3440-122">Semicolon-delimited list of required attendees for the appointment.</span></span>                  |
| <span data-ttu-id="a3440-123">**\_ressources de rendez-vous wpd \_**</span><span class="sxs-lookup"><span data-stu-id="a3440-123">**WPD\_APPOINTMENT\_RESOURCES**</span></span>            | <span data-ttu-id="a3440-124">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="a3440-124">**VT\_LPWSTR**</span></span> | <span data-ttu-id="a3440-125">Liste délimitée par des points-virgules des ressources requises pour le rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3440-125">Semicolon-delimited list of resources required for the appointment.</span></span>                  |
| <span data-ttu-id="a3440-126">**\_ \_ participants provisoires au rendez-vous pour wpd \_**</span><span class="sxs-lookup"><span data-stu-id="a3440-126">**WPD\_APPOINTMENT\_TENTATIVE\_ATTENDEES**</span></span> | <span data-ttu-id="a3440-127">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="a3440-127">**VT\_LPWSTR**</span></span> | <span data-ttu-id="a3440-128">Liste délimitée par des points-virgules des participants qui ont provisoirement accepté le rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3440-128">Semicolon-delimited list of attendees who have tentatively accepted the appointment.</span></span> |
| <span data-ttu-id="a3440-129">**\_type de rendez-vous wpd \_**</span><span class="sxs-lookup"><span data-stu-id="a3440-129">**WPD\_APPOINTMENT\_TYPE**</span></span>                 | <span data-ttu-id="a3440-130">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="a3440-130">**VT\_LPWSTR**</span></span> | <span data-ttu-id="a3440-131">Type de rendez-vous, par exemple « personnel », « professionnel », etc.</span><span class="sxs-lookup"><span data-stu-id="a3440-131">The type of appointment, for example,"Personal", "Business", and so on.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="a3440-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3440-132">Requirements</span></span>



| <span data-ttu-id="a3440-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3440-133">Requirement</span></span> | <span data-ttu-id="a3440-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3440-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3440-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3440-135">Header</span></span><br/> | <dl> <span data-ttu-id="a3440-136"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3440-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3440-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3440-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3440-138">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="a3440-138">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




