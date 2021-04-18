---
title: Structure MPEXPIRATION_DATA (MpClient. h)
description: Notification d’état d’expiration du produit.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPEXPIRATION_DATA
- PMPEXPIRATION_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512140"
---
# <a name="mpexpiration_data-structure"></a>\_Structure de données MPEXPIRATION

Notification d’état d’expiration du produit.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**Motif**
</dt> <dd>

Type : **\_ \_ raison** de l’expiration du point de gestion

</dd> <dd>

Raison de l’expiration. Il s’agit de l’une des valeurs possibles suivantes :



| Valeur                                                                                                                                                                                                                                | Signification                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> Pack d’e <dt>**\_ EXPIRÉ \_ inconnu**</dt> <dt>0</dt> </dl> | Inconnu.<br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> Pack d’e <dt>**\_ \_Eval expiré**</dt> <dt>1</dt> </dl>          | Analyse.<br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> Pack d’e <dt>**\_ \_Wat expirée**</dt> <dt>2</dt> </dl>             | Wat.<br/>        |



 

</dd> <dt>

**State**
</dt> <dd>

Type : **\_ \_ \_ rapport d’état d’expiration** du point de gestion

</dd> <dd>

État d’expiration. Il s’agit de l’une des valeurs possibles suivantes :



| Valeur                                                                                                                                                                                                                                                                      | Signification                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> Pack d’e <dt>**\_ Rapport d' \_ État d’expiration \_ \_ inconnu**</dt> <dt>0</dt> </dl> | État inconnu.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> Pack d’e <dt>**\_ Rapport d' \_ État d’expiration \_ \_ valide**</dt> <dt>1</dt> </dl>       | Pas d’expiration.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> Pack d’e <dt>**\_ \_ \_ \_ Avertissement de rapport d’état d’expiration**</dt> <dt>2</dt> </dl> | Proche de l’expiration.<br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> Pack d’e <dt>**\_ Le rapport d’état d’expiration \_ \_ \_ a expiré**</dt> <dt>3</dt> </dl> | Fin.<br/>       |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





