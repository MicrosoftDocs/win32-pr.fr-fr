---
title: Méthode CheckStatus de la classe Win32_TSGatewayConnection
description: Vérifie l’état d’une connexion de serveur de passerelle Bureau à distance (passerelle Bureau à distance) à un autre ordinateur et détermine si l’ordinateur cible est configuré pour l’équilibrage de charge.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CheckStatus
- Services Bureau à distance de la méthode CheckStatus, classe Win32_TSGatewayConnection
- Win32_TSGatewayConnection de la classe Services Bureau à distance, méthode CheckStatus
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118757"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a>Méthode CheckStatus de la \_ classe Win32 TSGatewayConnection

Vérifie l’état d’une connexion de serveur de passerelle Bureau à distance (passerelle Bureau à distance) à un autre ordinateur et détermine si l’ordinateur cible est configuré pour l’équilibrage de charge.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du serveur* \[ dans\]
</dt> <dd>

Nom du serveur de passerelle Bureau à distance source à partir duquel la connexion est vérifiée.

</dd> <dt>

*EndpointName* \[ dans\]
</dt> <dd>

Nom du serveur cible (point de terminaison) sur lequel l’accès est vérifié à partir du serveur source.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne les valeurs de retour possibles suivantes.

<dl> <dt>


</dt> <dd>

0

L’état de la connexion est OK. Le point de terminaison est accessible et configuré pour l’équilibrage de charge.

</dd> <dt>


</dt> <dd>

1

L’état de la connexion est inconnu. Probablement, une exception s’est produite.

</dd> <dt>


</dt> <dd>

0x80075c34

Le point de terminaison n’est pas accessible ou n’est pas configuré pour l’équilibrage de charge.

</dd> <dt>


</dt> <dd>

0x80075c32

Une erreur d’État s’est produite. Le point de terminaison est accessible, mais le service d’équilibrage de charge RPC/HTTP (RPCHTTPLBS) n’est pas démarré sur l’ordinateur cible.

</dd> </dl>

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

