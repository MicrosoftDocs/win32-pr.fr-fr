---
description: L’interface de l’appareil peut être décrite par une valeur GUID. Les appareils mobiles Windows définissent l’interface de périphérique suivante.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: GUID de l’interface de l’appareil (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c2f97e050f839a268048aaaabac46b9e7698ee9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542402"
---
# <a name="device-interface-guids"></a><span data-ttu-id="25f20-104">GUID de l’interface de l’appareil</span><span class="sxs-lookup"><span data-stu-id="25f20-104">Device Interface GUIDs</span></span>

<span data-ttu-id="25f20-105">L’interface de l’appareil peut être décrite par une valeur **GUID** .</span><span class="sxs-lookup"><span data-stu-id="25f20-105">The device interface can be described by a **GUID** value.</span></span> <span data-ttu-id="25f20-106">Les appareils mobiles Windows définissent l’interface de périphérique suivante.</span><span class="sxs-lookup"><span data-stu-id="25f20-106">Windows Portable Devices defines the following device interface.</span></span>



| <span data-ttu-id="25f20-107">Constante</span><span class="sxs-lookup"><span data-stu-id="25f20-107">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="25f20-108">Description</span><span class="sxs-lookup"><span data-stu-id="25f20-108">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <span data-ttu-id="25f20-109"><dt>**GUID \_ DEVINTERFACE \_ wpd**</dt></span><span class="sxs-lookup"><span data-stu-id="25f20-109"><dt>**GUID\_DEVINTERFACE\_WPD**</dt></span></span> </dl>                          | <span data-ttu-id="25f20-110">Identifie les périphériques qui s’affichent dans une énumération WPD normale.</span><span class="sxs-lookup"><span data-stu-id="25f20-110">Identifies devices that appear in a normal WPD enumeration.</span></span> <span data-ttu-id="25f20-111">Tout appareil qui inscrit ce GUID d’interface est énuméré quand une application appelle la méthode [**IPortableDeviceManager :: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .</span><span class="sxs-lookup"><span data-stu-id="25f20-111">Any device that registers this interface GUID will be enumerated when an application calls the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.</span></span><br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <span data-ttu-id="25f20-112"><dt>**GUID \_ DEVINTERFACE \_ wpd \_ privé**</dt></span><span class="sxs-lookup"><span data-stu-id="25f20-112"><dt>**GUID\_DEVINTERFACE\_WPD\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="25f20-113">Identifie les appareils qui n’apparaîtront pas au cours d’une énumération WPD normale.</span><span class="sxs-lookup"><span data-stu-id="25f20-113">Identifies devices that will not appear during a normal WPD enumeration.</span></span> <span data-ttu-id="25f20-114">Tout appareil qui inscrit ce GUID d’interface est énuméré uniquement quand une application appelle la méthode [**IPortableDeviceManager :: GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) .</span><span class="sxs-lookup"><span data-stu-id="25f20-114">Any device that registers this interface GUID will be enumerated only when an application calls the [**IPortableDeviceManager::GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) method.</span></span><br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <span data-ttu-id="25f20-115"><dt>**GUID \_ du \_ service DEVINTERFACE wpd \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25f20-115"><dt>**GUID\_DEVINTERFACE\_WPD\_SERVICE**</dt></span></span> </dl> | <span data-ttu-id="25f20-116">Dans Windows 7, les applications peuvent énumérer tous les services d’appareil WPD en appelant [**IPortableDeviceServiceManager :: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) et en utilisant cette classe d’interface comme GUID de type de service.</span><span class="sxs-lookup"><span data-stu-id="25f20-116">In Windows 7, applications can enumerate all WPD device services by calling [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) and using this interface class as the service-type GUID.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="25f20-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25f20-117">Requirements</span></span>



| <span data-ttu-id="25f20-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25f20-118">Requirement</span></span> | <span data-ttu-id="25f20-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="25f20-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f20-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="25f20-120">Header</span></span><br/> | <dl> <span data-ttu-id="25f20-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="25f20-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f20-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25f20-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f20-123">Guide de référence de programmation</span><span class="sxs-lookup"><span data-stu-id="25f20-123">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




