---
description: Contient un événement MCA (machine Check architecture). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: d1806b91-43a3-4329-8fe5-de1e4755740f
title: Classe MSMCAInfo_RawMCAEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAEvent
- MSMCAInfo_RawMCAEvent.Active
- MSMCAInfo_RawMCAEvent.Count
- MSMCAInfo_RawMCAEvent.InstanceName
- MSMCAInfo_RawMCAEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: e15af79c67265823e0025849e4c2ef27f690265c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952687"
---
# <a name="msmcainfo_rawmcaevent-class"></a>MSMCAInfo \_ RawMCAEvent, classe

La classe **MSMCAInfo \_ RawMCAEvent** contient un événement MCA (machine Check architecture). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAInfo_RawMCAEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Membres

La classe **MSMCAInfo \_ RawMCAEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSMCAInfo \_ RawMCAEvent** possède les propriétés suivantes.

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

Chaîne qui identifie de façon unique cette instance de la classe **MSMCAInfo \_ RawMCAEvent** .

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

La classe **MSMCAInfo \_ RawMCAEvent** est dérivée de [**WmiEvent**](wmievent.md).

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

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

