---
title: Méthode SetEnabled de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Active ou désactive la stratégie d’autorisation d’accès aux ressources Bureau à distance (RD \ 160 ; RAP) en définissant la propriété activé.
ms.assetid: ee5830ba-36a1-4f28-a902-be5867439ada
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetEnabled
- Services Bureau à distance de la méthode SetEnabled, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode SetEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bca5b483da23f4d137731a122def1481f940a2d76711e7ba5e028b2ddb7f4ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000480"
---
# <a name="setenabled-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Méthode SetEnabled de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy

Active ou désactive la stratégie d’autorisation des ressources Bureau à distance (RD RAP) en définissant la propriété **Enabled** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Activé* \[ dans\]
</dt> <dd>

Si la **valeur est true**, le rap des services Bureau à distance est activé. Si la **valeur est false**, la valeur RD RAP est désactivée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

