---
title: Méthode FetchReportFailedPerUserEntries de la classe Win32_TSLicenseReport
description: Récupère les détails des licences d’accès client en échec Services Bureau à distance par utilisateur (RDS \ 160 ; Licences d’accès client par utilisateur) à partir du rapport.
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FetchReportFailedPerUserEntries
- Services Bureau à distance de la méthode FetchReportFailedPerUserEntries, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode FetchReportFailedPerUserEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce4d78ff13ff58f7e80c1f177728ded24dc98588b0a0fb25c3976e9dcc19fdc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737629"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a>Méthode FetchReportFailedPerUserEntries de la \_ classe Win32 TSLicenseReport

Récupère les détails des licences d’accès client en échec Services Bureau à distance par utilisateur (RDS par utilisateur Cal par utilisateur) à partir du rapport.

## <a name="syntax"></a>Syntaxe


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartIndex* \[ dans\]
</dt> <dd>

Index de la première entrée de rapport à récupérer. La première entrée de rapport a un index de zéro.

</dd> <dt>

*Nombre* \[ in, out\]
</dt> <dd>

Nombre d’entrées de rapport à récupérer de l’objet de rapport. La valeur zéro indique que toutes les entrées de rapport à partir de *startIndex* doivent être récupérées. Au retour, contient le nombre d’entrées dans le tableau *ReportFailedPerUserEntries* .

</dd> <dt>

*ReportFailedPerUserEntries* \[ à\]
</dt> <dd>

Tableau de classes [**\_ TSLicenseReportFailedPerUserEntry Win32**](win32-tslicensereportfailedperuserentry.md) qui représentent les entrées de licence récupérées. Le paramètre *Count* contient le nombre d’éléments de ce tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

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

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> </dl>

 

 





