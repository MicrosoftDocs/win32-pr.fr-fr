---
title: Méthode GenerateReport de la classe Win32_TSLicenseReport (gpmgmt. h)
description: GenerateReport ne peut plus être utilisé à partir de Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GenerateReport
- Services Bureau à distance de la méthode GenerateReport, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode GenerateReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384992"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a>Méthode GenerateReport de la \_ classe Win32 TSLicenseReport

\[**GenerateReport** ne peut plus être utilisé à partir de Windows Server 2012. Utilisez plutôt [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]

Cette méthode n'est pas prise en charge.

**Windows server 2008 R2 et Windows server 2008 :** Génère un rapport d’utilisation des licences par utilisateur actuel sur le serveur de licences Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ScopeType* \[ dans\]
</dt> <dd>

Étendue du rapport d’utilisation de la licence. Il peut avoir les valeurs suivantes.

<dt>

1
</dt> <dd>

Le rapport sera généré pour l’ensemble du domaine.

</dd> <dt>

2
</dt> <dd>

Le rapport sera généré pour l’unité d’organisation (UO) spécifiée dans le paramètre *ScopeValue* .

</dd> <dt>

3
</dt> <dd>

Le rapport sera généré pour tous les domaines approuvés.

</dd> </dl> </dd> <dt>

*ScopeValue* \[ dans\]
</dt> <dd>

Si le paramètre *ScopeType* est 2, *ScopeType* spécifie l’unité d’organisation pour laquelle le rapport sera généré. Vous devez spécifier *ScopeValue* à l’aide du format **ou =**_OUName1_*_, ou =_*_OUName2_*_..._*.

</dd> <dt>

*Nom du fichier* \[ à\]
</dt> <dd>

Nom de fichier du rapport généré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **WBEM \_ E \_ non \_ pris en charge**.

**Windows server 2008 R2 et Windows server 2008 :** Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Il s’agit d’une méthode statique.

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Fin de la prise en charge des clients<br/>    | Aucun pris en charge<br/>                                                                 |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/>                                                         |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                    |
| En-tête<br/>                   | <dl> <dt>Gpmgmt. h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> </dl>

 

