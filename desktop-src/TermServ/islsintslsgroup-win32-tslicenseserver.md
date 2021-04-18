---
title: Méthode IsLSinTSLSGroup de la classe Win32_TSLicenseServer
description: Récupère si le Bureau à distance serveur de licences est membre du groupe de serveurs de licences Bureau à distance sur un contrôleur de domaine dans un domaine donné.
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLSinTSLSGroup
- Services Bureau à distance de la méthode IsLSinTSLSGroup, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsLSinTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511952"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a>Méthode IsLSinTSLSGroup de la \_ classe Win32 TSLicenseServer

Récupère si le Bureau à distance serveur de licences est membre du groupe de serveurs de licences Bureau à distance sur un contrôleur de domaine dans un domaine donné.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Domaine* \[ dans\]
</dt> <dd>

Nom du domaine.

</dd> <dt>

*IsMember* \[ à\]
</dt> <dd>

Valeur booléenne qui indique si le serveur de licences est membre du groupe de serveurs de licences Bureau à distance dans le domaine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Si aucun nom de domaine n’est fourni, un contrôleur de domaine dans le même domaine que le serveur de licences est interrogé.

Le serveur de licences doit être membre du groupe de serveurs de licences Bureau à distance si le serveur est configuré pour utiliser l’étendue de la découverte du domaine ou de la forêt. Si le serveur de licences n’est pas membre de ce groupe, le suivi des licences par utilisateur et la création de rapports ne fonctionneront pas.

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

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> <dt>

[**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

