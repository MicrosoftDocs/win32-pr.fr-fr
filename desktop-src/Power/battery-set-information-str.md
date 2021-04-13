---
description: Contient les informations sur la batterie à définir.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: Structure BATTERY_SET_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115558"
---
# <a name="battery_set_information-structure"></a>Structure des informations du \_ jeu de batteries \_

Contient les informations sur la batterie à définir. Cette structure est utilisée avec le code de contrôle d' [**\_ informations du \_ jeu \_ de batteries IOCTL**](ioctl-battery-set-information.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**BatteryTag**
</dt> <dd>

La balise de batterie actuelle pour la batterie. Les informations relatives à une batterie correspondant à la balise peuvent uniquement être retournées. Chaque fois que cette valeur ne correspond pas à la balise active de la batterie, la requête IOCTL se termine avec le fichier d’erreur \_ \_ \_ introuvable, ce qui indique à l’appelant que la batterie pour laquelle il a une balise n’existe plus. L’appelant peut choisir d’utiliser l’opération de [**\_ \_ \_ balises de requête de batterie IOCTL**](ioctl-battery-query-tag.md) pour déterminer la balise de la batterie nouvellement installée, le cas échéant. (Pour plus d’informations, consultez [balises de batterie](battery-information.md) .)

Quand une demande d’informations sur une requête est effectuée, cette valeur est vérifiée. En outre, si la demande est en cours alors que cette valeur change, la demande est abandonnée avec l’état \_ fichier d' \_ erreur \_ introuvable.

</dd> <dt>

**InformationLevel**
</dt> <dd>

Informations sur la batterie à définir. Le type de données dans le membre de la **mémoire tampon** dépend de la valeur de ce membre. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                       | Signification                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <dt>**BatteryCharge**</dt> <dt>1</dt> </dl>                         | Indique à l’appareil de batterie que l’utilisateur a demandé que la batterie soit chargée pour le moment. Par exemple, avec un sélecteur/batterie intelligent, l’application peut charger une batterie à la fois. Le membre de la **mémoire tampon** de cette structure est ignoré.<br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <dt>**BatteryCriticalBias**</dt> <dt>0</dt> </dl> | Définit le réglage de décalage critique de la batterie. Notez qu’il n’est pas prévu que cette valeur soit normalement modifiée par le logiciel et qu’elle soit présente dans les interfaces uniquement en tant que fonctionnalité de maintenance. Toutes les batteries ne peuvent pas gérer ce type de paramètre et les informations sur la batterie doivent être lues pour confirmer que la batterie a accepté le paramètre.<br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <dt>**BatteryDischarge**</dt> <dt>2</dt> </dl>             | Indique à l’appareil de batterie que l’utilisateur a demandé le déchargement de la batterie à ce moment-là. Par exemple, cela peut être utilisé pour indiquer la batterie que l’utilisateur veut actuellement alimenter sur le système. Le membre de la **mémoire tampon** de cette structure est ignoré.<br/>                                                                          |



 

</dd> <dt>

**Buffer**
</dt> <dd>

Informations sur la batterie à définir. Les données dépendent de la valeur de **InformationLevel**.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure d' **\_ \_ informations sur l’ensemble de batteries** est une structure de longueur variable et vous devez allouer une mémoire tampon de taille appropriée pour les informations à inclure dans la structure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                                                                                                                                                                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                                                                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>Poclass. h ; </dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ \_ informations sur le jeu de batteries IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

 




