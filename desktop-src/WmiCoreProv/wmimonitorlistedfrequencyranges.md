---
description: Répertorie les plages de fréquences prises en charge par l’analyse.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: WmiMonitorListedFrequencyRanges, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529277"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a>WmiMonitorListedFrequencyRanges, classe

La classe WMI **WmiMonitorListedFrequencyRanges** répertorie les plages de fréquences prises en charge par l’analyse. Ces plages se trouvent dans la définition d’entrée vidéo du bloc de données d’identification étendues (E-EDID) Enhanced Display standard Association (VESA) ou dans le fichier INF de Windows qui contient les données des pilotes de périphérique.

## <a name="syntax"></a>Syntaxe

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a>Membres

La classe **WmiMonitorListedFrequencyRanges** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **WmiMonitorListedFrequencyRanges** possède les propriétés suivantes.

<dl> <dt>

**Actif**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le moniteur actif.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Nom de l’instance d’analyse spécifique.

</dd> <dt>

**MonitorFreqRanges**
</dt> <dd> <dl> <dt>

Type de données : tableau **FrequencyRangeDescriptor**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste des plages de fréquence d’analyse représentées par des instances de la classe [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) .

</dd> <dt>

**NumOfMonitorFreqRanges**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de plages de fréquence d’analyse prises en charge.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Espace de noms<br/>                | \\WMI racine<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




