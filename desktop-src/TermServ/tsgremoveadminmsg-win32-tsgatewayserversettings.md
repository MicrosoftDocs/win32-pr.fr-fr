---
title: Méthode TSGRemoveAdminMsg de la classe Win32_TSGatewayServerSettings
description: Supprime le message d’administration pour le serveur de passerelle. | Méthode TSGRemoveAdminMsg de la classe Win32_TSGatewayServerSettings
ms.assetid: 36b157de-80ee-46f8-9803-5012cf1d6f5f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode TSGRemoveAdminMsg
- Services Bureau à distance de la méthode TSGRemoveAdminMsg, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode TSGRemoveAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba9877b9e8704c92eb482876ab69107e116207b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538301"
---
# <a name="tsgremoveadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode TSGRemoveAdminMsg de la \_ classe Win32 TSGatewayServerSettings

Supprime le message d’administration pour le serveur de passerelle.

## <a name="syntax"></a>Syntaxe


```mof
uint32 TSGRemoveAdminMsg();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                        |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

