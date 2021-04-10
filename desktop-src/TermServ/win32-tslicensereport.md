---
title: Classe Win32_TSLicenseReport
description: Fournit des instances de Services Bureau à distance licence d’accès client par utilisateur (RDS \ 160 ; Les rapports d’utilisation des licences d’accès client par utilisateur) qui sont générés sur le serveur de licences Bureau à distance, ainsi que les méthodes de génération, d’extraction et de suppression des rapports de licence.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport de la classe Services Bureau à distance
- Win32_TSLicenseReport de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843177"
---
# <a name="win32_tslicensereport-class"></a>\_Classe TSLicenseReport Win32

Fournit des instances de Services Bureau à distance les rapports d’utilisation de licence d’accès client par utilisateur (CAL par utilisateur) qui sont générés sur le serveur de licences Bureau à distance et les méthodes pour la génération de rapports de licence, les opérations d’extraction et de suppression.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSLicenseReport** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSLicenseReport** possède ces méthodes.



| Méthode                                                                                                         | Description                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | Supprime un objet de rapport sur le serveur de licences Bureau à distance. Il ne s’agit pas d’une méthode statique.<br/>                                                                                           |
| [**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)                                         | Récupère les entrées dans l’objet de rapport.<br/>                                                                                                                                              |
| [**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | Récupère les détails des licences d’accès client en échec Services Bureau à distance par utilisateur (RDS par utilisateur Cal par utilisateur) à partir du rapport.<br/>                                                             |
| [**FetchReportFailedPerUserSummaryEntries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | Récupère des informations récapitulatives de la Services Bureau à distance des licences d’accès client par utilisateur (licences d’accès client des services Bureau à distance par utilisateur) ayant échoué à partir du rapport.<br/>                                                 |
| [**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | Récupère des informations sur les licences d’accès client par périphérique Services Bureau à distance émises par périphérique (CAL par périphérique) à partir du rapport.<br/>                                                     |
| [**FetchReportSummaryEntries**](win32-tslicensereport-fetchreportsummaryentries.md)                           | Récupère des résumés de licence à partir de l’objet de rapport.<br/>                                                                                                                                  |
| [**GenerateReport**](generatereport-win32-tslicensereport.md)                                                 | Cette méthode n'est pas prise en charge.<br/> **Windows server 2008 R2 et Windows server 2008 :** Génère un rapport d’utilisation des licences par utilisateur actuel sur le serveur de licences Bureau à distance.<br/> |
| [**GenerateReportEx**](generatereportex-win32-tslicensereport.md)                                             | Génère un rapport d’utilisation des licences par utilisateur actuel sur le serveur de licences Bureau à distance.<br/>                                                                                              |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSLicenseReport** a ces propriétés.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom du rapport.

</dd> <dt>

**GenerationDateTime**
</dt> <dd> <dl> <dt>

Type de données : **[DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de génération du rapport du gestionnaire de licences des services Bureau à distance.

</dd> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Cette propriété n'est pas prise en charge.

**Windows server 2008 R2 et Windows server 2008 :** Nombre de licences d’accès client des services Bureau à distance par utilisateur installées.

</dd> <dt>

**LicenseUsageCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Cette propriété n'est pas prise en charge.

**Windows server 2008 R2 et Windows server 2008 :** Nombre de licences d’accès client aux services Bureau à distance par utilisateur en cours d’utilisation.

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Cette propriété n'est pas prise en charge.

**Windows server 2008 R2 et Windows server 2008 :** Type d’étendue du rapport de licences des services Bureau à distance.

</dd> <dt>

**ScopeValue**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Cette propriété n'est pas prise en charge.

**Windows server 2008 R2 et Windows server 2008 :** Valeur de l’étendue du rapport de licences des services Bureau à distance.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version du rapport de licences des services Bureau à distance.

</dd> </dl>

## <a name="remarks"></a>Notes

Les rapports générés à l’aide de WMI sont affichés dans le gestionnaire de licences des services Bureau à distance. Les rapports qui sont supprimés à l’aide de WMI sont également supprimés du gestionnaire de licences des services Bureau à distance.

Pour utiliser cette classe, vous devez être membre du groupe administrateurs.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

