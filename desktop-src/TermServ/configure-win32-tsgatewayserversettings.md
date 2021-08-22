---
title: Configurer la méthode de la classe Win32_TSGatewayServerSettings
description: Configure les paramètres IIS et RPC requis par le service de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 12d7264e-46aa-457f-b89d-547231573db8
ms.tgt_platform: multiple
keywords:
- Configurer la méthode Services Bureau à distance
- Configurez la méthode Services Bureau à distance, Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, configurer la méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.Configure
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e246b81569f63c3a6eac9cafe043c837deca593072b622efa3f854a4a74862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515689"
---
# <a name="configure-method-of-the-win32_tsgatewayserversettings-class"></a>Configurer la méthode de la \_ classe TSGatewayServerSettings Win32

Configure les paramètres IIS et RPC requis par le service de passerelle Bureau à distance (passerelle des services Bureau à distance).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Configure();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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

 

