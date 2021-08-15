---
title: Méthode FetchReportSummaryEntries de la classe Win32_TSLicenseReport
description: Récupère des résumés de Services Bureau à distance licences d’accès client par utilisateur (RDS \ 160 ; Licences d’accès client par utilisateur) à partir du rapport.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FetchReportSummaryEntries
- Services Bureau à distance de la méthode FetchReportSummaryEntries, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode FetchReportSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094d7fe1f7aa3d5acabce7d7d248c16601b5005d09f2583cc23c7390c3642361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348574"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a>Méthode FetchReportSummaryEntries de la \_ classe Win32 TSLicenseReport

Récupère des résumés de Services Bureau à distance licences d’accès client par utilisateur (licences d’accès client aux services Bureau à distance par utilisateur) à partir du rapport.

## <a name="syntax"></a>Syntaxe


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartIndex* \[ dans\]
</dt> <dd>

Index de la première entrée de rapport à recevoir. La première entrée de rapport a un index de zéro.

</dd> <dt>

*Nombre* \[ in, out\]
</dt> <dd>

Nombre d’entrées de rapport à récupérer de l’objet de rapport. La valeur zéro indique que toutes les entrées de rapport à partir de *startIndex* doivent être récupérées. Au retour, contient le nombre d’entrées dans le tableau *ReportSummaryEntries* .

</dd> <dt>

*ReportSummaryEntries* \[ à\]
</dt> <dd>

Retourne un tableau de [**classes \_ TSLicenseReportSummaryEntry Win32**](win32-tslicensereportsummaryentry.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. La valeur **lserver je n’y a \_ \_ plus de \_ \_ données** (0x4001) indique qu’il n’y a plus d’entrées de rapport.

## <a name="remarks"></a>Remarques

Il ne s’agit pas d’une méthode statique. Cette méthode doit être appelée à partir d’un objet de rapport d’utilisation de licence par utilisateur.

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

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

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportSummaryEntry Win32**](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

