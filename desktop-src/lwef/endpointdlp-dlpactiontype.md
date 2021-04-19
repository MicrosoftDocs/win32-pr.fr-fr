---
description: Spécifie le type d’action d’une opération de protection contre la perte de données (DLP) de point de terminaison.
title: Énumération DlpActionType (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495777"
---
# <a name="dlpactiontype-enumeration"></a>Énumération DlpActionType

Spécifie le type d’action d’une opération de protection contre la perte de données (DLP) de point de terminaison.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a>Constantes

<dl> <dt>

*DlpActionTypeCopyToRemovableMedia*
</dt> <dd>

Opération de copie sur un support amovible.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToNetworkShare*
</dt> <dd>

Opération de copie dans un dossier réseau partagé.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToClipboard*
</dt> <dd>

Opération de copie dans le presse-papiers.

</dd> </dl>

<dl> <dt>

*DlpActionTypePrint*
</dt> <dd>

Une opération d’impression.

</dd> </dl>


<dl> <dt>

*DlpActionTypeScreenClip*
</dt> <dd>

Opération de capture d’écran.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByUnallowedApp*
</dt> <dd>

Opération effectuée par une application non autorisée.

</dd> </dl>


<dl> <dt>

*DlpActionTypeCloudAppEgress*
</dt> <dd>

Opération ciblée vers un emplacement du Cloud.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByBluetoothApp*
</dt> <dd>

Opération qui comprend l’accès par une application Bluetooth.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByRDPApp*
</dt> <dd>

Opération qui comprend l’accès par un bureau à distance.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCount*
</dt> <dd>

Valeur maximale de l’énumération.

</dd> </dl>
 

## <a name="remarks"></a>Notes

Les valeurs de cette énumération sont utilisées par la structure [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .

## <a name="requirements"></a>Spécifications



| Condition requise          |    Valeur                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 (10,0 ; Build 17763)           |

