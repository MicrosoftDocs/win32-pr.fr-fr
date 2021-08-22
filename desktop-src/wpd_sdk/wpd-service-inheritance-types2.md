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
ms.openlocfilehash: 5a0e69986e7415a5a12eca7c450b0d7ff064c650d33c35997b9a166b01592c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444799"
---
# <a name="wpd_service_inheritance_types-enumeration"></a>\_ \_ Énumération des types d’héritage du service wpd \_

Le type d’énumération des **\_ types d' \_ héritage \_ du service wpd** spécifie la relation d’héritage pour un service.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**\_implémentation de \_ l’héritage du service wpd \_**
</dt> <dd>

Le service hérite en implémentant une définition de service abstraite.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPortableDeviceServiceCapabilities::GetInheritedServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




