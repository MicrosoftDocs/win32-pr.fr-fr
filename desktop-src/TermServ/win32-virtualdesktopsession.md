---
title: Classe Win32_VirtualDesktopSession
description: Gère une session de bureau virtuel.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Win32_VirtualDesktopSession de la classe Services Bureau à distance
- Win32_VirtualDesktopSession de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e039df658ded4534e3e2582f08ba4e5f5a04530d810349fff5633730a84332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137422"
---
# <a name="win32_virtualdesktopsession-class"></a>\_Classe VirtualDesktopSession Win32

Gère une session de bureau virtuel.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ VirtualDesktopSession** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ VirtualDesktopSession** possède ces méthodes.



| Méthode                                                         | Description                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**Déconnecter**](disconnect-win32-virtualdesktopsession.md)   | Déconnecte la session de bureau virtuel.<br/>                        |
| [**Fermeture**](logoff-win32-virtualdesktopsession.md)           | Déconnecte l’utilisateur de la session de bureau virtuel.<br/>             |
| [**SendMessage**](sendmessage-win32-virtualdesktopsession.md) | Envoyer un message à l’utilisateur via la session de bureau virtuel.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ VirtualDesktopSession** a ces propriétés.

<dl> <dt>

**ClientMachineName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le nom de l’ordinateur client qui est connecté à la session.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le nom de la collection de bureaux virtuels qui héberge l’ordinateur virtuel.

</dd> <dt>

**ConnectState**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’état de la connexion à la session.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le nom de domaine de l’utilisateur.

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient l’ID de la session de bureau virtuel.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le nom du compte d’utilisateur affecté à la session.

</dd> <dt>

**VMHostName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient le nom du serveur hôte de virtualisation Bureau à distance qui héberge l’ordinateur virtuel.

</dd> <dt>

**VMName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le nom de l’ordinateur virtuel affecté à la session.

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

 

