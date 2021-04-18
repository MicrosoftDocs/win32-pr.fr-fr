---
title: Méthode FetchReportEntries de la classe Win32_TSLicenseReport
description: Récupère les détails de Services Bureau à distance licences d’accès client par utilisateur (RDS \ 160 ; Licences d’accès client par utilisateur) à partir du rapport. Chaque entrée représente un objet RDS \ 160 ; Licence d’accès client par utilisateur en cours d’utilisation.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FetchReportEntries
- Services Bureau à distance de la méthode FetchReportEntries, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode FetchReportEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc64c9591444307ba0519da02cf9c6f13d20252e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509289"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a>Méthode FetchReportEntries de la \_ classe Win32 TSLicenseReport

Récupère les détails de Services Bureau à distance licences d’accès client par utilisateur (licences d’accès client aux services Bureau à distance par utilisateur) à partir du rapport. Chaque entrée représente une licence d’accès client des services Bureau à distance par utilisateur en cours d’utilisation.

## <a name="syntax"></a>Syntaxe


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
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

Nombre d’entrées de rapport à récupérer de l’objet de rapport. La valeur zéro indique que toutes les entrées de rapport à partir de *startIndex* doivent être récupérées. Au retour, contient le nombre d’entrées dans le tableau *ReportEntries* .

</dd> <dt>

*ReportEntries* \[ à\]
</dt> <dd>

Retourne un tableau de [**classes \_ TSLicenseReportEntry Win32**](win32-tslicensereportentry.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. La valeur **lserver je n’y a \_ \_ plus de \_ \_ données** (0x4001) indique qu’il n’y a plus d’entrées de rapport.

## <a name="remarks"></a>Notes

Il ne s’agit pas d’une méthode statique. Cette méthode doit être appelée à partir d’un objet de rapport d’utilisation de licence par utilisateur.

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

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

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> </dl>

 

