---
title: Classe Win32_TSLicenseKeyPack
description: Fournit des méthodes et des propriétés pour l’affichage et l’installation de Services Bureau à distance les jeux de clés de licence.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7927270f262d0a66722660bf4b2c8f15cf75f49bb807abcff604af9edf58d99b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137812"
---
# <a name="win32_tslicensekeypack-class"></a>\_Classe TSLicenseKeyPack Win32

Fournit des méthodes et des propriétés pour l’affichage et l’installation de Services Bureau à distance les jeux de clés de licence.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSLicenseKeyPack** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSLicenseKeyPack** possède ces méthodes.



| Méthode                                                                                                        | Description                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertLicenses**](convertlicenses-win32-tslicensekeypack.md)                                             | Convertit les licences dans le jeu de clés actuel.<br/>                                                                                                                                                                                 |
| [**ImportAgreementLicenseKeyPack**](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | Les importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.<br/> |
| [**ImportLicenseKeyPackOffline**](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance qui utilise un identificateur de licence reçu via Internet ou le téléphone.<br/>                                               |
| [**ImportOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Open License Services Bureau à distance.<br/>                                                                                                                 |
| [**ImportRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.<br/>                                                                                   |
| [**InstallAgreementLicenseKeyPack**](installagreementlicensekeypack-win32-tslicensekeypack.md)               | Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’une licence de contrat.<br/>                                                                                                                           |
| [**InstallLicenseKeyPack**](installlicensekeypack-win32-tslicensekeypack.md)                                 | Installe un jeu de clés de licence Services Bureau à distance qui utilise un ID de jeu de clés de licence reçu via Internet ou par téléphone.<br/>                                                                                          |
| [**InstallOpenLicenseKeyPack**](installopenlicensekeypack-win32-tslicensekeypack.md)                         | Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence ouvert.<br/>                                                                                                                      |
| [**InstallRetailPurchaseLicenseKeyPack**](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un magasin de vente au détail.<br/>                                                                                                                                 |
| [**ReinstallAgreementLicenseKeyPack**](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.<br/>                                           |
| [**ReinstallLicenseKeyPackOffline**](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | Réinstalle un jeu de clés de licence Services Bureau à distance qui utilise l’identificateur de licence reçu sur Internet ou sur le téléphone.<br/>                                                                                       |
| [**ReinstallOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | Réinstalle un jeu de clés de licence Open License Services Bureau à distance.<br/>                                                                                                                                                           |
| [**ReinstallRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.<br/>                                                                                                                             |
| [**RemoveLicensesWithIdCount**](win32-tslicensekeypack-removelicenseswithidcount.md)                         | Supprime le nombre spécifié de licences Services Bureau à distance du jeu de clés spécifié.<br/>                                                                                                                                  |
| [**UninstallLicenseKeyPack**](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | Désinstalle un jeu de clés de licence Services Bureau à distance.<br/>                                                                                                                                                                         |
| [**UninstallLicenseKeyPackWithId**](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | Désinstalle le jeu de clés de licence Services Bureau à distance avec l’identificateur de package de clés spécifié.<br/>                                                                                                                                |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSLicenseKeyPack** a ces propriétés.

<dl> <dt>

**AccessRights**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) (« 0 », « 1 », « 2 », « 3 »), [**bitvalues**](/windows/desktop/WmiSdk/standard-qualifiers) (« session Rd », « session VDI », « Calista », « partenaires VDI »)
</dt> </dl>

Qualificateur pour les droits d’accès au Pack de clés du gestionnaire de licences TS

</dd> <dt>

**AvailableLicenses**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total de licences disponibles dans le jeu de clés de licence Services Bureau à distance.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description du jeu de clés de licence Services Bureau à distance.

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Type de données : **[DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date d’expiration du jeu de clés de licence Services Bureau à distance.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total de licences émises dans le jeu de clés de licence Services Bureau à distance.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificateur du jeu de clés de licence Services Bureau à distance.

</dd> <dt>

**KeyPackType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de jeu de clés pour le serveur de licences Bureau à distance.

| Valeur | Description |
|-------|-------------|
| 0 | Le type de jeu de clés de licence Services Bureau à distance est inconnu. |
| 1 | Le type de jeu de clés de licence Services Bureau à distance est un achat au détail. |
| 2 | Le type de jeu de clés de licence Services Bureau à distance est un achat en volume. |
| 3 | Le type de jeu de clés de licence Services Bureau à distance est une licence simultanée. |
| 4 | Le type de jeu de clés de licence Services Bureau à distance est temporaire. |
| 5 | Le type de jeu de clés de licence Services Bureau à distance est une licence ouverte. |
| 6 | Non pris en charge. |

**ProductType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de produit du jeu de clés de licence Services Bureau à distance.

| Valeur | Description |
|-------|-------------|
| 0 | Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique. Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence. |
| 1 | Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur. Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence. |
| 2 | Ce type de produit n’est pas valide. |

**ProductVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version du produit pour le jeu de clés de licence Services Bureau à distance.

| Valeur | Description |
|-------|-------------|
| « Windows Server 2012 » | seuls les serveurs exécutant Windows Server 2012, Windows server 2008 R2 ou Windows server 2008 sont pris en charge avec cette licence. |
| « Windows Server 7 » | seuls les serveurs exécutant Windows server 2008 R2 ou Windows server 2008 sont pris en charge avec cette licence. |
| « Windows Server 2008 » | seuls les serveurs exécutant Windows Server 2008 sont pris en charge par ce pack de clés. |

**ProductVersionID**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur de la version du produit pour le Services Bureau à distance le jeu de clés de licence.

| Valeur | Description |
|-------|-------------|
| 0 | Non pris en charge |
| 1 | Non pris en charge |
| 2 | Windows Server 2008 |
| 3 | Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

**TotalLicenses**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total de licences dans le jeu de clés de licence Services Bureau à distance.

</dd> <dt>

**TypeAndModel**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Qualificateur pour le type et le modèle de jeu de clés du gestionnaire de licences TS. Exemples : licence d’abonnement VDI par appareil, CAL TS par utilisateur

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour utiliser cette classe, vous devez être membre du groupe administrateurs.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



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

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

