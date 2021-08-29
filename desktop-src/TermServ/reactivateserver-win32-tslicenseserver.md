---
title: Méthode ReactivateServer de la classe Win32_TSLicenseServer
description: Réactive le serveur de licences Bureau à distance à l’aide d’un nouvel identificateur qui a été obtenu sur le téléphone ou sur Internet.
ms.assetid: dd9ff938-a683-4f60-b7cc-7580892953b6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReactivateServer
- Services Bureau à distance de la méthode ReactivateServer, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode ReactivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af8f9a886e40968cc5393512d29e7a90f3cfc8815725eea780abda8bd7872328
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988799"
---
# <a name="reactivateserver-method-of-the-win32_tslicenseserver-class"></a>Méthode ReactivateServer de la \_ classe Win32 TSLicenseServer

Réactive le serveur de licences Bureau à distance à l’aide d’un nouvel identificateur qui a été obtenu sur le téléphone ou sur Internet.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ReactivateServer(
  [in]  string sNewLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sNewLicenseServerId* \[ dans\]
</dt> <dd>

Bureau à distance ID du serveur de licences qui a été obtenu sur le téléphone ou sur Internet.

</dd> <dt>

*ActivationStatus* \[ à\]
</dt> <dd>

L’état d’activation renvoyé peut être l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Le serveur de licences Bureau à distance est activé.

</dd> <dt>

1
</dt> <dd>

Le serveur de licences Bureau à distance n’est pas activé.

</dd> <dt>

2
</dt> <dd>

Une erreur inconnue s'est produite. Vous ne savez pas si le serveur de licences Bureau à distance est activé.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

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

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

