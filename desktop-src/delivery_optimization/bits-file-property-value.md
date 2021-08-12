---
title: Structure BITS_FILE_PROPERTY_VALUE (Deliveryoptimization. h)
description: L’BITS_FILE_PROPERTY_VALUE Union fournit la valeur de la propriété du fichier DO en fonction d’une valeur de l’énumération BITS_FILE_PROPERTY_ID.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- Structure BITS_FILE_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba01a8c83cef842c40149b3fe8cbc586a7da5f819ffc387befb9f84182cbce24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544624"
---
# <a name="bits_file_property_value-structure"></a>Structure BITS_FILE_PROPERTY_VALUE

L' **BITS_FILE_PROPERTY_VALUE** Union fournit la valeur de la propriété du fichier do en fonction d’une valeur de l’énumération [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Chaîne**
</dt> <dd>

Cette valeur est utilisée lors de l’utilisation de la valeur enum de l’ID de propriété **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)
</dt> <dt>

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





