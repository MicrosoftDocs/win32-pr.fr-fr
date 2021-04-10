---
title: Méthode IsTSCGroupPresent de la classe Win32_TSLicenseServer
description: IsTSCGroupPresent ne peut plus être utilisé à partir de Windows Server 2012.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsTSCGroupPresent
- Services Bureau à distance de la méthode IsTSCGroupPresent, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsTSCGroupPresent
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16683b10bbfdd08812454d67ebc8ffc169b0ca0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032637"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a>Méthode IsTSCGroupPresent de la \_ classe Win32 TSLicenseServer

\[**IsTSCGroupPresent** ne peut plus être utilisé à partir de Windows Server 2012.\]

Cette méthode n'est pas prise en charge.

**Windows server 2008 R2 et Windows server 2008 :** Récupère si le groupe local ordinateurs Terminal Server existe sur le serveur de licences Bureau à distance.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Présent* \[ à\]
</dt> <dd>

Valeur booléenne qui indique si le groupe local ordinateurs Terminal Server existe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **WBEM \_ E \_ non \_ pris en charge**.

**Windows server 2008 R2 et Windows server 2008 :** Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

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
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

