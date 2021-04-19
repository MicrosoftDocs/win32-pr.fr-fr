---
description: 'Pour Windows 7, Windows Mobile Devices prend en charge les attributs suivants pour les événements d’un service d’appareil. Ces attributs sont retournés par la méthode IPortableDeviceServiceCapabilities :: GetEventAttributes.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Attributs d’événement (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532492"
---
# <a name="event-attributes-portabledeviceh"></a><span data-ttu-id="0be50-104">Attributs d’événement (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="0be50-104">Event Attributes (PortableDevice.h)</span></span>

<span data-ttu-id="0be50-105">Pour Windows 7, Windows Mobile Devices prend en charge les attributs suivants pour les événements d’un service d’appareil.</span><span class="sxs-lookup"><span data-stu-id="0be50-105">For Windows 7, Windows Portable Devices supports the following attributes for events of a device service.</span></span> <span data-ttu-id="0be50-106">Ces attributs sont retournés par la méthode [**IPortableDeviceServiceCapabilities :: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .</span><span class="sxs-lookup"><span data-stu-id="0be50-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method.</span></span>




| <span data-ttu-id="0be50-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="0be50-107">Attribute</span></span>                             | <span data-ttu-id="0be50-108">VarType</span><span class="sxs-lookup"><span data-stu-id="0be50-108">VarType</span></span>         | <span data-ttu-id="0be50-109">Description</span><span class="sxs-lookup"><span data-stu-id="0be50-109">Description</span></span>                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0be50-110">**\_nom d' \_ attribut d’événement wpd \_**</span><span class="sxs-lookup"><span data-stu-id="0be50-110">**WPD\_EVENT\_ATTRIBUTE\_NAME**</span></span>       | <span data-ttu-id="0be50-111">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="0be50-111">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="0be50-112">Chaîne qui spécifie le nom convivial du script de l’événement.</span><span class="sxs-lookup"><span data-stu-id="0be50-112">A string that specifies the script-friendly name of the event.</span></span> <span data-ttu-id="0be50-113">Les caractères valides sont alphanumériques \[ a-zA-z0-9 \] et' \_ '.</span><span class="sxs-lookup"><span data-stu-id="0be50-113">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="0be50-114">**\_Options des \_ attributs d’événement wpd \_**</span><span class="sxs-lookup"><span data-stu-id="0be50-114">**WPD\_EVENT\_ATTRIBUTE\_OPTIONS**</span></span>    | <span data-ttu-id="0be50-115">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="0be50-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="0be50-116">[**IPortableDeviceValues**](iportabledevicevalues.md) qui contient les options d’événement.</span><span class="sxs-lookup"><span data-stu-id="0be50-116">An [**IPortableDeviceValues**](iportabledevicevalues.md) that contains the event options.</span></span>                               |
| <span data-ttu-id="0be50-117">**\_paramètres d' \_ attribut d’événement wpd \_**</span><span class="sxs-lookup"><span data-stu-id="0be50-117">**WPD\_EVENT\_ATTRIBUTE\_PARAMETERS**</span></span> | <span data-ttu-id="0be50-118">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="0be50-118">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="0be50-119">[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) qui contient les paramètres d’événement.</span><span class="sxs-lookup"><span data-stu-id="0be50-119">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) that contains the event parameters.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="0be50-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0be50-120">Requirements</span></span>



| <span data-ttu-id="0be50-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0be50-121">Requirement</span></span> | <span data-ttu-id="0be50-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0be50-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0be50-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0be50-123">Header</span></span><br/> | <dl> <span data-ttu-id="0be50-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be50-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0be50-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0be50-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be50-126">**Propriétés et attributs**</span><span class="sxs-lookup"><span data-stu-id="0be50-126">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




