---
title: Énumération WINBIO_POLICY_SOURCE ( \_ types WINBIO. h)
description: Répertorie les sources possibles d’informations de stratégie pour la détection de l’usurpation d’identité pour les facteurs biométriques.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- API Windows Biometric Framework de l’énumération WINBIO_POLICY_SOURCE
- API du pointeur d’énumération PWINBIO_POLICY_SOURCE Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237815"
---
# <a name="winbio_policy_source-enumeration"></a>Énumération de la source de la \_ stratégie WINBIO \_

Répertorie les sources possibles d’informations de stratégie pour la détection de l’usurpation d’identité pour les facteurs biométriques.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**\_stratégie WINBIO \_ inconnue**
</dt> <dd>

La source de la stratégie est inconnue.

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_ \_ valeur par défaut de la stratégie WINBIO**
</dt> <dd>

la stratégie est la stratégie par défaut fournie par le Windows Biometric Framework.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**\_stratégie WINBIO \_ locale**
</dt> <dd>

stratégie définie par l’utilisateur pour son compte à l’aide de l’application **Paramètres** . Cette stratégie remplace la stratégie par défaut.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_administrateur de stratégie WINBIO \_**
</dt> <dd>

Stratégie de groupe définie par l’administrateur informatique pour l’entreprise. Les utilisateurs individuels ne peuvent pas remplacer cette stratégie.

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
</dt> </dl>

 

 





