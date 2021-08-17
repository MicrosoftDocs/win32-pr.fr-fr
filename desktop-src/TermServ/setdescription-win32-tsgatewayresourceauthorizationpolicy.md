---
title: Méthode SetDescription de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Définit la propriété Description pour la stratégie d’autorisation d’accès aux ressources Bureau à distance (RD \ 160 ; RAP).
ms.assetid: 5a0f4c4b-50a4-4bd2-960f-8af7f4686d07
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetDescription
- Services Bureau à distance de la méthode SetDescription, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode SetDescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3380f1d38f28aac2821cc969f96ef60974c1336e77c108e31498c4c33198a705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137982"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Méthode SetDescription de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy

Définit la propriété **Description** de la stratégie d’autorisation des ressources Bureau À distance (RD RAP).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Description* \[ dans\]
</dt> <dd>

Description de la RD RAP.

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

 

