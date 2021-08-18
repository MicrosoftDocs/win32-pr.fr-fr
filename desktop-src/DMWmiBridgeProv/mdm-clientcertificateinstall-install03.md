---
title: Classe MDM_ClientCertificateInstall_Install03
description: La \_ classe ClientCertificateInstall \_ Install03 MDM permet à l’entreprise de définir l’installation des certificats clients.
ms.assetid: 0083e54c-e621-47da-a20d-17c8bbf7dd3a
keywords:
- Classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, Description
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03
- MDM_ClientCertificateInstall_Install03.InstanceID
- MDM_ClientCertificateInstall_Install03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d013341f7afd20f71bc939617e551cb018dbeaa96d5f140b37de99ea79843f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077333"
---
# <a name="mdm_clientcertificateinstall_install03-class"></a>\_ \_ Classe INSTALL03 ClientCertificateInstall MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ ClientCertificateInstall \_ Install03 MDM** permet à l’entreprise de définir l’installation des certificats clients. Obligatoire pour l’inscription de certificats SCEP. Nœud parent pour grouper le certificat SCEP demande d’installation associée.

> [!Note]  
> Bien que les nœuds enfants sous install prennent en charge les commandes de remplacement, après l’envoi de la commande exec à l’appareil, ce dernier prend les valeurs définies lorsque la commande exec est acceptée. Le serveur ne doit pas s’attendre à ce que la valeur du nœud change après que la commande exec a été acceptée aura un impact sur l’inscription actuelle. Le serveur doit vérifier la valeur du nœud État et vérifier que l’appareil n’est pas à l’étape inconnue avant de modifier les valeurs du nœud enfant.

 

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_Install03
{
  string InstanceID;
  string ParentID;
  string ServerURL;
  string Challenge;
  string EKUMapping;
  sint32 KeyUsage;
  string SubjectName;
  sint32 KeyProtection;
  sint32 RetryDelay;
  sint32 RetryCount;
  string TemplateName;
  sint32 KeyLength;
  string HashAlgorithm;
  string CAThumbprint;
  string SubjectAlternativeNames;
  string ValidPeriod;
  sint32 ValidPeriodUnits;
  string ContainerName;
  string CustomTextToShowInPrompt;
  string AADKeyIdentifierList;
};
```

## <a name="members"></a>Membres

La **classe \_ ClientCertificateInstall \_ Install03 MDM** contient les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La **classe \_ ClientCertificateInstall \_ Install03 MDM** possède ces méthodes.



| Méthode                                                                      | Description                                                                   |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**EnrollMethod**](mdm-clientcertificateinstall-install03-enrollmethod.md) | Obligatoire. Déclenche le démarrage de l’inscription de certificat par l’appareil.<br/> |



 

### <a name="properties"></a>Propriétés

La **classe \_ ClientCertificateInstall \_ Install03 MDM** a ces propriétés.

<dl> <dt>

[AADKeyIdentifierList](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-aadkeyidentifierlist)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[CAThumbprint](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-cathumbprint)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Problème](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-challenge)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[ContainerName](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[CustomTextToShowInPrompt](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-customtexttoshowinprompt)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[EKUMapping](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-ekumapping)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[HashAlgorithm](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-hashalgorithm)
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

Obligatoire pour l’inscription de certificats SCEP. Nœud parent pour grouper le certificat SCEP demande d’installation associée.

Le format est node.

</dd> <dt>

[KeyLength](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keylength)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Keyprotection](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keyprotection)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Utilisation](/windows/client-management/mdm/clientcertificateinstall-csp)
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

Décrit le chemin d’accès complet au nœud parent.

La chaîne est « ./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*».

</dd> <dt>

[RetryCount](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrycount)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[RetryDelay](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrydelay)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[ServerURL](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-serverurl)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[SubjectAlternativeNames](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectalternativenames)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[SubjectName](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectname)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[TemplateName](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-templatename)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[ValidPeriod](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiod)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[ValidPeriodUnits](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiodunits)
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

 

