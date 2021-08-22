---
description: Contient des informations sur l’inactivité du système.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: Structure SYSTEM_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 665c19a99bffae46cf20af8c5c634e2e9594ecd07d02f003f56d42277ce9a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143302"
---
# <a name="system_power_information-structure"></a>Structure des informations de gestion de l’alimentation du système \_ \_

Contient des informations sur l’inactivité du système.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**MaxIdlenessAllowed**
</dt> <dd>

Inactivité à laquelle le système est considéré comme inactif et dont le délai d’inactivité commence à compter, exprimé sous la forme d’un pourcentage. La suppression en dessous de ce nombre provoque l’annulation de la minuterie.

</dd> <dt>

**Inactivité**
</dt> <dd>

Niveau d’inactivité actuel, exprimé sous la forme d’un pourcentage.

</dd> <dt>

**TimeRemaining**
</dt> <dd>

Temps restant dans le minuteur d’inactivité, en secondes.

</dd> <dt>

**CoolingMode**
</dt> <dd>

Mode de refroidissement du système actuel. Ce membre doit avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                 | Signification                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <dt>**Bon de commande \_ TZ \_ actif**</dt> <dt>0</dt> </dl>                    | Le système est actuellement en mode de refroidissement actif.<br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <dt>**Bon de commande \_ TZ \_ - \_ mode 2 non valide**</dt> <dt></dt> </dl> | Le système ne prend pas en charge la limitation de l’UC ou aucune zone thermique n’est définie dans le système.<br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <dt>**Bon de commande \_ TZ \_ passif**</dt> <dt>1</dt> </dl>                 | Le système est actuellement en mode de refroidissement passif.<br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Notez que cette définition de structure a été omise par erreur dans Winnt. h. Cette erreur sera corrigée à l’avenir. En attendant, pour compiler votre application, incluez la définition de structure contenue dans cette rubrique dans votre code source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




