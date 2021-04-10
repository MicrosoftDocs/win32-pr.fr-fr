---
description: Contient des informations sur la requête de la batterie.
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
title: Structure BATTERY_QUERY_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 511980dd4307077b8b160550c661a15a5714b96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865085"
---
# <a name="battery_query_information-structure"></a>\_Structure des \_ informations sur les requêtes de batterie

Contient des informations sur la requête de la batterie. Cette structure est utilisée avec le code de contrôle des informations de requête de la [**\_ batterie \_ \_ IOCTL**](ioctl-battery-query-information.md) pour spécifier le type d’informations à retourner.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _BATTERY_QUERY_INFORMATION {
  ULONG                           BatteryTag;
  BATTERY_QUERY_INFORMATION_LEVEL InformationLevel;
  LONG                            AtRate;
} BATTERY_QUERY_INFORMATION, *PBATTERY_QUERY_INFORMATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**BatteryTag**
</dt> <dd>

La balise de batterie actuelle pour la batterie. Seules les informations relatives à une batterie correspondant à la balise peuvent être retournées. Chaque fois que cette valeur ne correspond pas à la balise active de la batterie, la demande IOCTL est effectuée avec le fichier d’erreur \_ \_ \_ introuvable. Cela indique à l’appelant que la batterie associée à la balise existe plus longtemps. L’appelant peut choisir d’utiliser l’opération de [**\_ \_ \_ balises de requête de batterie IOCTL**](ioctl-battery-query-tag.md) pour déterminer la balise de la batterie nouvellement installée, le cas échéant. (Pour plus d’informations, consultez [balises de batterie](battery-information.md) .)

Quand une demande d’informations sur une requête est effectuée, cette valeur est vérifiée. En outre, si la demande est en cours alors que cette valeur change, la demande est abandonnée avec l’état \_ fichier d' \_ erreur \_ introuvable.

</dd> <dt>

**InformationLevel**
</dt> <dd>

Niveau des informations de batterie interrogées. Les données retournées par l’IOCTL dépendent de cette valeur. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                               | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryDeviceName"></span><span id="batterydevicename"></span><span id="BATTERYDEVICENAME"></span><dl> <dt>**BatteryDeviceName**</dt> <dt>4</dt> </dl>                                                 | Chaîne Unicode terminée par le caractère null qui contient le nom de la batterie.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="BatteryEstimatedTime"></span><span id="batteryestimatedtime"></span><span id="BATTERYESTIMATEDTIME"></span><dl> <dt>**BatteryEstimatedTime**</dt> <dt>3</dt> </dl>                                     | **ULong** qui spécifie la durée d’exécution estimée de la batterie, en secondes. Si le taux de drainage fourni dans le membre **AtRate** de la structure d' **\_ \_ informations sur les requêtes** de la batterie est égal à zéro, ce calcul est basé sur le taux de drainage actuel. Si **AtRate** est différent de zéro, l’heure retournée correspond à la durée d’exécution attendue pour le taux donné. Si la durée estimée est inconnue (par exemple, si la batterie n’est pas déchargée et que le **AtRate** spécifié est égal à zéro), la valeur de retour est \_ durée d’indisponibilité de la batterie \_ . Notez que cette valeur n’est pas très précise sur certains systèmes de batterie et peut varier considérablement en fonction de l’utilisation actuelle de l’alimentation, ce qui peut être affecté par l’activité du disque et d’autres facteurs. Il n’existe aucun mécanisme de notification pour les modifications de cette valeur.<br/> |
| <span id="BatteryGranularityInformation"></span><span id="batterygranularityinformation"></span><span id="BATTERYGRANULARITYINFORMATION"></span><dl> <dt>**BatteryGranularityInformation**</dt> <dt>1</dt> </dl> | Tableau de [**batteries qui \_ signalent \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) des structures d’échelle, jamais plus de quatre entrées.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BatteryInformation"></span><span id="batteryinformation"></span><span id="BATTERYINFORMATION"></span><dl> <dt>**BatteryInformation**</dt> <dt>0</dt> </dl>                                             | Structure [**d' \_ informations sur la batterie**](battery-information-str.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BatteryManufactureDate"></span><span id="batterymanufacturedate"></span><span id="BATTERYMANUFACTUREDATE"></span><dl> <dt>**BatteryManufactureDate**</dt> <dt>5</dt> </dl>                             | Structure [**de \_ \_ Date**](battery-manufacture-date-str.md) de la fabrication d’une batterie.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="BatteryManufactureName"></span><span id="batterymanufacturename"></span><span id="BATTERYMANUFACTURENAME"></span><dl> <dt>**BatteryManufactureName**</dt> <dt>6</dt> </dl>                             | Chaîne Unicode terminée par le caractère null qui spécifie le nom du fabricant de la batterie.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatterySerialNumber"></span><span id="batteryserialnumber"></span><span id="BATTERYSERIALNUMBER"></span><dl> <dt>**BatterySerialNumber**</dt> <dt>8</dt> </dl>                                         | Chaîne Unicode terminée par le caractère null qui spécifie le numéro de série de la batterie.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryTemperature"></span><span id="batterytemperature"></span><span id="BATTERYTEMPERATURE"></span><dl> <dt>**BatteryTemperature**</dt> <dt>2</dt> </dl>                                             | **ULong** qui spécifie la température actuelle de la batterie, en dixièmes de degré Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryUniqueID"></span><span id="batteryuniqueid"></span><span id="BATTERYUNIQUEID"></span><dl> <dt>**BatteryUniqueID**</dt> <dt>7</dt> </dl>                                                         | Chaîne Unicode terminée par le caractère null qui identifie de façon unique la batterie. Cette valeur peut être utilisée pour effectuer le suivi d’une batterie spécifique. Dans le cas de batteries intelligentes, cet ID correspond à la concaténation du nom du fabricant, du nom de l’appareil, de la date de fabrication et d’une représentation imprimable du numéro de série. <br/> Cette valeur n’est pas destinée à être affichée à l’utilisateur.<br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**AtRate**
</dt> <dd>

Ce membre est utilisé uniquement si **InformationLevel** est BatteryEstimatedTime.

Si ce membre est différent de zéro, il s’agit d’un taux de drainage qui sera utilisé pour calculer le temps jusqu’à la déchargement de la batterie pour l’BatteryEstimatedTime d’une batterie individuelle. Elle doit être spécifiée dans mW et doit être une valeur négative pour représenter un taux de décharge de batterie.

</dd> </dl>

## <a name="remarks"></a>Notes

Certaines informations sur les batteries sont facultatives ou n’ont pas de sens pour certaines batteries. Si le type de données particulier demandé n’est pas disponible pour la batterie actuelle, la \_ fonction d’erreur non valide \_ est retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                                                                                                                                                                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                                                                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>Poclass. h ; </dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations sur la batterie**](battery-information-str.md)
</dt> <dt>

[**\_Date de fabrication de la batterie \_**](battery-manufacture-date-str.md)
</dt> <dt>

[**mise à l’échelle de la batterie \_ \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**\_ \_ informations sur les requêtes de batterie IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_ \_ balise de requête de batterie IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

 




