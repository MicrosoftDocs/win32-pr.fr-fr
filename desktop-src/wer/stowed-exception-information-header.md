---
title: Structure STOWED_EXCEPTION_INFORMATION_HEADER
description: Contient des informations qui identifient la structure parente.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- STOWED_EXCEPTION_INFORMATION_HEADER structure Rapport d’erreurs Windows
- pointeur de structure PSTOWED_EXCEPTION_INFORMATION_HEADER Rapport d’erreurs Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220020"
---
# <a name="stowed_exception_information_header-structure"></a>Structure d' \_ \_ \_ en-tête d’informations d’exception arrimé

Contient des informations qui identifient la structure parente.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**Taille**
</dt> <dd>

Type : **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Taille, en octets, de la structure parente.

</dd> <dt>

**Signature**
</dt> <dd>

Type : **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur 32 bits qui spécifie la signature de la structure parente.



| Valeur                                                                                                                                                                                                                                                                                                            | Signification                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <dt>**Rangé \_ \_Informations sur l’exception \_ v1 \_ signature**</dt> <dt>'SE01 '</dt> </dl> | Cette valeur indique que le parent est une structure d’informations d’exception de l' **arrimage \_ \_ \_** .<br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <dt>**Rangé \_ \_Informations sur l’exception \_ v2 \_ signature**</dt> <dt>'SE02 '</dt> </dl> | Cette valeur indique que le parent est une structure d' [**informations d’exception Alrangée \_ \_ \_ v2**](stowed-exception-information-v2.md) .<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

[**Rangé \_ Les \_ informations \_ sur l’exception v2**](stowed-exception-information-v2.md) et l' **\_ \_ \_ en-tête d’informations d’exception arrimées** ne sont actuellement pas définis dans un en-tête disponible publiquement. vous devez donc les définir dans votre code source avant de les utiliser.

La structure d’informations d’exception de la version **\_ \_ \_ v1** est identique à cette structure, sauf qu’elle ne contient pas les membres **NestedExceptionType** et **NestedException** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Aucun</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations sur les exceptions bacalées \_ \_ \_ v2**](stowed-exception-information-v2.md)
</dt> </dl>

 

