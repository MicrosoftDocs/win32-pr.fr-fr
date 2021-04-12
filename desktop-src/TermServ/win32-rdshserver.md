---
title: Classe Win32_RDSHServer
description: Gère un serveur hôte de session Bureau à distance.
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer de la classe Services Bureau à distance
- Win32_RDSHServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317265"
---
# <a name="win32_rdshserver-class"></a>\_Classe RDSHServer Win32

Gère un serveur hôte de session Bureau à distance.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDSHServer** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ RDSHServer** possède ces méthodes.



| Méthode                                                                          | Description                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshserver.md)                   | Récupère une valeur de propriété entière d’un objet **Win32 \_ RDSHServer** .<br/>                                                                                                 |
| [**GetPendingStartServerList**](win32-rdshserver-getpendingstartserverlist.md) | Récupère une liste de serveurs en attente de démarrage.<br/>                                                                                                                           |
| [**GetStringProperty**](getstringproperty-win32-rdshserver.md)                 | Récupère une valeur de propriété de type chaîne d’un objet **Win32 \_ RDSHServer** .<br/>                                                                                                   |
| [**SetInt32Property**](setint32property-win32-rdshserver.md)                   | Met à jour une valeur de propriété entière d’un objet **Win32 \_ RDSHServer** .<br/>                                                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdshserver.md)                 | Met à jour une valeur de propriété de type chaîne d’un objet **Win32 \_ RDSHServer** .<br/>                                                                                                     |
| [**TestAndSetState**](win32-rdshserver-testandsetstate.md)                     | Compare l’état actuel à l’objet comparand spécifié ; Si les deux correspondent, l’État est défini sur une nouvelle valeur. Quelle que soit la correspondance, l’état actuel est également retourné.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ RDSHServer** a ces propriétés.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtient et définit l’alias de la collection de serveurs d’hôtes de la hôte à laquelle le serveur hôte hôte est affecté.

</dd> <dt>

**ConnectionBroker**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit le nom de l’Connexion Bureau à distance Broker (RDCB) qui gère l’accès des utilisateurs au serveur hôte hôte.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient et définit le nom du serveur de l’hôte de la configuration.

</dd> <dt>

**ServerState**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Décrit l’état du serveur. Toute valeur autre que la **cible \_ en cours d’exécution** (3) est réservée et doit être prise en compte comme un État non valide.

Les valeurs possibles sont.

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

**Cible \_ INCONNU** (1)


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

**Cible \_ En cours d’exécution** (3)


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

**Cible \_ NON valide** (8)


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

**Cible \_ DÉMARRAGE** (9)


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

**Cible \_ ARRÊT** (10)


</dt> <dd></dd> </dl>

**Windows server 2012 R2 et Windows server 2012 :** Cette propriété n’est pas disponible avant Windows Server 2016.

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

 

