---
description: Spécifie les journaux MCA (machine Check architecture) bruts. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: Classe MSMCAInfo_RawMCAData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 6cafc16ddbc91181cc2114def07a193941988228
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526103"
---
# <a name="msmcainfo_rawmcadata-class"></a>MSMCAInfo \_ RawMCAData, classe

**MSMCAInfo \_ RawMCAData** spécifie les journaux MCA (machine Check architecture) bruts. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Membres

La classe **MSMCAInfo \_ RawMCAData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSMCAInfo \_ RawMCAData** possède les propriétés suivantes.

<dl> <dt>

**Actif**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

TRUE si cette instance de la classe est active ; Sinon, **false**.

</dd> <dt>

**Count**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre d’enregistrements d’erreur.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificateur unique de cette instance de la classe.

</dd> <dt>

**Enregistrements**
</dt> <dd> <dl> <dt>

Type de données : tableau d' **\_ entrée MSMCAInfo**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau d’enregistrements d’erreurs MCA. Le nombre d’enregistrements d’erreurs MCA dans le tableau est spécifié par la propriété **Count** .

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **MSMCAInfo \_ RawMCAData** est dérivée de [**MSMCAInfo**](msmcainfo.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/>                                                         |
| Espace de noms<br/>                | \\WMI racine<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes MSMCA](msmca-classes.md)
</dt> <dt>

[**MSMCAInfo**](msmcainfo.md)
</dt> </dl>

 

