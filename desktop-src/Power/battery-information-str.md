---
description: Contient des informations sur la batterie.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: Structure BATTERY_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: c449f325e03fb4ea81fe0aa148eaddcf65800b5a56356e22232477e0b6d4fa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033009"
---
# <a name="battery_information-structure"></a>\_Structure d’informations sur la batterie

Contient des informations sur la batterie. Cette structure est retournée par le code de contrôle des informations de requête de la [**\_ batterie \_ \_ IOCTL**](ioctl-battery-query-information.md) lorsque le niveau d’information BatteryInformation est demandé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**Capabilities**
</dt> <dd>

Capacités de la batterie. Ce membre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                 | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <dt>**Batterie \_ 0x40000000 \_ relative**</dt> à la capacité <dt></dt> </dl>                    | Indique que les informations relatives à la capacité et au taux de la batterie sont relatives, et non dans des unités spécifiques. Si ce bit n’est pas défini, les unités de rapport sont milliwatts heure-Hours (mWh) pour Capacity et milliwatts (mW) pour rate. Si ce bit est défini, toutes les références aux unités dans la documentation de l’autre batterie peuvent être ignorées. Toutes les informations sur les taux sont signalées en unités par heure. Par exemple, si la capacité entièrement facturée est signalée comme 100, un taux de 200 indique que la batterie utilise toute sa capacité en une demi-heure.<br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <dt>**Batterie \_ EST 0x20000000 à \_ bref \_ terme**</dt> <dt></dt> </dl>                               | Indique que l’opération normale est destinée à une fonction de prévention de défaillance. Si ce bit n’est pas défini, la batterie est censée être utilisée lors de l’utilisation normale du système.<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <dt>**Batterie \_ DÉFINIR les \_ frais \_ pris en charge**</dt> <dt>0x00000001</dt> </dl>          | Indique que les demandes d’informations set du type BatteryCharge sont prises en charge par ce périphérique de batterie.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <dt>**Batterie \_ DÉFINIR un \_ rejet \_ pris en charge**</dt> <dt>0x00000002</dt> </dl> | Indique que les demandes d’informations set du type BatteryDischarge sont prises en charge par ce périphérique de batterie.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <dt>**Batterie \_ \_Batterie système**</dt> <dt>0x80000000</dt> </dl>                             | Indique que la batterie peut fournir une alimentation générale pour l’exécution du système.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Technology**
</dt> <dd>

La technologie de la batterie. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                        | Signification                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Batterie Nonrechargeable, par exemple, alcaline.<br/> |
| <dl> <dt>1</dt> </dl> | Batterie refacturable, par exemple, l’acide de leads.<br/>   |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> <dt>

**Chimique**
</dt> <dd>

Chaîne de caractères abrégée qui indique la chimie de la batterie. Cette chaîne ne se termine pas nécessairement par zéro. Voici une liste partielle des abréviations qui peuvent être retournées et des Chemistries associés.



| chaîne Unicode                                                                                                                                           | Signification                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <dt>**PbAc**</dt> </dl> | Acidité<br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <dt>**LION**</dt> </dl>                        | Lithium-ion<br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <dt>**Li-I**</dt> </dl> | Lithium-ion<br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <dt>**NiCd**</dt> </dl> | Nickel cadmium<br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <dt>**NiMH**</dt> </dl> | Nickel metal-hydrure<br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <dt>**NiZn**</dt> </dl> | Nickel-zinc<br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <dt>**RAM**</dt> </dl>                           | Alkaline-Manganese refacturable<br/> |



 

D’autres Chemistries peuvent apparaître à l’avenir et votre code doit être en mesure de les gérer.

</dd> <dt>

**DesignedCapacity**
</dt> <dd>

Capacité théorique de la batterie lorsqu’elle est nouvelle, dans mWh, sauf si la capacité de la batterie \_ \_ est définie. Dans ce cas, les unités ne sont pas définies.

</dd> <dt>

**FullChargedCapacity**
</dt> <dd>

Capacité totale actuelle de la batterie dans mWh (ou relative). Comparez cette valeur à **DesignedCapacity** pour estimer l’usure de la batterie.

</dd> <dt>

**DefaultAlert1**
</dt> <dd>

Capacité suggérée par le fabricant, en mWh, à laquelle une alerte de batterie faible doit se produire. Les définitions de faible varient d’un fabricant au fabricant. En général, un état d’avertissement se produit avant un État faible, mais vous ne devez pas supposer qu’il le sera toujours. Pour réduire les risques de perte de données, cette valeur est généralement utilisée comme paramètre par défaut pour l’alarme de batterie critique.

</dd> <dt>

**DefaultAlert2**
</dt> <dd>

Capacité suggérée par le fabricant, en mWh, à laquelle une alerte de batterie d’avertissement doit se produire. Les définitions d’avertissement varient d’un fabricant à l’autres. En général, un état d’avertissement se produit avant un État faible, mais vous ne devez pas supposer qu’il le sera toujours. Pour réduire les risques de perte de données, cette valeur est généralement utilisée comme paramètre par défaut pour l’alerte de batterie faible.

</dd> <dt>

**CriticalBias**
</dt> <dd>

Biais de zéro, dans mWh, qui est appliqué à la création de rapports de batterie. Certaines batteries réservent une petite charge qui est écartée des valeurs de capacité de la batterie pour afficher « 0 » comme niveau de batterie critique. Le décalage critique est similaire à la définition d’une jauge de carburant pour afficher « vide » lorsqu’il existe plusieurs litres de carburant.

</dd> <dt>

**CycleCount**
</dt> <dd>

Nombre de cycles de charge/décharge que la batterie a rencontrés. Cela permet de déterminer l’usure de la batterie. Si la batterie ne prend pas en charge un compteur de cycles, ce membre est égal à zéro.

</dd> </dl>

## <a name="remarks"></a>Remarques

En règle générale, un état d’avertissement se produit avant un État faible, mais vous ne devez pas le supposer. Il est possible d’interroger une batterie et de constater qu’aucun niveau d’alerte ne s’est produit, et d’interroger à nouveau la batterie et de la trouver déductible dans la mesure où les deux niveaux ont été atteints. Cela peut indiquer que vous n’êtes pas assez souvent interrogé. Cela peut également indiquer que la batterie ne peut pas être facturée pendant très longtemps et qu’elle est en train de se décharger plus rapidement que prévu. Une batterie de ce type est proche de la fin de sa durée de vie utile, ou elle est peut-être endommagée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                                                                                                                                                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                                                                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>Poclass. h ;</dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ \_ informations sur les requêtes de batterie IOCTL \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




