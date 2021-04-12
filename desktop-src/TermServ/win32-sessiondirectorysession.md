---
title: Classe Win32_SessionDirectorySession
description: Fournit des propriétés pour afficher les propriétés d’une session Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectorySession de la classe Services Bureau à distance
- Win32_SessionDirectorySession de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384148"
---
# <a name="win32_sessiondirectorysession-class"></a>\_Classe SessionDirectorySession Win32

Fournit des propriétés pour afficher les propriétés d’une session Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).

> [!Note]  
> Dans Windows Server 2008 R2, le nom de session Broker TS (session Broker TS) a été modifié en service Broker pour les connexions Bureau à distance. Ces propriétés s’appliquent à tous les systèmes d’exploitation pris en charge, sauf indication contraire.

 

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SessionDirectorySession** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SessionDirectorySession** a ces propriétés.

<dl> <dt>

**ApplicationType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

L’application a démarré avec cette session. C’est le même que la propriété **StartProgram** de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).

</dd> <dt>

**La**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Profondeur de couleur de la session, mesurée en bits par pixel.

</dd> <dt>

**CreateTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création de la session. Cette valeur n’est pas réinitialisée lorsqu’une session est déconnectée et reconnectée.

</dd> <dt>

**DisconnectTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure auxquelles la session a été déconnectée (le cas échéant).

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine de l’utilisateur connecté à cette session.

</dd> <dt>

**ResolutionHeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Hauteur de la session, en pixels, pour cette session.

</dd> <dt>

**ResolutionWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Largeur de la session, en pixels, pour cette session.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse IP du serveur du Service Broker pour les connexions Bureau à distance pour cette session.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom du serveur du Service Broker pour les connexions Bureau à distance pour cette session.

</dd> <dt>

**IDsession**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

ID de session pour cette session.

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État de cette session.

<dt>

0
</dt> <dd>

La session est active.

</dd> <dt>

1
</dt> <dd>

La session est déconnectée.

</dd> </dl>

</dd> <dt>

**TSProtocol**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Protocole pour cette session.

<dt>

0
</dt> <dd>

Cette session s’exécute sur une console physique.

</dd> <dt>

1
</dt> <dd>

Un protocole tiers propriétaire est utilisé pour cette session.

</dd> <dt>

2
</dt> <dd>

Protocole RDP (Remote Desktop Protocol) (RDP) est utilisé pour cette session.

</dd> </dl>

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom d’utilisateur de l’utilisateur connecté à cette session.

</dd> </dl>

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SessionDirectoryCluster Win32**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**\_SessionDirectoryServer Win32**](win32-sessiondirectoryserver.md)
</dt> </dl>

 

