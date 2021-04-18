---
description: Le \_ type d’énumération Options de suppression d’objet décrit les \_ options prises en charge par un appareil lors de la suppression d’un objet.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: Énumération DELETE_OBJECT_OPTIONS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543197"
---
# <a name="delete_object_options-enumeration"></a>SUPPRIMER \_ l' \_ énumération des options d’objet

Le type d’énumération **\_ \_ options de suppression d’objet** décrit les options prises en charge par un appareil lors de la suppression d’un objet.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**suppression de l' \_ appareil mobile \_ \_ sans \_ récurrence**
</dt> <dd>

Supprimer l’objet uniquement et échouer s’il a des enfants.

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_Suppression de l’appareil portable \_ \_ avec \_ récurrence**
</dt> <dd>

Supprimez l’objet et tous ses enfants.

</dd> </dl>

## <a name="remarks"></a>Notes

L’application peut récupérer les options de suppression que l’appareil prend en charge en appelant [**IPortableDeviceCapabilities :: GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) pour la commande de **Suppression d' \_ \_ \_ \_ \_ objets de commande wpd** . Il doit examiner la valeur de l’option **\_ \_ \_ \_ \_ \_ prise en charge de la gestion récursive des objets d’option wpd** retournée par cette méthode dans un objet [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




