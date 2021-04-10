---
title: WINBIO_ACCOUNT_POLICY structure (WinBio \_ adapter. h)
description: Contient une stratégie d’antiusurpation propre à la valeur par défaut ou spécifique au compte.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- API de Windows Biometric Framework de structure de WINBIO_ACCOUNT_POLICY
- API du pointeur de structure PWINBIO_ACCOUNT_POLICY Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942123"
---
# <a name="winbio_account_policy-structure"></a>Structure de stratégie de \_ compte WINBIO \_

La structure de la **\_ \_ stratégie de compte WINBIO** contient une stratégie de lutte contre l’usurpation d’identité spécifique au compte ou à la valeur par défaut.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a>Membres

<dl> <dt>

**Identité**
</dt> <dd>

Structure [**d' \_ identité WINBIO**](winbio-identity.md) qui spécifie les informations de compte.

</dd> <dt>

**AntiSpoofBehavior**
</dt> <dd>

L’une des valeurs d’énumération d' [**\_ \_ action de \_ stratégie \_ anti-usurpation WINBIO**](winbio-anti-spoof-policy-action.md) qui spécifie l’action de stratégie d’usurpation d’identité à utiliser pour le compte.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour obtenir une description de l’utilisation de cette structure, consultez la rubrique relative à la méthode [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ adaptateur. h (include WinBio \_ adapter. h)</dt> </dl> |



 

 





