---
title: Classe Win32_TSLicenseServer
description: Fournit des méthodes et des propriétés permettant d’afficher et de configurer des licences Bureau à distance (licences des services Bureau à distance) sur un serveur de licences Bureau à distance.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer de la classe Services Bureau à distance
- Win32_TSLicenseServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193416"
---
# <a name="win32_tslicenseserver-class"></a>\_Classe TSLicenseServer Win32

Fournit des méthodes et des propriétés permettant d’afficher et de configurer des licences Bureau à distance (licences des services Bureau à distance) sur un serveur de licences Bureau à distance.

## <a name="syntax"></a>Syntaxe

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSLicenseServer** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSLicenseServer** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateServer**](activateserver-win32-tslicenseserver.md)                           | Active le serveur de licences Bureau à distance à l’aide d’un ID de serveur de licences Bureau à distance qui est obtenu sur le téléphone ou sur Internet.<br/>                                                                                           |
| [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)         | Active automatiquement le serveur de licences Bureau à distance via Internet. Les propriétés **FirstName**, **LastName**, **Company** et **PaysRégion** ne doivent pas être vides lorsque cette méthode est appelée, sinon la méthode échoue.<br/> |
| [**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)                       | Ajoute le Bureau à distance serveur de licences au groupe serveurs de licences Bureau à distance sur un contrôleur de domaine dans le même domaine que le serveur de licences.<br/>                                                                                |
| [**ChangeRole**](changerole-win32-tslicenseserver.md)                                   | Modifie l’étendue de la découverte du serveur de licences Bureau à distance.<br/>                                                                                                                                                                  |
| [**CreateTSCGroup**](createtscgroup-win32-tslicenseserver.md)                           | Cette méthode n'est pas prise en charge.<br/> **Windows server 2008 R2 et Windows server 2008 :** Crée le groupe local ordinateurs Terminal Server sur le serveur de licences Bureau à distance.<br/>                                               |
| [**DeactivateServer**](deactivateserver-win32-tslicenseserver.md)                       | Désactive le serveur de licences Bureau à distance à l’aide d’un code de confirmation reçu sur le téléphone.<br/>                                                                                                                        |
| [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md)     | Désactive le serveur de licences Bureau à distance sur Internet. Les propriétés **FirstName** et **LastName** ne doivent pas être vides lorsque cette méthode est appelée, sinon la méthode échoue.<br/>                                              |
| [**GetActivationStatus**](getactivationstatus-win32-tslicenseserver.md)                 | Récupère l’état d’activation actuel.<br/>                                                                                                                                                                                           |
| [**GetLicenseServerId**](getlicenseserverid-win32-tslicenseserver.md)                   | Récupère un Bureau à distance ID du serveur de licences si le serveur est actuellement activé.<br/>                                                                                                                                                 |
| [**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)                         | Récupère si le Bureau à distance serveur de licences est membre du groupe serveurs de licences Bureau à distance sur un contrôleur de domaine dans un domaine donné.<br/>                                                                              |
| [**IsLSonDC**](islsondc-win32-tslicenseserver.md)                                       | Récupère si le gestionnaire de licences des services Bureau à distance est installé sur un contrôleur de domaine.<br/>                                                                                                                                                                |
| [**IsLSPreventUpgradeGPEnabled**](islspreventupgradegpenabled-win32-tslicenseserver.md) | Récupère si le paramètre de stratégie de groupe « empêcher la mise à niveau de licence » est activé sur le serveur de licences Bureau à distance.<br/>                                                                                                              |
| [**IsLSPublished**](islspublished-win32-tslicenseserver.md)                             | Récupère si le serveur de licences Bureau à distance est publié dans Active Directory Domain Services (AD DS).<br/>                                                                                                                      |
| [**IsLSRegisteredToSCP**](win32-tslicenseserver-islsregisteredtoscp.md)                 | Récupère si le serveur de licences Bureau à distance est inscrit en tant que point de connexion de service dans Active Directory Domain Services.<br/>                                                                                               |
| [**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)                 | Récupère si le paramètre de stratégie de groupe « Groupe de sécurité du serveur de licences » est activé sur le serveur de licences Bureau à distance.<br/>                                                                                                        |
| [**IsSecureAccessAllowed**](issecureaccessallowed-win32-tslicenseserver.md)             | Récupère une valeur indiquant si un serveur hôte de session Bureau à distance est autorisé à demander Services Bureau à distance licences d’accès client (CAL RDS) à partir du serveur de licences Bureau à distance.<br/>                                                                |
| [**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)                     | Cette méthode n'est pas prise en charge.<br/> **Windows server 2008 R2 et Windows server 2008 :** Récupère si le groupe local ordinateurs Terminal Server existe sur le serveur de licences Bureau à distance.<br/>                              |
| [**IsTSinTSCGroup**](istsintscgroup-win32-tslicenseserver.md)                           | Récupère une valeur qui détermine si un serveur hôte de session Bureau à distance est membre du groupe local ordinateurs Terminal Server sur le serveur de licences Bureau à distance.<br/>                                                                                         |
| [**PublishLS**](publishls-win32-tslicenseserver.md)                                     | Publie le serveur de licences Bureau à distance dans AD DS.<br/>                                                                                                                                                                              |
| [**ReactivateServer**](reactivateserver-win32-tslicenseserver.md)                       | Réactive le serveur de licences Bureau à distance à l’aide d’un nouvel ID de serveur de licences Bureau à distance qui est obtenu sur le téléphone ou sur Internet.<br/>                                                                                     |
| [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)     | Réactive le serveur de licences Bureau à distance via Internet. Les propriétés **FirstName** et **LastName** ne doivent pas être vides lorsque cette méthode est appelée, sinon la méthode échoue.<br/>                                              |
| [**RegisterLSToSCP**](win32-tslicenseserver-registerlstoscp.md)                         | Inscrit le serveur de licences Bureau à distance en tant que point de connexion de service dans Active Directory Domain Services.<br/>                                                                                                                     |
| [**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)             | Supprime le Bureau à distance serveur de licences du groupe serveurs de licences Bureau à distance sur un contrôleur de domaine dans le même domaine que le serveur de licences.<br/>                                                                           |
| [**RemoveTSCGroup**](removetscgroup-win32-tslicenseserver.md)                           | Cette méthode n'est pas prise en charge.<br/> **Windows server 2008 R2 et Windows server 2008 :** Supprime le Terminal Server groupe local ordinateurs du serveur de licences Bureau à distance.<br/>                                             |
| [**UnpublishLS**](unpublishls-win32-tslicenseserver.md)                                 | Annule la publication d’un serveur de licences Bureau à distance à partir de AD DS.<br/>                                                                                                                                                                            |
| [**UnRegisterLSFromSCP**](win32-tslicenseserver-unregisterlsfromscp.md)                 | Supprime le serveur de licences Bureau à distance comme point de connexion de service dans Active Directory Domain Services.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSLicenseServer** a ces propriétés.

