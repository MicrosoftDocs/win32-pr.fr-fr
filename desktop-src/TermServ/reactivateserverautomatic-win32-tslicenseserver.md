---
title: Méthode ReactivateServerAutomatic de la classe Win32_TSLicenseServer
description: Réactive le serveur de licences Bureau à distance à l’aide d’une connexion automatique à Internet.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReactivateServerAutomatic
- Services Bureau à distance de la méthode ReactivateServerAutomatic, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode ReactivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e822c441410ae3757f7cdb0a4a714b435facbb20e171646c889e2ea53ec82b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866039"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Méthode ReactivateServerAutomatic de la \_ classe Win32 TSLicenseServer

Réactive le serveur de licences Bureau à distance à l’aide d’une connexion automatique à Internet.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Raison* \[ dans\]
</dt> <dd>

Raison de l’activation. Il peut avoir l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Le serveur a été redéployé.

</dd> <dt>

1
</dt> <dd>

Le certificat est endommagé.

</dd> <dt>

2
</dt> <dd>

La clé privée a été compromise.

</dd> <dt>

3
</dt> <dd>

La clé d’activation a expiré.

</dd> <dt>

4
</dt> <dd>

Le serveur a été mis à niveau.

</dd> </dl> </dd> <dt>

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

 

