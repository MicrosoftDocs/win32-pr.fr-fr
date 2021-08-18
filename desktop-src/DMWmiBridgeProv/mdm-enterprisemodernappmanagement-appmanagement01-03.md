---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01_03
description: La \_ classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 03 fournit des informations spécifiques sur l’application, telles que le nom, la version et le serveur de publication.
ms.assetid: 424e68de-1411-490f-b33b-5243ffa5a31e
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_03
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_03, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_03
- MDM_EnterpriseModernAppManagement_AppManagement01_03.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9395f59519d37b5a86ec3aa1c8e53b03c5c75ee86b8431d2cd98239aef717b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018167"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_03-class"></a>\_Classe EnterpriseModernAppManagement \_ AppManagement01 \_ 03 de MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** fournit des informations spécifiques sur l’application, telles que le nom, la version et le serveur de publication.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_03
{
  string InstanceID;
  string ParentID;
  string Name;
  string Version;
  string Publisher;
  string Architecture;
  string InstallLocation;
  sint32 IsFramework;
  sint32 IsBundle;
  string InstallDate;
  string ResourceID;
  sint32 PackageStatus;
  sint32 RequiresReinstall;
  string Users;
  sint32 IsProvisioned;
};
```

## <a name="members"></a>Membres

La **classe \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03 de MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** possède ces propriétés.

<dl> <dt>

[Architecture](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-architecture)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[InstallDate](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installdate)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[InstallLocation](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installlocation)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent. Pour cette classe, la chaîne est l’instance du nom complet du package.

</dd> <dt>

[IsBundle](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isbundle)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[IsFramework](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isframework)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[IsProvisioned](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isprovisioned)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Nom](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-name)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[PackageStatus](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-packagestatus)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/msft/EnterpriseModernAppManagement/AppManagement/*EnterpriseID* / *PackageFamilyName*»

</dd> <dt>

[Publisher](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-publisher)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[RequiresReinstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-requiresreinstall)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[ResourceID](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-resourceid)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Utilisateurs](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-users)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Version](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-version)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

