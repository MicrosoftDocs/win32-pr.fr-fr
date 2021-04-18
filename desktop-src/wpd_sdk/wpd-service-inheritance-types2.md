---
description: Spécifie la relation d’héritage pour un service.
ms.assetid: e7f5314a-75e8-4f36-8e18-d614eda7a097
title: Énumération WPD_SERVICE_INHERITANCE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SERVICE_INHERITANCE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ad9115bf7bb0912362455986e77d5792cceec3b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525974"
---
# <a name="wpd_service_inheritance_types-enumeration"></a><span data-ttu-id="56ef7-103">\_ \_ Énumération des types d’héritage du service wpd \_</span><span class="sxs-lookup"><span data-stu-id="56ef7-103">WPD\_SERVICE\_INHERITANCE\_TYPES enumeration</span></span>

<span data-ttu-id="56ef7-104">Le type d’énumération des **\_ types d' \_ héritage \_ du service wpd** spécifie la relation d’héritage pour un service.</span><span class="sxs-lookup"><span data-stu-id="56ef7-104">The **WPD\_SERVICE\_INHERITANCE\_TYPES** enumeration type specifies the inheritance relationship for a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ef7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56ef7-105">Syntax</span></span>


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="56ef7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="56ef7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="56ef7-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**\_implémentation de \_ l’héritage du service wpd \_**</span><span class="sxs-lookup"><span data-stu-id="56ef7-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**WPD\_SERVICE\_INHERITANCE\_IMPLEMENTATION**</span></span>
</dt> <dd>

<span data-ttu-id="56ef7-108">Le service hérite en implémentant une définition de service abstraite.</span><span class="sxs-lookup"><span data-stu-id="56ef7-108">The service inherits by implementing an abstract service definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56ef7-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56ef7-109">Requirements</span></span>



| <span data-ttu-id="56ef7-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56ef7-110">Requirement</span></span> | <span data-ttu-id="56ef7-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="56ef7-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="56ef7-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="56ef7-112">Header</span></span><br/> | <dl> <span data-ttu-id="56ef7-113"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ef7-113"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ef7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56ef7-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ef7-115">**IPortableDeviceServiceCapabilities::GetInheritedServices**</span><span class="sxs-lookup"><span data-stu-id="56ef7-115">**IPortableDeviceServiceCapabilities::GetInheritedServices**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




