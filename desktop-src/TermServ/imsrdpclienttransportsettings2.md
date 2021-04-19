---
title: Interface IMsRdpClientTransportSettings2
description: Gère les paramètres de transport client pour le serveur de passerelle Bureau à distance (passerelle Bureau à distance). | Interface IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, Description
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106542117"
---
# <a name="imsrdpclienttransportsettings2-interface"></a>Interface IMsRdpClientTransportSettings2

Gère les paramètres de transport client pour le serveur de passerelle Bureau à distance (passerelle Bureau à distance).

## <a name="members"></a>Membres

L’interface **IMsRdpClientTransportSettings2** hérite de [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md). **IMsRdpClientTransportSettings2** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientTransportSettings2** possède les propriétés suivantes.



| Propriété                                                                                                    | Type d’accès           | Description                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [**GatewayCredSharing**](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | Lecture/écriture<br/> | Indique si la fonctionnalité d’authentification unique pour la passerelle des services Bureau à distance est activée.<br/>                |
| [**GatewayDomain**](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | Lecture/écriture<br/> | Nom de domaine qu’un utilisateur fournit pour se connecter au serveur de passerelle Bureau à distance.<br/>              |
| [**GatewayEncryptedOtpCookie**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | Lecture/écriture<br/> | Cookie à mot de passe à usage unique chiffré.<br/>                                                              |
| [**GatewayEncryptedOtpCookieSize**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | Lecture/écriture<br/> | Taille, en octets, du cookie à mot de passe à usage unique chiffré.<br/>                                       |
| [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | Écriture seule<br/> | Mot de passe fourni par l’utilisateur pour se connecter au serveur de passerelle Bureau à distance.<br/>                 |
| [**GatewayPreAuthRequirement**](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | Lecture/écriture<br/> | Indique si la fonctionnalité de mot de passe à usage unique de la passerelle des services Bureau à distance est activée.<br/>           |
| [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | Lecture/écriture<br/> | Adresse Web du serveur de pré-authentification.<br/>                                      |
| [**GatewaySupportUrl**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | Lecture/écriture<br/> | Adresse Web du site qui fournit un support technique pour le serveur de passerelle Bureau à distance.<br/> |
| [**GatewayUsername**](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | Lecture/écriture<br/> | Nom d’utilisateur qu’un utilisateur fournit pour se connecter au serveur de passerelle Bureau à distance.<br/>                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista avec SP1<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                    |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





