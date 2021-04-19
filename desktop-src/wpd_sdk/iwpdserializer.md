---
description: 'L’interface IWpdSerializer est utilisée par le pilote de périphérique pour sérialiser les interfaces IPortableDeviceValues vers et depuis les mémoires tampons de données brutes utilisées pour communiquer avec l’application. Les applications n’ont pas besoin d’utiliser cette interface, car les données sont sérialisées et désérialisées automatiquement lors de l’appel de IPortableDevice :: SendCommand. pour accéder à cette interface, appelez CoCreateInstance et Pass dans IID \_ IWpdSerializer.'
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Interface IWpdSerializer (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531011"
---
# <a name="iwpdserializer-interface"></a><span data-ttu-id="4bea3-103">Interface IWpdSerializer</span><span class="sxs-lookup"><span data-stu-id="4bea3-103">IWpdSerializer interface</span></span>

<span data-ttu-id="4bea3-104">L’interface **IWpdSerializer** est utilisée par le pilote de périphérique pour sérialiser les interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) vers et depuis les mémoires tampons de données brutes utilisées pour communiquer avec l’application.</span><span class="sxs-lookup"><span data-stu-id="4bea3-104">The **IWpdSerializer** interface is used by the device driver to serialize [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces to and from the raw data buffers used to communicate with the application.</span></span>

<span data-ttu-id="4bea3-105">Les applications n’ont pas besoin d’utiliser cette interface, car les données sont sérialisées et désérialisées automatiquement lors de l’appel de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="4bea3-105">Applications do not need to use this interface, because the data is serialized and deserialized automatically when calling [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

<span data-ttu-id="4bea3-106">Pour accéder à cette interface, appelez **CoCreateInstance** et Pass dans **IID \_ IWpdSerializer**.</span><span class="sxs-lookup"><span data-stu-id="4bea3-106">To get this interface, call **CoCreateInstance** and pass in **IID\_IWpdSerializer**.</span></span>

## <a name="members"></a><span data-ttu-id="4bea3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4bea3-107">Members</span></span>

<span data-ttu-id="4bea3-108">L’interface **IWpdSerializer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4bea3-108">The **IWpdSerializer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4bea3-109">**IWpdSerializer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4bea3-109">**IWpdSerializer** also has these types of members:</span></span>

-   [<span data-ttu-id="4bea3-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4bea3-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4bea3-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4bea3-111">Methods</span></span>

<span data-ttu-id="4bea3-112">L’interface **IWpdSerializer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4bea3-112">The **IWpdSerializer** interface has these methods.</span></span>



| <span data-ttu-id="4bea3-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="4bea3-113">Method</span></span>                                                                                          | <span data-ttu-id="4bea3-114">Description</span><span class="sxs-lookup"><span data-stu-id="4bea3-114">Description</span></span>                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bea3-115">**GetBufferFromIPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="4bea3-115">**GetBufferFromIPortableDeviceValues**</span></span>](iwpdserializer-getbufferfromiportabledevicevalues.md) | <span data-ttu-id="4bea3-116">Sérialise une interface **IPortableDeviceValues** soumise à un tableau d’octets alloué.</span><span class="sxs-lookup"><span data-stu-id="4bea3-116">Serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span><br/>                |
| [<span data-ttu-id="4bea3-117">**GetIPortableDeviceValuesFromBuffer**</span><span class="sxs-lookup"><span data-stu-id="4bea3-117">**GetIPortableDeviceValuesFromBuffer**</span></span>](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | <span data-ttu-id="4bea3-118">Désérialise un tableau d’octets en une interface **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="4bea3-118">Deserializes a byte array to an **IPortableDeviceValues** interface.</span></span><br/>                                  |
| [<span data-ttu-id="4bea3-119">**GetSerializedSize**</span><span class="sxs-lookup"><span data-stu-id="4bea3-119">**GetSerializedSize**</span></span>](iwpdserializer-getserializedsize.md)                                   | <span data-ttu-id="4bea3-120">Calcule la taille de la mémoire tampon requise pour contenir une interface **IPortableDeviceValues** sérialisée.</span><span class="sxs-lookup"><span data-stu-id="4bea3-120">Calculates the buffer size that is required to hold a serialized **IPortableDeviceValues** interface.</span></span><br/> |
| [<span data-ttu-id="4bea3-121">**WriteIPortableDeviceValuesToBuffer**</span><span class="sxs-lookup"><span data-stu-id="4bea3-121">**WriteIPortableDeviceValuesToBuffer**</span></span>](iwpdserializer-writeiportabledevicevaluestobuffer.md) | <span data-ttu-id="4bea3-122">Sérialise une interface **IPortableDeviceValues** dans un tableau d’octets alloué par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="4bea3-122">Serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="4bea3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bea3-123">Requirements</span></span>



| <span data-ttu-id="4bea3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bea3-124">Requirement</span></span> | <span data-ttu-id="4bea3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bea3-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bea3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bea3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4bea3-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bea3-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4bea3-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4bea3-128">Library</span></span><br/> | <dl> <span data-ttu-id="4bea3-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bea3-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bea3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bea3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bea3-131">**Interfaces du pilote**</span><span class="sxs-lookup"><span data-stu-id="4bea3-131">**Driver Interfaces**</span></span>](driver-interfaces.md)
</dt> </dl>

 

