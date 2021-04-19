---
description: Représente les paramètres de luminosité d’un moniteur d’ordinateur.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: WmiMonitorBrightness, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521944"
---
# <a name="wmimonitorbrightness-class"></a>WmiMonitorBrightness, classe

La classe WMI **WmiMonitorBrightness** représente les paramètres de luminosité d’un moniteur d’ordinateur.

## <a name="syntax"></a>Syntaxe

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a>Membres

La classe **WmiMonitorBrightness** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **WmiMonitorBrightness** possède les propriétés suivantes.

<dl> <dt>

**Actif**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le moniteur cible est actif.

</dd> <dt>

**CurrentBrightness**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Luminosité actuelle. Cette valeur doit être comprise entre les *niveaux*.

Exemple : 100

</dd> <dt>

InstanceName
</dt> <dd> <dl> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : Clé
</dt> </dl>

Nom de l’instance d’analyse spécifique.

</dd> <dt>

**Niveau**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau contenant les niveaux de luminosité possibles.

Exemple : \[ 0, 1, 2,..., 100 \] .

</dd> <dt>

**Niveaux**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total de niveaux de luminosité pris en charge par le moniteur, comme décrit dans *niveau*.

Exemple : 101

</dd> </dl>

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir des exemples de code sur l’utilisation de cette classe dans PowerShell, consultez [Utiliser PowerShell pour créer des rapports et définir la luminosité](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx)de l’analyse.

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

 

 




