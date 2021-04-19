---
description: Appareils mobiles Windows prend en charge les propriétés d’attribut de ressource suivantes.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Propriétés d’attribut de ressource (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541476"
---
# <a name="resource-attribute-properties"></a><span data-ttu-id="ba241-103">Propriétés d’attribut de ressource</span><span class="sxs-lookup"><span data-stu-id="ba241-103">Resource Attribute Properties</span></span>

<span data-ttu-id="ba241-104">Appareils mobiles Windows prend en charge les propriétés d’attribut de ressource suivantes.</span><span class="sxs-lookup"><span data-stu-id="ba241-104">Windows Portable Devices supports the following resource attribute properties.</span></span>



| <span data-ttu-id="ba241-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="ba241-105">Property</span></span>                                    | <span data-ttu-id="ba241-106">VarType</span><span class="sxs-lookup"><span data-stu-id="ba241-106">VarType</span></span>         | <span data-ttu-id="ba241-107">Description</span><span class="sxs-lookup"><span data-stu-id="ba241-107">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba241-108">**\_clé de \_ ressource d’attribut de ressource wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ba241-108">**WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY**</span></span> | <span data-ttu-id="ba241-109">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="ba241-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="ba241-110">Il s’agit d’un [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenant une valeur unique, qui est la clé qui identifie la ressource.</span><span class="sxs-lookup"><span data-stu-id="ba241-110">This is an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value, which is the key identifying the resource.</span></span>                     |
| <span data-ttu-id="ba241-111">**\_format d' \_ attribut de ressource wpd \_**</span><span class="sxs-lookup"><span data-stu-id="ba241-111">**WPD\_RESOURCE\_ATTRIBUTE\_FORMAT**</span></span>        | <span data-ttu-id="ba241-112">**\_CLSID VT**</span><span class="sxs-lookup"><span data-stu-id="ba241-112">**VT\_CLSID**</span></span>   | <span data-ttu-id="ba241-113">Valeur GUID qui spécifie le format de la ressource.</span><span class="sxs-lookup"><span data-stu-id="ba241-113">A GUID value that specifies the format of the resource.</span></span> <span data-ttu-id="ba241-114">Pour obtenir la liste des formats définis par les appareils mobiles Windows, consultez [formats d’objet](object-format-guids.md) .</span><span class="sxs-lookup"><span data-stu-id="ba241-114">See [Object Formats](object-format-guids.md) for a list of formats that are defined by Windows Portable Devices.</span></span> |
| <span data-ttu-id="ba241-115">**\_ \_ \_ taille totale de l’attribut de ressource wpd \_**</span><span class="sxs-lookup"><span data-stu-id="ba241-115">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>   | <span data-ttu-id="ba241-116">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="ba241-116">**VT\_UI8**</span></span>     | <span data-ttu-id="ba241-117">Taille totale des données de ressource, en octets.</span><span class="sxs-lookup"><span data-stu-id="ba241-117">The total size of the resource data, in bytes.</span></span>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="ba241-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ba241-118">Remarks</span></span>

<span data-ttu-id="ba241-119">Ces attributs sont retournés par la méthode [**IPortableDeviceResources :: GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="ba241-119">These attributes are returned by the [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba241-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba241-120">Requirements</span></span>



| <span data-ttu-id="ba241-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba241-121">Requirement</span></span> | <span data-ttu-id="ba241-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba241-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba241-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba241-123">Header</span></span><br/> | <dl> <span data-ttu-id="ba241-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba241-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba241-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba241-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba241-126">**IPortableDeviceResources::GetResourceAttributes**</span><span class="sxs-lookup"><span data-stu-id="ba241-126">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[<span data-ttu-id="ba241-127">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="ba241-127">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




