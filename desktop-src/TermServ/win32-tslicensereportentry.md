---
title: Classe Win32_TSLicenseReportEntry
description: Fournit des détails sur la licence d’accès client Services Bureau à distance par utilisateur (RDS \ 160 ; CAL par utilisateur).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry de la classe Services Bureau à distance
- Win32_TSLicenseReportEntry de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e08041ac0878f3466712001a0a5e2cc90eb74ea1e360da9785b5d84805574389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126519"
---
# <a name="win32_tslicensereportentry-class"></a>\_Classe TSLicenseReportEntry Win32

Fournit des détails sur la licence d’accès client par utilisateur Services Bureau à distance émis (RDS par utilisateur).

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSLicenseReportEntry** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSLicenseReportEntry** a ces propriétés.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type de licence d’accès client émise. Il s’agit de l’une des valeurs suivantes.

**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas prise en charge.

« CAL TS par périphérique » intégrée

« CAL TS par périphérique »

« CAL du connecteur Internet TS »

« CAL TS par utilisateur »

Licence d’accès client « TS ou RDS par périphérique »

Licence d’accès client TS ou RDS par utilisateur

« Licence d’abonnement VDI standard suite par périphérique »

« licence d’abonnement VDI Premium Suite par appareil »

« SERVICES CAL par périphérique »

« Licences d’accès client des services Bureau à distance par utilisateur »

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date d’expiration de la licence émise pour l’utilisateur.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version de Services Bureau à distance pour laquelle la licence d’accès client des services Bureau à distance a été émise.

<dt>

« Windows Server 2012 »
</dt> <dd>

seuls les serveurs exécutant Windows Server 2012, Windows server 2008 R2 ou Windows server 2008 sont pris en charge avec cette licence.

</dd> <dt>

« Windows Server 7 »
</dt> <dd>

seuls les serveurs exécutant Windows server 2008 R2 ou Windows server 2008 sont pris en charge avec cette licence.

</dd> <dt>

« Windows Server 2008 »
</dt> <dd>

seuls les serveurs exécutant Windows Server 2008 sont pris en charge avec cette licence.

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur de la version du produit pour le Services Bureau à distance le jeu de clés de licence.

<dt>

4
</dt> <dd>

Windows Server 2012

</dd> <dt>

3
</dt> <dd>

Windows Server 2008 R2

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> <dt>

1
</dt> <dd>

Non pris en charge.

</dd> <dt>

0
</dt> <dd>

Non pris en charge.

</dd> </dl>

</dd> <dt>

**Utilisateur**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom de l’utilisateur pour lequel la licence a été émise.

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

[**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

