---
title: Classe Win32_RDMSVirtualDesktop
description: Représente un bureau virtuel.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510531"
---
# <a name="win32_rdmsvirtualdesktop-class"></a>\_Classe RDMSVirtualDesktop Win32

Représente un bureau virtuel.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDMSVirtualDesktop** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ RDMSVirtualDesktop** possède ces méthodes.



| Méthode                                                                                              | Description                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**GetUserAssignment**](getuserassignment-win32-rdmsvirtualdesktop.md)                             | Récupère le nom d’utilisateur et le nom de domaine de l’utilisateur affecté au bureau virtuel.<br/> |
| [**GetVirtualDesktopAssignedToUser**](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | Récupère le bureau virtuel affecté à l’utilisateur spécifié.<br/>                       |
| [**GetVirtualDesktopDetails**](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | Récupère les informations supplémentaires sur le bureau virtuel.<br/>                             |
| [**GetVirtualDesktopState**](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | Récupère l’état du bureau virtuel.<br/>                                                 |
| [**RemoveUserAssignment**](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | Supprime l’affectation d’utilisateur du bureau virtuel.<br/>                                       |
| [**SetUserAssignment**](setuserassignment-win32-rdmsvirtualdesktop.md)                             | Affecte un bureau virtuel à un utilisateur.<br/>                                                        |
| [**SetVirtualDesktopState**](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | Met à jour l’état du bureau virtuel.<br/>                                                   |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ RDMSVirtualDesktop** a ces propriétés.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtient l’alias de la collection de bureaux virtuels qui gère l’ordinateur virtuel.

</dd> <dt>

**HostName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le nom de l’ordinateur qui héberge l’ordinateur virtuel.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient le nom de l’ordinateur virtuel.

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtient l’état de la session de bureau virtuel.

</dd> <dt>

**SessionUserName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtient le nom d’utilisateur de l’utilisateur qui est connecté à la session de bureau virtuel.

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’état de la machine virtuelle.

</dd> <dt>

**UserDomain**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtient le nom de domaine de l’utilisateur affecté au bureau virtuel.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtient le nom d’utilisateur de l’utilisateur affecté au bureau virtuel.

</dd> <dt>

**VMState**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’état du bureau virtuel.

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

 

