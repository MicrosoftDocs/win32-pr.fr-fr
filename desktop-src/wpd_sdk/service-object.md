---
description: Objet de service
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Objet de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868670"
---
# <a name="service-object"></a><span data-ttu-id="3abec-103">Objet de service</span><span class="sxs-lookup"><span data-stu-id="3abec-103">Service Object</span></span>

<span data-ttu-id="3abec-104">L’objet de service doit prendre en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3abec-104">The service object must support the following properties.</span></span>



| <span data-ttu-id="3abec-105">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="3abec-105">Property Name</span></span>                                                                                                                      | <span data-ttu-id="3abec-106">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="3abec-106">Required or Optional</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3abec-107">[\_ID d’objet wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abec-107">[WPD\_OBJECT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                         | <span data-ttu-id="3abec-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3abec-108">Required.</span></span> <span data-ttu-id="3abec-109">.</span><span class="sxs-lookup"><span data-stu-id="3abec-109">.</span></span>                                                                           |
| <span data-ttu-id="3abec-110">[\_ \_ ID parent de l’objet wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abec-110">[WPD\_OBJECT\_PARENT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                   | <span data-ttu-id="3abec-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3abec-111">Required.</span></span>                                                                             |
| <span data-ttu-id="3abec-112">[nom de l' \_ objet wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abec-112">[WPD\_OBJECT\_NAME](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                   | <span data-ttu-id="3abec-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3abec-113">Required.</span></span>                                                                             |
| <span data-ttu-id="3abec-114">[\_ \_ \_ ID unique persistant de l’objet wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abec-114">[WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span> | <span data-ttu-id="3abec-115">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3abec-115">Required.</span></span>                                                                             |
| <span data-ttu-id="3abec-116">[WPD, \_ objet \_ ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abec-116">[WPD\_OBJECT\_ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="3abec-117">Obligatoire si l’objet de service ne doit pas être présenté à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3abec-117">Required if the service object should not be shown to the user.</span></span>                       |
| <span data-ttu-id="3abec-118">[WPD, \_ objet \_ ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abec-118">[WPD\_OBJECT\_ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="3abec-119">Obligatoire si l’objet est un objet système (par exemple, il représente un fichier système).</span><span class="sxs-lookup"><span data-stu-id="3abec-119">Required if the object is a system object (for example, it represents a system file).</span></span> |
| <span data-ttu-id="3abec-120">[\_catégorie d' \_ objet \_ fonctionnel wpd](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abec-120">[WPD\_FUNCTIONAL\_OBJECT\_CATEGORY](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>     | <span data-ttu-id="3abec-121">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3abec-121">Required.</span></span> <span data-ttu-id="3abec-122">Cela représente le type de service de l’appareil, tel que les contacts du SERVICE.</span><span class="sxs-lookup"><span data-stu-id="3abec-122">This represents the Device Service type, such as SERVICE Contacts.</span></span>          |
| <span data-ttu-id="3abec-123">[\_version du service wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abec-123">[WPD\_SERVICE\_VERSION](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="3abec-124">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3abec-124">Required.</span></span>                                                                             |
| <span data-ttu-id="3abec-125">[\_type de stockage wpd \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abec-125">[WPD\_STORAGE\_TYPE](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                | <span data-ttu-id="3abec-126">Obligatoire si le service est utilisé pour stocker des objets.</span><span class="sxs-lookup"><span data-stu-id="3abec-126">Required if the service is used to store objects.</span></span>                                     |
| <span data-ttu-id="3abec-127">[\_capacité de stockage wpd \_](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abec-127">[WPD\_STORAGE\_CAPACITY](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span></span>                                    | <span data-ttu-id="3abec-128">Obligatoire si le service est utilisé pour stocker des objets.</span><span class="sxs-lookup"><span data-stu-id="3abec-128">Required if the service is used to store objects.</span></span>                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="3abec-129">Ressources standard</span><span class="sxs-lookup"><span data-stu-id="3abec-129">Typical Resources</span></span>

<span data-ttu-id="3abec-130">Ces objets n’hébergent généralement pas de ressources.</span><span class="sxs-lookup"><span data-stu-id="3abec-130">These objects typically do not host resources.</span></span>

## <a name="typical-formats"></a><span data-ttu-id="3abec-131">Formats standard</span><span class="sxs-lookup"><span data-stu-id="3abec-131">Typical Formats</span></span>

<span data-ttu-id="3abec-132">La liste suivante identifie les formats typiques utilisés par l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="3abec-132">The following list identifies typical formats used by the Service object.</span></span> <span data-ttu-id="3abec-133">Toutefois, cet objet n’est pas limité à ces formats.</span><span class="sxs-lookup"><span data-stu-id="3abec-133">However, this object is not limited to these formats.</span></span>

-   <span data-ttu-id="3abec-134">\_format d’objet wpd \_ \_ non spécifié</span><span class="sxs-lookup"><span data-stu-id="3abec-134">WPD\_OBJECT\_FORMAT\_UNSPECIFIED</span></span>

## <a name="related-topics"></a><span data-ttu-id="3abec-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3abec-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3abec-136">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="3abec-136">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 
