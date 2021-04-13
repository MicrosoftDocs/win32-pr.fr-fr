---
title: Classe Win32_RDMSCollectionProperties
description: Gère les propriétés d’une collection de bureaux virtuels.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSCollectionProperties de la classe Services Bureau à distance
- Win32_RDMSCollectionProperties de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384448"
---
# <a name="win32_rdmscollectionproperties-class"></a>\_Classe RDMSCollectionProperties Win32

Gère les propriétés d’une collection de bureaux virtuels.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDMSCollectionProperties** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](/windows)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ RDMSCollectionProperties** possède ces méthodes.



| Méthode                                                                                        | Description                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**GetProvisioningProperties**](getprovisioningproperties-win32-rdmscollectionproperties.md) | Récupère les propriétés de configuration de la collection de bureaux virtuels.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ RDMSCollectionProperties** a ces propriétés.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient l’alias de la collection.

</dd> <dt>

**ReferenceVirtualDesktopAdapters**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit les noms des cartes réseau virtuelles de la machine virtuelle maître.

</dd> <dt>

**ReferenceVirtualDesktopArchitecture**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit l’architecture de processeur de la machine virtuelle maître.

</dd> <dt>

**ReferenceVirtualDesktopGuid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le GUID de la machine virtuelle principale.

</dd> <dt>

**ReferenceVirtualDesktopHost**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le nom du serveur hôte de la machine virtuelle maître.

</dd> <dt>

**ReferenceVirtualDesktopMachineName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le nom d’ordinateur de la machine virtuelle maître.

</dd> <dt>

**ReferenceVirtualDesktopName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le nom de la machine virtuelle maître.

</dd> <dt>

**ReferenceVirtualDesktopOsversion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit la version du système d’exploitation de la machine virtuelle principale.

</dd> <dt>

**ReferenceVirtualDesktopRamsizeMB**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit la taille de la mémoire de la machine virtuelle principale.

</dd> <dt>

**ReferenceVirtualDesktopRemoteFX**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si RemoteFX est activé pour la machine virtuelle Master. **True** si RemoteFX est activé ; Sinon, **false**. La valeur par défaut de cette propriété est **false**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fournisseur de services de gestion Bureau à distance](rdms-api-reference.md)
</dt> </dl>

 

