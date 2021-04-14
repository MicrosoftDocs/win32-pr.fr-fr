---
title: Niveau d’authentification
description: Le niveau d’authentification contrôle la sécurité qu’un client ou un serveur souhaite obtenir de son SSP.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250661e4a8da42ffd91f37e282a39fbb52b6328a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311509"
---
# <a name="authentication-level"></a><span data-ttu-id="aab0a-103">Niveau d’authentification</span><span class="sxs-lookup"><span data-stu-id="aab0a-103">Authentication Level</span></span>

<span data-ttu-id="aab0a-104">Le niveau d’authentification contrôle la sécurité qu’un client ou un serveur souhaite obtenir de son SSP.</span><span class="sxs-lookup"><span data-stu-id="aab0a-104">The authentication level controls how much security a client or server wants from its SSP.</span></span> <span data-ttu-id="aab0a-105">Le niveau d’authentification est défini en passant une valeur de niveau d’authentification RPC appropriée \_ \_ \_ \_ xxx à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) via le paramètre *dwAuthnLevel* .</span><span class="sxs-lookup"><span data-stu-id="aab0a-105">The authentication level is set by passing an appropriate RPC\_C\_AUTHN\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwAuthnLevel* parameter.</span></span> <span data-ttu-id="aab0a-106">Les niveaux d’authentification du client et du serveur sont comparés pendant le protocole de transfert, et le paramètre de protection de niveau supérieur est utilisé pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="aab0a-106">The authentication levels from the client and server are compared during the handshake, and the higher level security protection setting is used for the connection.</span></span>

<span data-ttu-id="aab0a-107">Les différents niveaux d’authentification sont décrits comme suit, de la protection de la sécurité de niveau le plus bas à la plus élevée :</span><span class="sxs-lookup"><span data-stu-id="aab0a-107">The different authentication levels are described as follows, from lowest level security protection to highest:</span></span>

<dl> <dt>

<span data-ttu-id="aab0a-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Aucun (RPC \_ C \_ Authn \_ niveau \_ aucun)</span><span class="sxs-lookup"><span data-stu-id="aab0a-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC\_C\_AUTHN\_LEVEL\_NONE)</span></span>
</dt> <dd>

<span data-ttu-id="aab0a-109">Aucune authentification n’est effectuée pendant la communication entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="aab0a-109">No authentication is performed during the communication between client and server.</span></span> <span data-ttu-id="aab0a-110">Tous les paramètres de sécurité sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="aab0a-110">All security settings are ignored.</span></span> <span data-ttu-id="aab0a-111">Ce niveau d’authentification ne peut être défini que si le [niveau de service d’authentification](com-authentication-service-constants.md) est RPC \_ C \_ Authn \_ None.</span><span class="sxs-lookup"><span data-stu-id="aab0a-111">This authentication level can be set only if the [authentication service level](com-authentication-service-constants.md) is RPC\_C\_AUTHN\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="aab0a-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Valeur par défaut \_ ( \_ niveau d' \_ authentification \_ par défaut C RPC)</span><span class="sxs-lookup"><span data-stu-id="aab0a-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Default (RPC\_C\_AUTHN\_LEVEL\_DEFAULT)</span></span>
</dt> <dd>

<span data-ttu-id="aab0a-113">COM choisit le niveau d’authentification à l’aide de sa négociation permanente de sécurité normale.</span><span class="sxs-lookup"><span data-stu-id="aab0a-113">COM chooses the authentication level by using its normal security blanket negotiation.</span></span> <span data-ttu-id="aab0a-114">Elle ne choisit jamais un niveau d’authentification None.</span><span class="sxs-lookup"><span data-stu-id="aab0a-114">It will never choose an authentication level of None.</span></span>

</dd> <dt>

<span data-ttu-id="aab0a-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect ( \_ \_ connexion au niveau Authn C RPC \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="aab0a-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (RPC\_C\_AUTHN\_LEVEL\_CONNECT)</span></span>
</dt> <dd>

