---
description: Contient des méthodes qui obtiennent le contenu brut de la définition d’entrée vidéo de la norme VESA (Video Electronics standard Association) (E-EDID) améliorée des données d’identification d’affichage étendu (E-EDID) v. 1. x blocs de données 128 octets standard.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: WmiMonitorDescriptorMethods, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526184"
---
# <a name="wmimonitordescriptormethods-class"></a>WmiMonitorDescriptorMethods, classe

La classe WMI **WmiMonitorDescriptorMethods** contient des méthodes qui obtiennent le contenu brut de la définition d’entrée vidéo de la norme VESA (Video Electronics standard Association) améliorée Extended Display Identification Data (E-EDID) v. 1. x blocs de données 128 octets standard.

## <a name="syntax"></a>Syntaxe

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Membres

La classe **WmiMonitorDescriptorMethods** possède les types de membres suivants :

-   [Méthodes](#wmimonitordescriptormethods-class)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **WmiMonitorDescriptorMethods** possède ces méthodes.



| Méthode                                                                                           | Description                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | Accède aux données brutes d’un bloc de descripteur EDID v. 1. x spécifié.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **WmiMonitorDescriptorMethods** possède les propriétés suivantes.

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

 

 




