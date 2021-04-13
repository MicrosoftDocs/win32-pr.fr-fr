---
title: Classe MSAD_DomainController
description: Représente le contrôleur de domaine sur lequel s’exécute le fournisseur WMI.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController de la classe Active Directory
- MSAD_DomainController de la classe Active Directory, Description
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465395"
---
# <a name="msad_domaincontroller-class"></a>\_Classe DOMAINCONTROLLER MSAD

Représente le contrôleur de domaine sur lequel s’exécute le fournisseur WMI.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a>Membres

La **classe \_ DomainController MSAD** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La **classe \_ DomainController MSAD** possède ces méthodes.



| Méthode                                                 | Description                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ExecuteKCC**](executekcc-msad-domaincontroller.md) | Appelle le vérificateur de cohérence des connaissances pour vérifier la topologie de réplication.<br/> |



 

### <a name="properties"></a>Propriétés

La **classe \_ DomainController MSAD** possède ces propriétés.

<dl> <dt>

**CommonName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le nom commun de l’objet serveur.

</dd> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient le chemin d’accès X. 500 de l’objet [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) .

</dd> <dt>

**IsAdvertisingToLocator**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si le service Localisateur sur le contrôleur de périphérique publie correctement. **True** si le service de localisation sur le contrôleur de service publie correctement ; Sinon, **false**.

</dd> <dt>

**IsGC**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si le DC est un serveur de catalogue global. **True** si le contrôleur de périphérique est un serveur de catalogue global ; Sinon, **false**.

</dd> <dt>

**IsNextRIDPoolAvailable**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si le DC a obtenu un autre pool RID. **True** si le contrôleur de l’objet a obtenu un autre pool RID et que l’allocation d’identificateurs RID sur ce contrôleur de groupe peut se poursuivre même si le pool actuel d’identificateurs RID est épuisé ; Sinon, **false**.

</dd> <dt>

**IsRegisteredInDNS**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si le contrôleur de domaine est inscrit correctement dans DNS. **True** si le contrôleur de domaine est inscrit correctement dans DNS ; Sinon, **false**.

</dd> <dt>

**IsSysVolReady**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur qui indique si SysVol a été publié correctement. **True** si SYSVOL a été publié correctement ; Sinon, **false**.

</dd> <dt>

**NTDsaGUID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le GUID associé à l’objet [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) dans le conteneur de configuration. L’objet **NTDS-DSA** représente le domaine Active Directory processus DSA du service sur le serveur.

</dd> <dt>

**PercentOfRIDsLeft**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le pourcentage d’identificateurs RID restants dans le pool RID actuel sur ce contrôleur de périphérique.

</dd> <dt>

**SiteName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le site dans lequel le contrôleur de site existe.

</dd> <dt>

**TimeOfOldestReplAdd**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’horodateur de l’opération d’ajout de réplication la plus ancienne qui est encore dans la file d’attente sur ce contrôleur de domaine.

</dd> <dt>

**TimeOfOldestReplDel**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’horodateur de l’opération de suppression de réplication la plus ancienne qui est encore dans la file d’attente sur ce contrôleur de domaine.

</dd> <dt>

**TimeOfOldestReplMod**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’horodateur de l’opération de modification de réplication la plus ancienne qui est encore dans la file d’attente sur ce contrôleur de domaine.

</dd> <dt>

**TimeOfOldestReplSync**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’horodateur de l’opération de synchronisation de réplication la plus ancienne qui est encore dans la file d’attente sur ce contrôleur de domaine.

</dd> <dt>

**TimeOfOldestReplUpdRefs**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’horodateur de l’opération de mise à jour de réplication la plus ancienne qui est encore dans la file d’attente sur ce contrôleur de domaine.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\MicrosoftActiveDirectory racine<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

