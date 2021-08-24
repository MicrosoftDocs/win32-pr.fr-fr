---
description: Fournit des informations d’État pour une image de disque dur virtuel existante.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Classe Msvm_VirtualHardDiskState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5896e8b19d2897084997bd01b65bbb0d6e80e0ca15f662fff38871bdc0b6755
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426309"
---
# <a name="msvm_virtualharddiskstate-class"></a>MSVM \_ VirtualHardDiskState, classe

Fournit des informations d’État pour une image de disque dur virtuel existante.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualHardDiskState** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualHardDiskState** possède les propriétés suivantes.

<dl> <dt>

**Alignment**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type d’alignement du disque dur virtuel. Il s’agit de l’une des valeurs suivantes.



| Valeur                                                                        | Signification                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>0</dt> </dl> | alignement de 512 octets.<br/> |
| <dl> <dt>1</dt> </dl> | alignement de 4 Ko.<br/>     |



 

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille du fichier de disque dur virtuel (quantité réelle de stockage consommée par le fichier), en octets.

</dd> <dt>

**FragmentationPercentage**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Approximation du pourcentage de blocs de disque virtuel fragmentés dans le fichier de disque dur virtuel.

</dd> <dt>

**Utilisées**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Cette propriété est réservée à une utilisation ultérieure.

</dd> <dt>

**MinInternalSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille minimale d’un disque dur virtuel, en octets. Cette taille est arrondie au plus grand multiple de la taille de secteur suivante.

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille de secteur physique utilisée par le disque physique sous-jacent, en octets.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Horodatage du disque dur virtuel

> [!Note]  
> ajouté dans Windows 10 et Windows Server 2016.

 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




