---
description: Contient un événement de plateforme corrigé (CPE). cette classe est disponible uniquement dans les systèmes Windowss 64 bits.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: Classe MSMCAInfo_RawCorrectedPlatformEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518956"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a>MSMCAInfo \_ RawCorrectedPlatformEvent, classe

La classe **MSMCAInfo \_ RawCorrectedPlatformEvent** contient un événement de plateforme corrigé (CPE). cette classe est disponible uniquement dans les systèmes Windowss 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Membres

La classe **MSMCAInfo \_ RawCorrectedPlatformEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSMCAInfo \_ RawCorrectedPlatformEvent** possède les propriétés suivantes.

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

**Enregistrements**
</dt> <dd> <dl> <dt>

Type de données : tableau d' **\_ entrée MSMCAInfo**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau d’enregistrements d’erreurs MCA. Le nombre d’enregistrements d’erreurs MCA dans le tableau est spécifié par la propriété **Count** .

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **MSMCAInfo \_ RawCorrectedPlatformEvent** est dérivée de [**WmiEvent**](wmievent.md).

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

 

 




