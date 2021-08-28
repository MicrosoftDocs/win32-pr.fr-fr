---
description: Les qualificateurs suivants sont utilisés par le fournisseur WDM dans les fichiers MOF de pilote de périphérique lors de l’extraction de données à partir de WNODEs pour générer des instances de classes de pilote WDM.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Qualificateurs spécifiques du fournisseur WDM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 673b53d8cea23cd044175129af85c367f6f20c8dc92240c8bdf52f34708d96f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996079"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a>Qualificateurs spécifiques du fournisseur WDM

Les qualificateurs suivants sont utilisés par le [fournisseur WDM](/windows/desktop/WmiCoreProv/wdm-provider) dans les fichiers MOF de pilote de périphérique lors de l’extraction de données à partir de WNODEs pour générer des instances de classes de pilote WDM.

<dt>

<span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**
</dt> <dd>

Type de données : **DWORD, Array, UInt8, UInt16, UInt32, sint8, sint16 ou sint32.**

S’applique à : Properties

Une valeur manquante pour cette propriété doit être représentée par **null** au lieu de 0 (zéro).

</dd> <dt>

<span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**
</dt> <dd>

Type de données : **UInt32**

S’applique à : Properties

Index dans le WNODE des données pour la propriété. Le fournisseur WDM utilise ce qualificateur pour déterminer comment les données sont formatées lors de l’extraction des données à partir de WNODE et de la génération de classes WMI. La valeur de départ est 1.

</dd> <dt>

<span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**
</dt> <dd>

Type de données : **UInt32**

S’applique à : classes

Indication du coût des ressources pour accéder au bloc de données. Par exemple, les informations sur la géométrie du disque ne nécessitent pas beaucoup de ressources à obtenir, car elles sont disponibles dans l’extension de l’appareil. Les performances de lecture/écriture sur le disque sont plus gourmandes en ressources, car elles nécessitent un travail supplémentaire pour chaque opération de lecture/écriture. Par conséquent, la valeur du qualificateur **WMIExpense** est supérieure pour les performances de lecture/écriture sur le disque.

</dd> <dt>

<span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**
</dt> <dd>

Type de données : **UInt32**

S’applique à : méthodes

Index dans le WNODE des données pour la propriété. Le fournisseur WDM utilise ce qualificateur pour déterminer comment les données sont formatées lors de l’extraction des données à partir de WNODE et de la génération de classes WMI. La valeur de départ est 1.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



 

