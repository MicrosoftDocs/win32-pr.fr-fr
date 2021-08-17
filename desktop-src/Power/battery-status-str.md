---
description: Contient l’état actuel de la batterie.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: Structure BATTERY_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 28b75a8eb1c7abf647f3f8ea61b29dedb40978f3ea639fc505364a12ae5e57cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143602"
---
# <a name="battery_status-structure"></a>Structure d’état de la batterie \_

Contient l’état actuel de la batterie. Cette structure est utilisée par le code de contrôle de l’état de la [**\_ requête de batterie \_ \_ IOCTL**](ioctl-battery-query-status.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a>Membres

<dl> <dt>

**PowerState**
</dt> <dd>

État de la batterie. Ce membre peut être égal à zéro, une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                   | Signification                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**Batterie \_ CHARGEMENT**</dt> de <dt>0x00000004</dt> </dl>                  | Indique que la batterie est en cours de chargement.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**Batterie \_**</dt> <dt>0x00000008</dt> critique </dl>                  | Indique que la défaillance de la batterie est imminente. Pour plus d'informations, consultez la section Notes.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**Batterie \_ Déchargement**</dt> de <dt>0x00000002</dt> </dl>         | Indique que la batterie est en cours de déchargement.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**Batterie \_ METTRE \_ sous \_ tension**</dt> <dt>0x00000001</dt> </dl> | Indique que le système a accès à l’alimentation secteur, donc aucune batterie n’est en cours de défacturation.<br/>   |



 

</dd> <dt>

**Capacité**
</dt> <dd>

Capacité actuelle de la batterie, en mWh (ou relatif). Cette valeur peut être utilisée pour générer un affichage de « jauge de gaz » en le divisant par le membre **FullChargedCapacity** de la structure d' [**\_ informations sur la batterie**](battery-information-str.md) . Si la capacité n’est pas disponible, il s’agit de la capacité inconnue de la batterie \_ \_ .

</dd> <dt>

**Voltage**
</dt> <dd>

Tension actuelle de la batterie sur les bornes de la batterie, en millivolts (MV). Si la tension n’est pas disponible, il s’agit d’une tension de batterie \_ inconnue \_ .

</dd> <dt>

**Tarif**
</dt> <dd>

Taux actuel de charge ou de décharge de la batterie. Cette valeur sera en milliwatts, sauf si les informations relatives au taux de batterie sont relatives, auquel cas elle sera en unités arbitraires par heure. Pour déterminer si les informations sur la batterie sont relatives, examinez l' \_ indicateur relatif à la capacité de la batterie \_ dans le membre **capacités** de la structure d' [**\_ informations sur la batterie**](battery-information-str.md) . Un taux positif différent de zéro indique une charge ; un taux négatif indique un déchargement. Certaines batteries signalent uniquement des taux de rejet. Si le taux n’est pas disponible, la fréquence de la batterie est inconnue pour ce membre \_ \_ . Si l’état de la batterie ou de la source d’alimentation change, le taux peut devenir disponible.

</dd> </dl>

## <a name="remarks"></a>Remarques

L' \_ indicateur critique de la batterie dans le membre **PowerState** de cette structure indique une condition matérielle « critique pour la batterie ». Ce niveau critique est défini par le fabricant de la batterie, et non par l’utilisateur dans la « alarme de batterie critique ». Cela signifie généralement que le système de batterie a calculé que la batterie est entièrement drainée et que toute puissance dessinée dépasse ce qui est attendu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                                                                                                                                                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                                                                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>Poclass. h ;</dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations sur la batterie**](battery-information-str.md)
</dt> <dt>

[**État de la \_ requête de batterie IOCTL \_ \_**](ioctl-battery-query-status.md)
</dt> </dl>

 

 




