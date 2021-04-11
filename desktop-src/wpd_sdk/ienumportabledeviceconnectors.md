---
description: Prend en charge l’énumération des interfaces IPortableDeviceConnector, représentant les appareils MTP/Bluetooth qui ont été couplés avec le PC.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Interface IEnumPortableDeviceConnectors (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202909"
---
# <a name="ienumportabledeviceconnectors-interface"></a><span data-ttu-id="87b87-103">Interface IEnumPortableDeviceConnectors</span><span class="sxs-lookup"><span data-stu-id="87b87-103">IEnumPortableDeviceConnectors interface</span></span>

<span data-ttu-id="87b87-104">L’interface **IEnumPortableDeviceConnectors** prend en charge l’énumération des interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , représentant les appareils MTP/Bluetooth qui ont été couplés avec le PC.</span><span class="sxs-lookup"><span data-stu-id="87b87-104">The **IEnumPortableDeviceConnectors** interface supports the enumeration of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces, representing MTP/Bluetooth devices that were paired with the PC.</span></span> <span data-ttu-id="87b87-105">Notez que cela permet de récupérer tous les appareils précédemment couplés, y compris ceux qui sont associés mais déconnectés.</span><span class="sxs-lookup"><span data-stu-id="87b87-105">Note that this will retrieve all previously-paired devices, including devices that are paired but disconnected.</span></span> <span data-ttu-id="87b87-106">Pour déterminer si un appareil est toujours connecté, interrogez la propriété **DEVPKEY \_ MTPBTH \_ IsConnected** de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="87b87-106">To determine if a device is still connected, query the **DEVPKEY\_MTPBTH\_IsConnected** property for that device.</span></span>

## <a name="members"></a><span data-ttu-id="87b87-107">Membres</span><span class="sxs-lookup"><span data-stu-id="87b87-107">Members</span></span>

<span data-ttu-id="87b87-108">L’interface **IEnumPortableDeviceConnectors** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="87b87-108">The **IEnumPortableDeviceConnectors** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="87b87-109">**IEnumPortableDeviceConnectors** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="87b87-109">**IEnumPortableDeviceConnectors** also has these types of members:</span></span>

-   [<span data-ttu-id="87b87-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="87b87-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="87b87-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="87b87-111">Methods</span></span>

<span data-ttu-id="87b87-112">L’interface **IEnumPortableDeviceConnectors** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="87b87-112">The **IEnumPortableDeviceConnectors** interface has these methods.</span></span>



| <span data-ttu-id="87b87-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="87b87-113">Method</span></span>                                               | <span data-ttu-id="87b87-114">Description</span><span class="sxs-lookup"><span data-stu-id="87b87-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87b87-115">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="87b87-115">**Clone**</span></span>](ienumportabledeviceconnectors-clone.md) | <span data-ttu-id="87b87-116">Crée une copie de l’interface **IEnumPortableDeviceConnectors** actuelle.</span><span class="sxs-lookup"><span data-stu-id="87b87-116">Creates a copy of the current **IEnumPortableDeviceConnectors** interface.</span></span><br/>                                                       |
| [<span data-ttu-id="87b87-117">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="87b87-117">**Next**</span></span>](ienumportabledeviceconnectors-next.md)   | <span data-ttu-id="87b87-118">Récupère le suivant d’un ou plusieurs objets [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="87b87-118">Retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="87b87-119">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="87b87-119">**Reset**</span></span>](ienumportabledeviceconnectors-reset.md) | <span data-ttu-id="87b87-120">Réinitialise la séquence d'énumération au début.</span><span class="sxs-lookup"><span data-stu-id="87b87-120">Resets the enumeration sequence to the beginning.</span></span><br/>                                                                                |
| [<span data-ttu-id="87b87-121">**Saut**</span><span class="sxs-lookup"><span data-stu-id="87b87-121">**Skip**</span></span>](ienumportabledeviceconnectors-skip.md)   | <span data-ttu-id="87b87-122">Ignore le nombre spécifié d’appareils dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="87b87-122">Skips the specified number of devices in the enumeration sequence.</span></span><br/>                                                               |



 

## <a name="requirements"></a><span data-ttu-id="87b87-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87b87-123">Requirements</span></span>



| <span data-ttu-id="87b87-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87b87-124">Requirement</span></span> | <span data-ttu-id="87b87-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="87b87-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87b87-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87b87-126">Minimum supported client</span></span><br/> | <span data-ttu-id="87b87-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87b87-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="87b87-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87b87-128">Minimum supported server</span></span><br/> | <span data-ttu-id="87b87-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="87b87-129">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="87b87-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="87b87-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="87b87-131"><dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="87b87-131"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="87b87-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="87b87-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87b87-133"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87b87-133"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="87b87-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="87b87-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="87b87-135"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87b87-135"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 

