---
description: Contient des informations sur les conditions dans lesquelles l’état de la batterie doit être récupéré.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: Structure BATTERY_WAIT_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 52885b75c7f9afba7ff336b3210ecf1b852f85b0091afe13026616816e43d7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143592"
---
# <a name="battery_wait_status-structure"></a>Structure d’état d' \_ attente de la batterie \_

Contient des informations sur les conditions dans lesquelles l’état de la batterie doit être récupéré. Cette structure est utilisée par le code de contrôle de l’état de la [**\_ requête de batterie \_ \_ IOCTL**](ioctl-battery-query-status.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a>Membres

<dl> <dt>

**BatteryTag**
</dt> <dd>

La balise de batterie actuelle pour la batterie. Seules les informations relatives à une batterie correspondant à la balise peuvent être retournées. Chaque fois que cette valeur ne correspond pas à la balise active de la batterie, l’opération [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) échoue avec le code d’erreur fichier d’erreur \_ \_ \_ introuvable, qui indique à l’appelant que la batterie pour laquelle il a une balise n’est plus installée. l’appelant peut choisir d’utiliser l’opération d' [**étiquette de \_ requête de batterie \_ \_ IOCTL**](ioctl-battery-query-tag.md) pour déterminer l’étiquette de la batterie nouvellement installée, le cas En outre, si la demande est en cours lors de la suppression de la batterie ou si la balise change, l’opération est abandonnée avec l’État fichier d’erreur \_ \_ \_ introuvable. (Pour plus d’informations, consultez [balises de batterie](battery-information.md) .)

</dd> <dt>

**Délai d'expiration**
</dt> <dd>

Nombre de millisecondes pendant lesquelles la requête attendra la condition spécifiée par les membres **PowerState**, **LowCapacity** et **HighCapacity** avant de se terminer. La valeur-1 indique que la demande attend indéfiniment que les conditions soient satisfaites. La valeur zéro indique que les informations sur la batterie demandées doivent être retournées immédiatement, indépendamment des autres conditions. Toute autre valeur indique que la requête doit attendre ce laps de temps, ou jusqu’à ce que l’une des autres conditions soit satisfaite.

Si l’ordinateur est passé en mode veille, l’horloge continue à s’exécuter, mais le fait d’épuiser le nombre n’est pas mis en éveil par l’ordinateur. Si le nombre est épuisé lorsque l’ordinateur est activé et que d’autres conditions sont satisfaites, l’appel est immédiatement retourné en cas de réveil.

</dd> <dt>

**PowerState**
</dt> <dd>

Zéro, un ou plusieurs des bits d’état suivants, qui indiquent l’état de la batterie. Il est identique au membre **PowerState** de la structure [**d' \_ État**](battery-status-str.md) de la batterie.



| Valeur                                                                                                                                                                                                                                                   | Signification                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <dt>**Batterie \_ CHARGEMENT**</dt> de <dt>0x00000004</dt> </dl>                  | Indique que la batterie est en cours de chargement.<br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <dt>**Batterie \_**</dt> <dt>0x00000008</dt> critique </dl>                  | Indique que la défaillance de la batterie est imminente. Pour plus d'informations, consultez la section Notes.<br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <dt>**Batterie \_ Déchargement**</dt> de <dt>0x00000002</dt> </dl>         | Indique que la batterie est en cours de déchargement.<br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <dt>**Batterie \_ METTRE \_ sous \_ tension**</dt> <dt>0x00000001</dt> </dl> | Indique que la batterie a accès à l’alimentation secteur.<br/>                                        |



 

</dd> <dt>

**LowCapacity**
</dt> <dd>

Capacité actuelle de la batterie, en mWh (ou relatif). Cette valeur est identique à la **capacité** membre de la structure d' [**\_ État**](battery-status-str.md) de la batterie.

</dd> <dt>

**HighCapacity**
</dt> <dd>

Capacité actuelle de la batterie, en mWh (ou relatif). Cette valeur est identique à la **capacité** membre de la structure d' [**\_ État**](battery-status-str.md) de la batterie.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les demandes d’informations sur la batterie sont reportées jusqu’à ce que l’un des éléments suivants se produise :

-   Le délai d’attente expire (en supposant que le **délai d’expiration** n’est pas-1).
-   L’état actuel de la batterie ne correspond pas à **PowerState**.
-   La capacité de la batterie est inférieure à **LowCapacity**.
-   La capacité de la batterie est supérieure à **HighCapacity**.
-   La balise de batterie change.

Quand l’une de ces conditions est satisfaite, les données sont collectées et l’opération est retournée. Cela permet aux applications de surveiller les informations de batterie dynamique classiques sans interroger l’appareil.

Avant d’utiliser l’une des deux conditions de capacité, assurez-vous que la batterie les prend en charge en utilisant le code de contrôle d' [**\_ \_ \_ État de la batterie IOCTL**](ioctl-battery-query-status.md) avec un délai d’expiration de zéro. Examinez les résultats pour déterminer si le membre de **capacité** est pris en charge (c’est-à-dire, pas de capacité de batterie \_ inconnue \_ ).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                                                                                                                                                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                                                                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>Poclass. h ;</dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**État de la batterie \_**](battery-status-str.md)
</dt> <dt>

[**État de la \_ requête de batterie IOCTL \_ \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_ \_ balise de requête de batterie IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

