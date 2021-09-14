---
title: Structure WINBIO_ANTI_SPOOF_POLICY ( \_ types WINBIO. h)
description: Représente la stratégie d’antiusurpation pour un utilisateur.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- API de Windows Biometric Framework de structure de WINBIO_ANTI_SPOOF_POLICY
- API du pointeur de structure PWINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011171"
---
# <a name="winbio_anti_spoof_policy-structure"></a>\_Structure de stratégie anti- \_ usurpation WINBIO \_

Représente la stratégie d’antiusurpation pour un utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a>Membres

<dl> <dt>

**Action**
</dt> <dd>

Type d’action à entreprendre pour la stratégie d’antiusurpation.

</dd> <dt>

**Source**
</dt> <dd>

Source de la stratégie d’antiusurpation.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_action de stratégie anti- \_ usurpation WINBIO \_ \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**SOURCE de la \_ stratégie WINBIO \_**](winbio-policy-source.md)
</dt> <dt>

[**\_Résultat asynchrone \_ WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





