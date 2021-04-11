---
title: Énumération WINBIO_ANTI_SPOOF_POLICY_ACTION ( \_ types WINBIO. h)
description: Spécifie les types d’actions que vous effectuez pour la stratégie d’antiusurpation d’un utilisateur.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- API Windows Biometric Framework de l’énumération WINBIO_ANTI_SPOOF_POLICY_ACTION
- API du pointeur d’énumération PWINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942351"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>\_ \_ \_ Énumération des actions de stratégie anti-usurpation WINBIO \_

Spécifie les types d’actions que vous effectuez pour la stratégie d’antiusurpation d’un utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**désactivation de la \_ protection contre l' \_ usurpation WINBIO \_**
</dt> <dd>

Désactive la détection de l’usurpation d’identité pour un facteur biométrique.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ anti- \_ usurpation \_ activée**
</dt> <dd>

Active la détection de l’usurpation d’identité pour un facteur biométrique.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO \_ anti- \_ usurpation \_**
</dt> <dd>

Supprime l’intégralité de la stratégie d’antiusurpation pour le facteur biométrique du compte.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_action de stratégie anti- \_ usurpation WINBIO \_ \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**SOURCE de la \_ stratégie WINBIO \_**](winbio-policy-source.md)
</dt> </dl>

 

 





