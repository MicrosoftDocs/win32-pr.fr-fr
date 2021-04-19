---
description: Appareils mobiles Windows prend en charge les propriétés d’informations courantes suivantes.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Propriétés des informations communes (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b773d8404997da20b4196c802ba12286679af683
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529925"
---
# <a name="common-information-properties"></a><span data-ttu-id="04f09-103">Propriétés des informations communes</span><span class="sxs-lookup"><span data-stu-id="04f09-103">Common Information Properties</span></span>

<span data-ttu-id="04f09-104">Appareils mobiles Windows prend en charge les propriétés d’informations courantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="04f09-104">Windows Portable Devices supports the following common information properties.</span></span>



| <span data-ttu-id="04f09-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="04f09-105">Property</span></span>                                      | <span data-ttu-id="04f09-106">VarType</span><span class="sxs-lookup"><span data-stu-id="04f09-106">VarType</span></span>        | <span data-ttu-id="04f09-107">Description</span><span class="sxs-lookup"><span data-stu-id="04f09-107">Description</span></span>                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04f09-108">**\_Notes d' \_ informations \_ communes wpd**</span><span class="sxs-lookup"><span data-stu-id="04f09-108">**WPD\_COMMON\_INFORMATION\_NOTES**</span></span>           | <span data-ttu-id="04f09-109">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="04f09-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="04f09-110">Pour les rendez-vous, les tâches et les objets similaires, cette propriété contient toutes les remarques relatives à l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="04f09-110">For appointments, tasks, and similar objects, this property contains any notes for the given object.</span></span>     |
| <span data-ttu-id="04f09-111">**\_objet d' \_ informations \_ communes wpd**</span><span class="sxs-lookup"><span data-stu-id="04f09-111">**WPD\_COMMON\_INFORMATION\_SUBJECT**</span></span>         | <span data-ttu-id="04f09-112">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="04f09-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="04f09-113">Valeur qui spécifie le champ objet de cet objet.</span><span class="sxs-lookup"><span data-stu-id="04f09-113">A value that specifies the subject field of this object.</span></span>                                                 |
| <span data-ttu-id="04f09-114">**\_ \_ \_ texte du corps d’informations communes wpd \_**</span><span class="sxs-lookup"><span data-stu-id="04f09-114">**WPD\_COMMON\_INFORMATION\_BODY\_TEXT**</span></span>      | <span data-ttu-id="04f09-115">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="04f09-115">**VT\_LPWSTR**</span></span> | <span data-ttu-id="04f09-116">Cette propriété contient le texte du corps d’un objet, en texte brut ou au format HTML.</span><span class="sxs-lookup"><span data-stu-id="04f09-116">This property contains the body text of an object, in plaintext or HTML format.</span></span>                          |
| <span data-ttu-id="04f09-117">**\_priorité des \_ informations \_ communes wpd**</span><span class="sxs-lookup"><span data-stu-id="04f09-117">**WPD\_COMMON\_INFORMATION\_PRIORITY**</span></span>        | <span data-ttu-id="04f09-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="04f09-118">**VT\_UI4**</span></span>    | <span data-ttu-id="04f09-119">Valeur qui spécifie la priorité de cet objet.</span><span class="sxs-lookup"><span data-stu-id="04f09-119">A value that specifies the priority of this object.</span></span> <span data-ttu-id="04f09-120">0 indique la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="04f09-120">0 indicates the highest priority.</span></span>                    |
| <span data-ttu-id="04f09-121">**\_date et \_ \_ heure de début des informations communes wpd \_**</span><span class="sxs-lookup"><span data-stu-id="04f09-121">**WPD\_COMMON\_INFORMATION\_START\_DATETIME**</span></span> | <span data-ttu-id="04f09-122">**\_Date VT**</span><span class="sxs-lookup"><span data-stu-id="04f09-122">**VT\_DATE**</span></span>   | <span data-ttu-id="04f09-123">Valeur qui spécifie la date/l’heure de début planifiée d’un rendez-vous, d’une tâche ou d’un objet similaire.</span><span class="sxs-lookup"><span data-stu-id="04f09-123">A value that specifies the date/time that an appointment, task, or similar object is scheduled to start.</span></span> |
| <span data-ttu-id="04f09-124">**\_date et \_ \_ heure de fin des informations communes wpd \_**</span><span class="sxs-lookup"><span data-stu-id="04f09-124">**WPD\_COMMON\_INFORMATION\_END\_DATETIME**</span></span>   | <span data-ttu-id="04f09-125">**\_Date VT**</span><span class="sxs-lookup"><span data-stu-id="04f09-125">**VT\_DATE**</span></span>   | <span data-ttu-id="04f09-126">Valeur qui spécifie la date/l’heure de fin planifiée d’un rendez-vous, d’une tâche ou d’un objet similaire.</span><span class="sxs-lookup"><span data-stu-id="04f09-126">A value that specifies the date/time that an appointment, task, or similar object is scheduled to end.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="04f09-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04f09-127">Requirements</span></span>



| <span data-ttu-id="04f09-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04f09-128">Requirement</span></span> | <span data-ttu-id="04f09-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="04f09-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="04f09-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="04f09-130">Header</span></span><br/> | <dl> <span data-ttu-id="04f09-131"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="04f09-131"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f09-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04f09-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f09-133">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="04f09-133">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




