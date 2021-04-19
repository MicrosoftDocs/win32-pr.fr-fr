---
description: L’événement DVDNotify avertit une application de nombreux événements DVD et instructions sur le disque.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544098"
---
# <a name="dvdnotify"></a><span data-ttu-id="ba0f1-103">DVDNotify</span><span class="sxs-lookup"><span data-stu-id="ba0f1-103">DVDNotify</span></span>

> [!Note]  
> <span data-ttu-id="ba0f1-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ba0f1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ba0f1-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ba0f1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ba0f1-106">L' `DVDNotify` événement avertit une application de nombreux événements DVD et instructions sur le disque.</span><span class="sxs-lookup"><span data-stu-id="ba0f1-106">The `DVDNotify` event notifies an application of many different DVD events and disc instructions.</span></span>

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a><span data-ttu-id="ba0f1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba0f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba0f1-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span><span class="sxs-lookup"><span data-stu-id="ba0f1-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span></span>
</dt> <dd>

<span data-ttu-id="ba0f1-109">Spécifie le code de notification d’événement DVD.</span><span class="sxs-lookup"><span data-stu-id="ba0f1-109">Specifies the DVD event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="ba0f1-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span><span class="sxs-lookup"><span data-stu-id="ba0f1-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span></span>
</dt> <dd>

<span data-ttu-id="ba0f1-111">Peut contenir des informations supplémentaires relatives à l’événement.</span><span class="sxs-lookup"><span data-stu-id="ba0f1-111">Can contain additional information related to the event.</span></span>

</dd> <dt>

<span data-ttu-id="ba0f1-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span><span class="sxs-lookup"><span data-stu-id="ba0f1-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span></span>
</dt> <dd>

<span data-ttu-id="ba0f1-113">Peut contenir des informations supplémentaires relatives à l’événement.</span><span class="sxs-lookup"><span data-stu-id="ba0f1-113">Can contain additional information related to the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba0f1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ba0f1-114">Remarks</span></span>

<span data-ttu-id="ba0f1-115">Les [codes de notification d’événement DVD](dvd-notification-codes.md) donnent une explication complète de tous les codes de notification d’événements DVD et de leurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="ba0f1-115">[DVD Event Notification Codes](dvd-notification-codes.md) gives a full explanation of all DVD event notification codes and their parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0f1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba0f1-116">Requirements</span></span>



| <span data-ttu-id="ba0f1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba0f1-117">Requirement</span></span> | <span data-ttu-id="ba0f1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba0f1-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0f1-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba0f1-119">Header</span></span><br/> | <dl> <span data-ttu-id="ba0f1-120"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba0f1-120"><dt>Segment.h</dt></span></span> </dl> |



 

 




