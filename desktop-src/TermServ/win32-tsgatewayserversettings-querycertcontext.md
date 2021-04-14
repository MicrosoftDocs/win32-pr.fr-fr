---
title: Méthode QueryCertContext de la classe Win32_TSGatewayServerSettings
description: Indique si le certificat spécifié est installé.
ms.assetid: 25d56f72-befd-46b4-84ff-dca748eeaca4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode QueryCertContext
- Services Bureau à distance de la méthode QueryCertContext, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode QueryCertContext
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.QueryCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e158b348debc610682380d793b66949c5a7648
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466707"
---
# <a name="querycertcontext-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode QueryCertContext de la \_ classe Win32 TSGatewayServerSettings

Indique si le certificat spécifié est installé.

## <a name="syntax"></a>Syntaxe


```mof
uint32 QueryCertContext(
  [out] uint8 CertHash[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Certhash* \[ à\]
</dt> <dd>

Hachage du certificat utilisé par le serveur de passerelle Bureau à distance.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

