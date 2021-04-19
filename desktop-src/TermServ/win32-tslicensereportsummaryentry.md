---
title: Classe Win32_TSLicenseReportSummaryEntry
description: Fournit un résumé des Services Bureau à distance installées et émises par les licences d’accès client par utilisateur (RDS \ 160 ; Cal par utilisateur).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry de la classe Services Bureau à distance
- Win32_TSLicenseReportSummaryEntry de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511737"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>\_Classe TSLicenseReportSummaryEntry Win32

Fournit un résumé des Services Bureau à distance installées et émises par les licences d’accès client par utilisateur (licences d’accès client des services Bureau à distance par utilisateur).

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSLicenseReportSummaryEntry** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSLicenseReportSummaryEntry** a ces propriétés.

<dl> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de licences d’accès client des services Bureau à distance par utilisateur installées.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de licences d’accès client des services Bureau à distance par utilisateur émises.

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

**TSCALAvailability**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Disponibilité des licences d’accès client des services Bureau à distance par utilisateur. Il s’agit de l’une des valeurs suivantes.

<dt>

Téléchargé
</dt> <dd>

Les licences d’accès client des services Bureau à distance par utilisateur sont disponibles.

</dd> <dt>

Certaine
</dt> <dd>

La disponibilité des CAL par utilisateur des services Bureau à distance est limitée.

</dd> <dt>

"None"
</dt> <dd>

Les CAL par utilisateur des services Bureau à distance ne sont pas disponibles.

</dd> <dt>

« Pas de suivi »
</dt> <dd>

La disponibilité des licences d’accès client des services Bureau à distance par utilisateur n’est pas suivie.

</dd> </dl>

</dd> <dt>

**TSCALType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de licences d’accès client aux services Bureau à distance par utilisateur. Il s’agit de l’une des valeurs suivantes.

<dt>

« Par appareil »
</dt> <dd>

Les licences d’accès client des services Bureau à distance par utilisateur sont émises par appareil.

</dd> <dt>

« Par utilisateur »
</dt> <dd>

Les licences d’accès client des services Bureau à distance par utilisateur sont émises par utilisateur.

</dd> <dt>

Connue
</dt> <dd>

Le type de licences d’accès client aux services Bureau à distance par utilisateur est inconnu.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 





