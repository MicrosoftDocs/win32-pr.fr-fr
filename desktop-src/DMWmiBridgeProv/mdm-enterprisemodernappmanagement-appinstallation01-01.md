---
title: Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: la \_ classe MDM EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 est utilisée pour installer des applications à partir du magasin de Windows ou d’un emplacement hébergé.
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d29cde4408cac13471e98d0c42b36779f8b23c0101f6ba22f383d97e181893e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875339"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>\_Classe EnterpriseModernAppManagement \_ APPINSTALLATION01 \_ 01 MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

la classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** est utilisée pour installer des applications à partir du magasin de Windows ou d’un emplacement hébergé.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a>Membres

La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** possède ces méthodes.



| Méthode                                                                                                    | Description                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**HostedInstallMethod**](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | Méthode permettant d’effectuer l’installation d’un package d’application à partir d’un emplacement hébergé (il peut s’agir d’un lecteur local, d’une source de données UNC ou https).<br/> |
| [**StoreInstallMethod**](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | méthode permettant d’effectuer l’installation d’une application et d’une licence à partir du magasin de Windows.<br/>                                                    |



 

### <a name="properties"></a>Propriétés

La classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** possède ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « AppInstallation ».

</dd> <dt>

[LastError](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[LastErrorDesc](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
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

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation »

</dd> <dt>

[ProgressStatus](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[État](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
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

 

