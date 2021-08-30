---
title: Méthode SetSslBridging de la classe Win32_TSGatewayServerSettings
description: Définit le type de pontage SSL à utiliser par le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSslBridging
- Services Bureau à distance de la méthode SetSslBridging, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetSslBridging
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b383c97bf58669a9365e7c0ce96156b80af314997d4c9c380e34bd47f7c76d03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987529"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode SetSslBridging de la \_ classe Win32 TSGatewayServerSettings

Définit le type de pontage SSL à utiliser par le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance). Cette valeur est stockée dans la propriété **SslBridging** .

> [!IMPORTANT]
> Lorsque le type de pontage SSL est modifié avec cette méthode, le service de passerelle des services Bureau à distance doit être redémarré pour que cette modification prenne effet.

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SslBridging* \[ dans\]
</dt> <dd>

Type : **UInt32**

Spécifie la nouvelle valeur de pontage SSL. Il peut s’agir de l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Aucun pontage SSL.

</dd> <dt>

1
</dt> <dd>

Pontage HTTPs vers HTTP.

</dd> <dt>

2
</dt> <dd>

Pontage HTTPs vers HTTPs.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

