---
title: Énumération WINBIO_CREDENTIAL_FORMAT ( \_ types WINBIO. h)
description: Définit des indicateurs qui peuvent être utilisés pour spécifier le format des informations d’identification de l’utilisateur final.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- API Windows Biometric Framework de l’énumération WINBIO_CREDENTIAL_FORMAT
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011156"
---
# <a name="winbio_credential_format-enumeration"></a>\_Énumération du format des informations d’identification WINBIO \_

Définit des indicateurs qui peuvent être utilisés pour spécifier le format des informations d’identification de l’utilisateur final. Cette énumération est utilisée par la fonction [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**\_mot de passe WINBIO \_ générique**
</dt> <dd>

Le mot de passe est dans un format générique.

</dd> <dt>

<span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO \_ mot de passe \_ condensé**
</dt> <dd>

Le mot de passe est dans un format compressé.

</dd> <dt>

<span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ protégé par mot de passe \_**
</dt> <dd>

Les informations d’identification du mot de passe ont été encapsulées avec [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations des applications clientes](client-application-enumerations.md)
</dt> <dt>

[**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

