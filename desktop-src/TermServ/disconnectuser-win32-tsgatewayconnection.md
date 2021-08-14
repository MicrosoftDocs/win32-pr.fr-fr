---
title: Méthode DisconnectUser de la classe Win32_TSGatewayConnection (Tsgauthenticationengine. h)
description: Déconnecte toutes les connexions de l’utilisateur spécifié du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DisconnectUser
- Services Bureau à distance de la méthode DisconnectUser, classe Win32_TSGatewayConnection
- Win32_TSGatewayConnection de la classe Services Bureau à distance, méthode DisconnectUser
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d31c7c89d285aed576024c551b07766a7387938762d60c252dec43e491037e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130994"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a>Méthode DisconnectUser de la \_ classe Win32 TSGatewayConnection

Déconnecte toutes les connexions de l’utilisateur spécifié du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).

## <a name="syntax"></a>Syntaxe


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom d’utilisateur* \[ dans\]
</dt> <dd>

Nom d’utilisateur, au format * domaine * **\\** _nom d'_ utilisateur, dont les connexions doivent être déconnectées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                       |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Tsgauthenticationengine. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl>             |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