<span data-ttu-id="aab0a-116">La négociation d’authentification normale se produit entre le client et le serveur, et une clé de session est établie, mais cette clé n’est jamais utilisée pour la communication entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="aab0a-116">The normal authentication handshake occurs between the client and server, and a session key is established but that key is never used for communication between the client and server.</span></span> <span data-ttu-id="aab0a-117">Toute communication après l’établissement de la liaison n’est pas sécurisée.</span><span class="sxs-lookup"><span data-stu-id="aab0a-117">All communication after the handshake is nonsecure.</span></span>

</dd> <dt>

<span data-ttu-id="aab0a-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Appel ( \_ appel de \_ niveau Authn C RPC \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="aab0a-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call (RPC\_C\_AUTHN\_LEVEL\_CALL)</span></span>
</dt> <dd>

<span data-ttu-id="aab0a-119">Seuls les en-têtes du début de chaque appel sont signés.</span><span class="sxs-lookup"><span data-stu-id="aab0a-119">Only the headers of the beginning of each call are signed.</span></span> <span data-ttu-id="aab0a-120">Le reste des données échangées entre le client et le serveur n’est ni signé ni chiffré.</span><span class="sxs-lookup"><span data-stu-id="aab0a-120">The rest of the data exchanged between the client and server is neither signed nor encrypted.</span></span> <span data-ttu-id="aab0a-121">La plupart des SSP ne prennent pas en charge ce niveau d’authentification et le promeut en mode silencieux vers le paquet.</span><span class="sxs-lookup"><span data-stu-id="aab0a-121">Most SSPs do not support this authentication level and silently promote it to Packet.</span></span>

</dd> <dt>

<span data-ttu-id="aab0a-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Paquet (Authentication Authentication \_ C RPC \_ niveau d’authentification \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="aab0a-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Packet (RPC\_C\_AUTHN\_LEVEL\_PKT)</span></span>
</dt> <dd>

<span data-ttu-id="aab0a-123">L’en-tête de chaque paquet est signé mais pas chiffré.</span><span class="sxs-lookup"><span data-stu-id="aab0a-123">The header of each packet is signed but not encrypted.</span></span> <span data-ttu-id="aab0a-124">Les paquets eux-mêmes ne sont pas signés ou chiffrés.</span><span class="sxs-lookup"><span data-stu-id="aab0a-124">The packets themselves are not signed or encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="aab0a-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Intégrité des paquets ( \_ \_ intégrité PKT du niveau d’authentification RPC C \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="aab0a-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Packet Integrity (RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY)</span></span>
</dt> <dd>

<span data-ttu-id="aab0a-126">Chaque paquet de données est signé dans son intégralité, mais n’est pas chiffré.</span><span class="sxs-lookup"><span data-stu-id="aab0a-126">Each packet of data is signed in its entirety but is not encrypted.</span></span> <span data-ttu-id="aab0a-127">Étant donné que toutes les données sont signées par l’expéditeur, le destinataire peut être certain qu’aucune des données n’a été falsifiée pendant le transit.</span><span class="sxs-lookup"><span data-stu-id="aab0a-127">Because all of the data is signed by the sender, the recipient can be certain that none of the data has been tampered with during transit.</span></span>

</dd> <dt>

<span data-ttu-id="aab0a-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Confidentialité des paquets (RPC-niveau d’authentification de la \_ \_ \_ \_ \_ confidentialité)</span><span class="sxs-lookup"><span data-stu-id="aab0a-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Packet Privacy (RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY)</span></span>
</dt> <dd>

<span data-ttu-id="aab0a-129">Chaque paquet de données est signé et chiffré.</span><span class="sxs-lookup"><span data-stu-id="aab0a-129">Each data packet is signed and encrypted.</span></span> <span data-ttu-id="aab0a-130">Cela permet de protéger l’ensemble de la communication entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="aab0a-130">This helps protect the entire communication between the client and server.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="aab0a-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aab0a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aab0a-132">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="aab0a-132">AuthenticationLevel</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="aab0a-133">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="aab0a-133">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
</dt> </dl>

 

 




