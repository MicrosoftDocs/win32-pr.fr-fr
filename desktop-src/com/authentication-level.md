---
title: Niveau d’authentification
description: Le niveau d’authentification contrôle la sécurité qu’un client ou un serveur souhaite obtenir de son SSP.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250661e4a8da42ffd91f37e282a39fbb52b6328a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295763"
---
# <a name="authentication-level"></a>Niveau d’authentification

Le niveau d’authentification contrôle la sécurité qu’un client ou un serveur souhaite obtenir de son SSP. Le niveau d’authentification est défini en passant une valeur de niveau d’authentification RPC appropriée \_ \_ \_ \_ xxx à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) via le paramètre *dwAuthnLevel* . Les niveaux d’authentification du client et du serveur sont comparés pendant le protocole de transfert, et le paramètre de protection de niveau supérieur est utilisé pour la connexion.

Les différents niveaux d’authentification sont décrits comme suit, de la protection de la sécurité de niveau le plus bas à la plus élevée :

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Aucun (RPC \_ C \_ Authn \_ niveau \_ aucun)
</dt> <dd>

Aucune authentification n’est effectuée pendant la communication entre le client et le serveur. Tous les paramètres de sécurité sont ignorés. Ce niveau d’authentification ne peut être défini que si le [niveau de service d’authentification](com-authentication-service-constants.md) est RPC \_ C \_ Authn \_ None.

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Valeur par défaut \_ ( \_ niveau d' \_ authentification \_ par défaut C RPC)
</dt> <dd>

COM choisit le niveau d’authentification à l’aide de sa négociation permanente de sécurité normale. Elle ne choisit jamais un niveau d’authentification None.

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connecter ( \_ \_ connexion au niveau authn C RPC \_ \_ )
</dt> <dd>

La négociation d’authentification normale se produit entre le client et le serveur, et une clé de session est établie, mais cette clé n’est jamais utilisée pour la communication entre le client et le serveur. Toute communication après l’établissement de la liaison n’est pas sécurisée.

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Appel ( \_ appel de \_ niveau Authn C RPC \_ \_ )
</dt> <dd>

Seuls les en-têtes du début de chaque appel sont signés. Le reste des données échangées entre le client et le serveur n’est ni signé ni chiffré. La plupart des SSP ne prennent pas en charge ce niveau d’authentification et le promeut en mode silencieux vers le paquet.

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Paquet (Authentication Authentication \_ C RPC \_ niveau d’authentification \_ \_ )
</dt> <dd>

L’en-tête de chaque paquet est signé mais pas chiffré. Les paquets eux-mêmes ne sont pas signés ou chiffrés.

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Intégrité des paquets ( \_ \_ intégrité PKT du niveau d’authentification RPC C \_ \_ \_ )
</dt> <dd>

Chaque paquet de données est signé dans son intégralité, mais n’est pas chiffré. Étant donné que toutes les données sont signées par l’expéditeur, le destinataire peut être certain qu’aucune des données n’a été falsifiée pendant le transit.

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Confidentialité des paquets (RPC-niveau d’authentification de la \_ \_ \_ \_ \_ confidentialité)
</dt> <dd>

Chaque paquet de données est signé et chiffré. Cela permet de protéger l’ensemble de la communication entre le client et le serveur.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[AuthenticationLevel](authenticationlevel.md)
</dt> <dt>

[LegacyAuthenticationLevel](legacyauthenticationlevel.md)
</dt> </dl>

 

 




