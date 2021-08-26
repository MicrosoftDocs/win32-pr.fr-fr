---
title: Énumération WINBIO_CREDENTIAL_STATE ( \_ types WINBIO. h)
description: Définit des valeurs qui spécifient si des informations d’identification ont été associées aux données biométriques pour un utilisateur final.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- API Windows Biometric Framework de l’énumération WINBIO_CREDENTIAL_STATE
- API du pointeur d’énumération PWINBIO_CREDENTIAL_STATE Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0e176479a68d39b017e852e17a73691b8349d7c6faa6be62130007a09dcef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868059"
---
# <a name="winbio_credential_state-enumeration"></a>\_Énumération de l’état des informations d’identification WINBIO \_

Définit des valeurs qui spécifient si des informations d’identification ont été associées aux données biométriques pour un utilisateur final. Cette énumération est utilisée par la fonction [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**\_informations d’identification WINBIO \_ non \_ définies**
</dt> <dd>

Des informations d’identification ont été associées à l’utilisateur final.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**\_jeu d’informations d’identification WINBIO \_**
</dt> <dd>

Les informations d’identification n’ont pas été associées à l’utilisateur final.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations des applications clientes](client-application-enumerations.md)
</dt> <dt>

[**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





