---
description: Représente les fonctionnalités d’affichage prises en charge de l’analyse.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: SupportedDisplayFeaturesDescriptor, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524510"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>SupportedDisplayFeaturesDescriptor, classe

Le **SupportedDisplayFeaturesDescriptor** représente les fonctionnalités d’affichage prises en charge de l’analyse. Les informations contenues dans cette classe correspondent aux données de la définition d’entrée vidéo de la norme E-EDID (Extended Display Identification Data) améliorée de l’Association Video Electronics standard Association (VESA).

## <a name="syntax"></a>Syntaxe

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a>Membres

La classe **SupportedDisplayFeaturesDescriptor** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SupportedDisplayFeaturesDescriptor** possède les propriétés suivantes.

<dl> <dt>

**ActiveOffSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Prise en charge d’une alimentation active et très faible. L’affichage consomme moins d’énergie lorsqu’il reçoit un signal de minutage qui est en dehors de la plage de fonctionnement active déclarée. L’affichage est rétabli en mode de fonctionnement normal si le signal de minutage revient à la plage de fonctionnement normale. Les signaux de synchronisation en dehors de la plage de fonctionnement normale ne sont pas des signaux de synchronisation ou aucun signal.

</dd> <dt>

**DisplayType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type d’affichage de l’analyse. Le tableau suivant répertorie les valeurs possibles.



| Valeur                                                                              | Signification                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Affichage monochrome/nuances de gris<br/> |
| <dl> <dt>1 (0x1)</dt> </dl> | Affichage des couleurs RVB<br/>            |
| <dl> <dt>2 (0X2)</dt> </dl> | Affichage des couleurs non RVB<br/>   |



 

</dd> <dt>

**GTFSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’affichage est pris en charge par GTF. Si la **valeur est true**, l’affichage prend en charge les minutages basés sur la norme GTF à l’aide des valeurs de paramètre GTF par défaut.

</dd> <dt>

**HasPreferredTimingMode**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’affichage a un mode de minutage préféré. Si la **valeur est true**, le premier bloc de synchronisation détaillé contient le mode de minutage préféré du moniteur. L’utilisation du mode de minutage préféré est requise par EDID v. 1.3 et versions ultérieures.

</dd> <dt>

**sRGBSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si la **valeur est true**, l’affichage prend en charge sRVB.

</dd> <dt>

**StandbySupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’affichage prend en charge la mise en veille de la gestion de l’alimentation de l’affichage VESA (DPMS). Si la **valeur est true**, la mise en veille DPMS est prise en charge.

</dd> <dt>

**SuspendSupported**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’affichage prend en charge l’interruption de la gestion de l’alimentation de l’affichage VESA (DPMS). Si la **valeur est true**, DPMS suspend est pris en charge.

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

 

 




