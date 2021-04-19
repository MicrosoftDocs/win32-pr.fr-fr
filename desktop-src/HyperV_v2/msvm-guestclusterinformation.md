---
description: Utilisé dans la méthode QueryGuestClusterInformation de la \_ classe MSVM VssService pour récupérer des informations sur le cluster invité dont fait partie la machine virtuelle.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Classe Msvm_GuestClusterInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515884"
---
# <a name="msvm_guestclusterinformation-class"></a>MSVM \_ GuestClusterInformation, classe

Utilisé dans la méthode [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) de la classe [**MSVM \_ VssService**](msvm-vssservice.md) pour récupérer des informations sur le cluster invité dont fait partie la machine virtuelle.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ GuestClusterInformation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ GuestClusterInformation** possède les propriétés suivantes.

<dl> <dt>

**ClusterId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur du cluster de basculement dont le système d’exploitation invité de la machine virtuelle fait partie.

</dd> <dt>

**ClusterSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de nœuds dans le cluster dont le système d’exploitation invité de la machine virtuelle fait partie.

</dd> <dt>

**IsActiveActive**
</dt> <dd> <dl> <dt>

Type de données : tableau **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau de valeurs booléennes correspondant à chaque disque dur virtuel partagé indiquant si la ressource de disque correspondante dans le cluster invité est partagée entre les machines virtuelles en mode actif/actif.

</dd> <dt>

**IsClustered**
</dt> <dd> <dl> <dt>

Type de données : tableau **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau de valeurs booléennes correspondant à chaque disque dur virtuel partagé indiquant si le disque correspondant est une ressource de cluster dans le cluster invité.

</dd> <dt>

**IsOnline**
</dt> <dd> <dl> <dt>

Type de données : tableau **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau de valeurs booléennes correspondant à chaque disque dur virtuel partagé indiquant si la ressource de disque correspondante dans le cluster invité est en ligne.

</dd> <dt>

**IsOwned**
</dt> <dd> <dl> <dt>

Type de données : tableau **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau de valeurs booléennes correspondant à chaque disque dur virtuel partagé, indiquant si la ressource de disque correspondante dans le cluster invité est Currenly appartenant à cette machine virtuelle.

</dd> <dt>

**LastResourceMoveTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de battements d’horloge lors du dernier déplacement de l’une des ressources de disque partagé.

> [!Note]  
> Cette propriété a été ajoutée dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

**SharedVirtualHardDiskPaths**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau de chemins d’accès de disque dur virtuel partagés connectés à la machine virtuelle.

</dd> <dt>

**SharedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Tableau de données de paramètre d’allocation de ressources (RASD) représentant les disques durs virtuels partagés connectés à la machine virtuelle.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

