---
title: Classe Win32_RDMSJoinedNode
description: Représente un nœud de serveur géré par Bureau à distance Management Services (RDMS).
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Win32_RDMSJoinedNode de la classe Services Bureau à distance
- Win32_RDMSJoinedNode de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82a515f556c7193ef376972c5a8786dd0aaaafd7bcec3a56bf43244ea72a739
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868129"
---
# <a name="win32_rdmsjoinednode-class"></a>\_Classe RDMSJoinedNode Win32

Représente un nœud de serveur géré par Bureau à distance Management Services (RDMS).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDMSJoinedNode** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ RDMSJoinedNode** possède ces méthodes.



| Méthode                                                                | Description                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetJoinedNodeCount**](win32-rdmsjoinednode-getjoinednodecount.md) | **Windows Server 2012 R2 et Windows Server 2012 :** Cette méthode n’est pas disponible avant Windows Server 2016.<br/> Obtient le nombre de serveurs sur lesquels le rôle spécifié est installé.<br/> |
| [**Joindre**](join-win32-rdmsjoinednode.md)                             | Ajoute un nœud à RDMS.<br/>                                                                                                                                                                       |
| [**Disjoindre**](unjoin-win32-rdmsjoinednode.md)                         | Supprime un nœud de RDMS.<br/>                                                                                                                                                                  |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ RDMSJoinedNode** a ces propriétés.

<dl> <dt>

**FQDN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Obtient le nom de domaine complet du nœud.

</dd> <dt>

**IsGatewayCertificateInstalled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si le serveur a un certificat pour effectuer l’authentification pour les connexions Bureau à distance passerelle. **True** si le certificat est installé ; Sinon, **false**.

</dd> <dt>

**IsPublishingCertificateInstalled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si le serveur dispose d’un certificat pour signer protocole RDP (Remote Desktop Protocol) fichiers de publication. **True** si le certificat est installé ; Sinon, **false**.

</dd> <dt>

**IsRdcb**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si le serveur est Connexion Bureau à distance Broker. **True** si le serveur est un connexion Bureau à distance Broker ; Sinon, **false**.

</dd> <dt>

**IsRdg**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si le serveur est Bureau à distance serveur de passerelle. **True** si le serveur est un serveur de passerelle Bureau à distance ; Sinon, **false**.

</dd> <dt>

**IsRdls**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si le serveur est Bureau à distance serveur de licences. **True** si le serveur est un serveur de licences bureau à distance ; Sinon, **false**.

</dd> <dt>

**IsRdsh**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si le serveur est Bureau à distance serveur hôte de session. **True** si le serveur est un serveur hôte de session Bureau à distance ; Sinon, **false**.

</dd> <dt>

**IsRdvh**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si le serveur est Bureau à distance ordinateur hôte de virtualisation. **True** si le serveur est un hôte de virtualisation Bureau à distance ; Sinon, **false**.

</dd> <dt>

**IsRdwa**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si le serveur est Bureau à distance serveur d’accès Web. **True** si le serveur est un serveur Bureau à distance accès Web ; Sinon, **false**.

</dd> <dt>

**IsRedirectorCertificateInstalled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si le serveur a un certificat pour effectuer l’authentification pour le déploiement de Services Bureau à distance. **True** si le certificat est installé ; Sinon, **false**.

</dd> <dt>

**IsWebAccessCertificateInstalled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obtient et définit une valeur qui indique si le serveur a un certificat pour effectuer l’authentification pour Bureau à distance Accès web. **True** si le certificat est installé ; Sinon, **false**.

</dd> <dt>

**OSVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Obtient et définit la version des systèmes d’exploitation sur le nœud.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Obtient l’identificateur de sécurité (SID) du nœud.

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

 

