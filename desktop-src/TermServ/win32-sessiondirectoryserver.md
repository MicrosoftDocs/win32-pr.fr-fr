---
title: Classe Win32_SessionDirectoryServer
description: Fournit des propriétés pour afficher les propriétés d’un serveur Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryServer de la classe Services Bureau à distance
- Win32_SessionDirectoryServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941985"
---
# <a name="win32_sessiondirectoryserver-class"></a>\_Classe SessionDirectoryServer Win32

Fournit des propriétés pour afficher les propriétés d’un serveur Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).

> [!Note]  
> Dans Windows Server 2008 R2, le nom de session Broker TS (session Broker TS) a été modifié en service Broker pour les connexions Bureau à distance. Ces propriétés s’appliquent à tous les systèmes d’exploitation pris en charge, sauf indication contraire.

 

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SessionDirectoryServer** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SessionDirectoryServer** a ces propriétés.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la batterie de serveurs qui comprend le serveur.

</dd> <dt>

**LoadIndicator**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre relatif qui représente la charge du serveur hôte de session Bureau à distance lorsque l’algorithme d’équilibrage de charge par défaut est utilisé. La valeur de la propriété *LoadIndicator* est basée sur le nombre de sessions, le nombre de demandes de redirection en attente et la valeur de poids du serveur.

</dd> <dt>

**NumberOfSessions**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de sessions sur le serveur du Service Broker pour les connexions Bureau à distance.

</dd> <dt>

**NumPendRedir**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de demandes de redirection en attente.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse IP du serveur du Service Broker pour les connexions Bureau à distance. Si le serveur est configuré pour les adresses IPv4 et IPv6, il contient l’adresse IPv4.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom du serveur du Service Broker pour les connexions Bureau à distance.

</dd> <dt>

**ServerWeight**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur de poids du serveur, utilisée dans l’équilibrage de charge.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Paramètre de mode de session unique du serveur du Service Broker pour les connexions Bureau à distance.

<dt>

0
</dt> <dd>

La batterie de serveurs n’est pas en mode de session unique.

</dd> <dt>

1
</dt> <dd>

La batterie de serveurs de est en mode de session unique.

</dd> </dl>

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

[**\_SessionDirectorySession Win32**](win32-sessiondirectorysession.md)
</dt> </dl>

 

