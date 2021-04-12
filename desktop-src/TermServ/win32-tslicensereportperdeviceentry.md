---
title: Classe Win32_TSLicenseReportPerDeviceEntry
description: Fournit des détails sur la licence d’accès client par périphérique Services Bureau à distance par périphérique (RDS \ 160 ; Licence d’accès client par périphérique).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportPerDeviceEntry de la classe Services Bureau à distance
- Win32_TSLicenseReportPerDeviceEntry de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a120d477ff03675f160d94f1506f59cdf1462fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464471"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a>\_Classe TSLicenseReportPerDeviceEntry Win32

Fournit des détails sur la licence d’accès client par périphérique (CAL par périphérique) qui a échoué Services Bureau à distance.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSLicenseReportPerDeviceEntry** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSLicenseReportPerDeviceEntry** a ces propriétés.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type de licence d’accès client émise. Il s’agit de l’une des valeurs suivantes.

« CAL TS par périphérique » intégrée

« CAL TS par périphérique »

« CAL du connecteur Internet TS »

« CAL TS par utilisateur »

Licence d’accès client « TS ou RDS par périphérique »

Licence d’accès client TS ou RDS par utilisateur

« Licence d’abonnement VDI standard suite par périphérique »

« Licence d’abonnement VDI Premium suite par appareil »

« SERVICES CAL par périphérique »

« Licences d’accès client des services Bureau à distance par utilisateur »

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date d’expiration de la licence.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version de Services Bureau à distance pour laquelle la licence d’accès client des services Bureau à distance a été émise. Il s’agit de l’une des valeurs suivantes.

<dt>

« Windows Server 2012 »
</dt> <dd>

Seuls les serveurs exécutant Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.

</dd> <dt>

« Windows Server 7 »
</dt> <dd>

Seuls les serveurs exécutant Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.

</dd> <dt>

« Windows Server 2008 »
</dt> <dd>

Seuls les serveurs exécutant Windows Server 2008 sont pris en charge avec cette licence.

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

**sHardwareId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificateur matériel de l’ordinateur.

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’ordinateur pour lequel l’émission de la licence a été tentée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                            |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