<dl> <dt>

**Adresse**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Adresse du contact pour le gestionnaire de licences des services Bureau à distance. Cette propriété est utilisée lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée. (Cette propriété est facultative lors de l’utilisation de la méthode **ActivateServerAutomatic** .)

</dd> <dt>

**Ville**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Ville du contact pour les licences des services Bureau à distance. Cette propriété est utilisée lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée. (Cette propriété est facultative lors de l’utilisation de la méthode **ActivateServerAutomatic** .)

</dd> <dt>

**Société**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Société du contact pour les licences des services Bureau à distance. Cette propriété est utilisée (et obligatoire) lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée.

</dd> <dt>

**Pays**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pays/région du contact pour les licences des services Bureau à distance. Cette propriété est utilisée (et obligatoire) lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée.

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès de la base de données des licences des services Bureau à distance.

</dd> <dt>

**Messagerie**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Adresse de messagerie du contact pour les licences des services Bureau à distance. Cette propriété est utilisée lorsque les méthodes [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) sont appelées. (Cette propriété est facultative pour ces appels de méthode.)

</dd> <dt>

**FirstName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Prénom du contact pour les licences des services Bureau à distance. Cette propriété est utilisée (et obligatoire) lorsque les méthodes [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) sont appelées.

</dd> <dt>

**LastName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom du contact pour le gestionnaire de licences des services Bureau à distance. Cette propriété est utilisée (et obligatoire) lorsque les méthodes [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) sont appelées.

</dd> <dt>

**OrgUnit**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Unité d’organisation du contact pour les licences des services Bureau à distance. Cette propriété est utilisée lorsque le [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelé. (Cette propriété est facultative lors de l’utilisation de la méthode **ActivateServerAutomatic** .)

</dd> <dt>

**PostalCode**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Code postal du contact pour les licences des services Bureau à distance. Cette propriété est utilisée lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée. (Cette propriété est facultative lors de l’utilisation de la méthode **ActivateServerAutomatic** .)

</dd> <dt>

**ProductId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

ID de produit du serveur de licences Bureau à distance.

</dd> <dt>

**ServerRole**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décrit l’étendue de la gestion de licences pour le Bureau à distance serveur de licences au sein de l’organisation.

<dt>

0
</dt> <dd>

Les serveurs hôtes de session Bureau à distance dans le même groupe de travail peuvent découvrir le serveur de licences.

</dd> <dt>

1
</dt> <dd>

Les serveurs hôtes de session Bureau à distance dans le même domaine peuvent découvrir le serveur de licences.

</dd> <dt>

2
</dt> <dd>

Les serveurs hôtes de session Bureau à distance de plusieurs domaines de la même forêt peuvent découvrir le serveur de licences.

</dd> </dl>

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

État du contact pour le gestionnaire de licences des services Bureau à distance. Cette propriété est utilisée lorsque la méthode [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) est appelée. (Cette propriété est facultative lors de l’utilisation de la méthode **ActivateServerAutomatic** .)

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version du serveur de licences Bureau à distance.

</dd> <dt>

**VersionNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de version du serveur de licences Bureau à distance.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette classe est une classe [Singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) et ne peut avoir qu’une seule instance. Toutes les méthodes contenues dans cette classe sont statiques.

Pour utiliser cette classe, vous devez être membre du groupe administrateurs. Si l’appelant n’est pas membre du groupe administrateurs, les propriétés retournées sont vides.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> </dl>

 

