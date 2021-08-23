---
description: Indique une entrée MCA, corrigée de la vérification de l’ordinateur (CMC) ou erreur de plateforme corrigée (CPE). cette classe est disponible uniquement dans les systèmes Windowss 64 bits.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: Classe MSMCAInfo_Entry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8f6146d629678c1ee209738095fea901f0edb865bccb9aff2d4eeab02d18e773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640900"
---
# <a name="msmcainfo_entry-class"></a>\_Classe d’entrée MSMCAInfo

La classe d' **\_ entrée MSMCAInfo** indique une entrée MCA, corrigée de la vérification de l’ordinateur (CMC) ou une erreur de plateforme corrigée (CPE). cette classe est disponible uniquement dans les systèmes Windowss 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a>Membres

La classe d' **\_ entrée MSMCAInfo** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ entrée MSMCAInfo** a ces propriétés.

<dl> <dt>

**Données**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau d’entiers qui contient un enregistrement d’erreur MCA complet, tel qu’il est signalé par la couche d’abstraction système (SAL). Le SAL est du code gravé dans la mémoire ROM que le système d’exploitation appelle pour effectuer des opérations dépendantes de la plateforme. Il est similaire au BIOS sur une plateforme x86.

</dd> <dt>

**Durée**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre d’octets dans l’enregistrement d’erreur.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe d' **\_ entrée MSMCAInfo** est dérivée de [**MSMCAInfo**](msmcainfo.md).

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

 

 




