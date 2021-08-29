---
title: Classe MDM_ClientCertificateInstall_SCEP01_01
description: La \_ classe MDM ClientCertificateInstall \_ SCEP01 \_ 01 permet d’accéder au nœud pour l’installation du certificat SCEP, en utilisant des ID uniques pour différencier les différentes demandes d’installation de certificat.
ms.assetid: 273e6ef7-fd00-4049-bb8b-b9900b3d250b
keywords:
- Classe MDM_ClientCertificateInstall_SCEP01_01
- Classe MDM_ClientCertificateInstall_SCEP01_01, Description
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_SCEP01_01
- MDM_ClientCertificateInstall_SCEP01_01.InstanceID
- MDM_ClientCertificateInstall_SCEP01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152b5867a6b93f00a0389148f72a5280ae8de1616e8338dad1a36841195cb67a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077323"
---
# <a name="mdm_clientcertificateinstall_scep01_01-class"></a>\_Classe ClientCertificateInstall \_ SCEP01 \_ 01 MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** permet d’accéder au nœud pour l’installation du certificat SCEP, en utilisant des ID uniques pour différencier les différentes demandes d’installation de certificat.

Requis pour l’installation du certificat SCEP.

Les opérations prises en charge sont les opérations d’extraction, d’ajout et de suppression.

L’appel de Delete sur le nœud This doit supprimer le certificat SCEP correspondant.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_SCEP01_01
{
  string InstanceID;
  string ParentID;
  string CertThumbprint;
  sint32 Status;
  sint32 ErrorCode;
  string RespondentServerUrl;
};
```

## <a name="members"></a>Membres

La classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** possède ces propriétés.

<dl> <dt>

[CertThumbprint](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-certthumbprint)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[ErrorCode](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-errorcode)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
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

Identifie le nom du nœud parent. Pour cette classe, ID unique permettant de différencier les différentes demandes d’installation de certificat.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent.

La chaîne est « ./Vendor/MSFT/ClientCertificateInstall/SCEP »

</dd> <dt>

[RespondentServerUrl](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-respondentserverurl)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[État](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
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

 

