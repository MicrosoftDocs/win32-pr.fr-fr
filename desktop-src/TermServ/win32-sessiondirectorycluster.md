---
title: Classe Win32_SessionDirectoryCluster
description: Fournit des propriétés pour l’affichage des propriétés d’une batterie de serveurs dans Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryCluster de la classe Services Bureau à distance
- Win32_SessionDirectoryCluster de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464966"
---
# <a name="win32_sessiondirectorycluster-class"></a>\_Classe SessionDirectoryCluster Win32

Fournit des propriétés pour l’affichage des propriétés d’une batterie de serveurs dans Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).

> [!Note]  
> Dans Windows Server 2008 R2, le nom de session Broker TS (session Broker TS) a été modifié en service Broker pour les connexions Bureau à distance. Ces propriétés s’appliquent à tous les systèmes d’exploitation pris en charge, sauf indication contraire.

 

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SessionDirectoryCluster** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SessionDirectoryCluster** a ces propriétés.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom de la batterie de serveurs du Service Broker pour les connexions Bureau à distance.

</dd> <dt>

**NumberOfServers**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de serveurs dans la batterie de serveurs du Service Broker pour les connexions Bureau à distance.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Mode de session unique de la batterie de serveurs du Service Broker pour les connexions Bureau à distance.

<dt>

0
</dt> <dd>

La batterie de serveurs du Service Broker pour les connexions Bureau à distance n’est pas en mode de session unique.

</dd> <dt>

1
</dt> <dd>

La batterie de serveurs du Service Broker pour les connexions Bureau à distance est en mode de session unique.

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

[**\_SessionDirectoryServer Win32**](win32-sessiondirectoryserver.md)
</dt> <dt>

[**\_SessionDirectorySession Win32**](win32-sessiondirectorysession.md)
</dt> </dl>

 

