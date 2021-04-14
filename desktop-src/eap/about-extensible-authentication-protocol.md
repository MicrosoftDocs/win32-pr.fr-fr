---
title: À propos d’EAP
description: Le protocole EAP (Extensible Authentication Protocol), un standard pris en charge par de nombreux composants de mise en réseau Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Protocole EAP (Extensible Authentication Protocol), décrit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383096"
---
# <a name="about-eap"></a><span data-ttu-id="ed4b9-104">À propos d’EAP</span><span class="sxs-lookup"><span data-stu-id="ed4b9-104">About EAP</span></span>

<span data-ttu-id="ed4b9-105">Cette rubrique décrit le protocole EAP (Extensible Authentication Protocol), un standard pris en charge par de nombreux composants de mise en réseau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-105">This topic describes Extensible Authentication Protocol (EAP), a standard supported by many Microsoft networking components.</span></span>

## <a name="eap-components"></a><span data-ttu-id="ed4b9-106">Composants EAP</span><span class="sxs-lookup"><span data-stu-id="ed4b9-106">EAP Components</span></span>

<span data-ttu-id="ed4b9-107">EAP est essentiel pour la protection de la sécurité des réseaux locaux (LAN) sans fil (802.1 X), des réseaux locaux câblés et des réseaux privés virtuels (VPN) et d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-107">EAP is crucial for protecting the security of wireless (802.1X) LANs, wired LANs, and dial-up and Virtual Private Networks (VPNs).</span></span>

<span data-ttu-id="ed4b9-108">Les composants suivants prennent en charge le protocole EAP.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-108">The following components support the EAP protocol.</span></span>

-   <span data-ttu-id="ed4b9-109">Les clients et les serveurs d’accès à distance Microsoft pour l’accès à distance et VPN (PPTP et L2TP/IPSec) implémentent EAP en tant qu’extension de PPP.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-109">Microsoft Remote Access Clients and Servers for both dial-up and VPN (PPTP and L2TP/IPSec) implement EAP as an extension to PPP.</span></span> <span data-ttu-id="ed4b9-110">Pour plus d’informations, consultez la [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span><span class="sxs-lookup"><span data-stu-id="ed4b9-110">For more information, see [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span></span>
-   <span data-ttu-id="ed4b9-111">Les clients LAN câblés et sans fil compatibles Microsoft IEEE 802.1 X implémentent le protocole EAP tel que défini dans la norme IEEE 802.1 X Draft.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-111">Microsoft IEEE 802.1X compatible wireless and wired LAN clients implement EAP as defined in the IEEE 802.1X draft standard.</span></span>
-   <span data-ttu-id="ed4b9-112">Le serveur Microsoft RADIUS, appelé service d’authentification Internet (IAS), implémente le protocole EAP tel que défini dans la [norme RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span><span class="sxs-lookup"><span data-stu-id="ed4b9-112">Microsoft RADIUS server, called Internet Authentication Service (IAS) implement EAP as defined in [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span></span>

<span data-ttu-id="ed4b9-113">Tous les composants ci-dessus prennent en charge cette architecture extensible via le kit de développement logiciel (SDK) Microsoft Windows, ce qui vous permet d’intégrer des modules d’authentification tiers.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-113">All of the above components support this extensible architecture through the Microsoft Windows Software Development Kit (SDK), making it possible to integrate third-party authentication modules.</span></span> <span data-ttu-id="ed4b9-114">Ce mécanisme extensible peut être utilisé pour prendre en charge les cartes à jetons, Kerberos, la clé publique et les protocoles d’authentification S/Key.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-114">This extensible mechanism can be used to support token cards, Kerberos, Public Key, and S/Key authentication protocols.</span></span>

## <a name="protected-extensible-authentication-protocol"></a><span data-ttu-id="ed4b9-115">Protocole EAP (Protected Extensible Authentication Protocol)</span><span class="sxs-lookup"><span data-stu-id="ed4b9-115">Protected Extensible Authentication Protocol</span></span>

<span data-ttu-id="ed4b9-116">En plus de l’EAP, l’implémentation sans fil (802.1 X) et le serveur RADIUS prennent également en charge une norme émergente appelée PEAP (Protected EAP).</span><span class="sxs-lookup"><span data-stu-id="ed4b9-116">In addition to EAP, the wireless (802.1X) implementation and RADIUS server also support an emerging standard called Protected EAP (PEAP).</span></span>

<span data-ttu-id="ed4b9-117">PEAP fournit plusieurs services clés à d’autres protocoles d’authentification EAP, comme suit.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-117">PEAP provides several key services to other EAP authentication protocols, as follows.</span></span>

-   <span data-ttu-id="ed4b9-118">PEAP chiffre les paquets EAP d’autres protocoles d’authentification EAP à l’aide de TLS (Transport Layer Security), une technologie SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="ed4b9-118">PEAP encrypts EAP packets of other EAP authentication protocols using Transport Layer Security (TLS), a Secure Socket Layer (SSL) based technology.</span></span> <span data-ttu-id="ed4b9-119">Pour plus d’informations, consultez la [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span><span class="sxs-lookup"><span data-stu-id="ed4b9-119">For more information, see [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span></span>
-   <span data-ttu-id="ed4b9-120">PEAP authentifie le côté serveur à l’aide d’un certificat de serveur, avec le serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-120">PEAP authenticates the server-side using a Server Certificate, with RADIUS server.</span></span>
-   <span data-ttu-id="ed4b9-121">PEAP offre une nouvelle fonctionnalité d’authentification rapide qui prend en charge l’itinérance efficace entre les périphériques sans fil.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-121">PEAP offers fast re-authentication capability that supports efficient roaming between wireless devices.</span></span>
-   <span data-ttu-id="ed4b9-122">PEAP gère la fragmentation et le réassemblage des paquets EAP.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-122">PEAP manages the fragmentation and re-assembly of EAP packets.</span></span>
-   <span data-ttu-id="ed4b9-123">PEAP génère des clés utilisées pour le chiffrement du trafic sans fil.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-123">PEAP generates keys used for encrypting wireless traffic.</span></span>

<span data-ttu-id="ed4b9-124">Grâce à PEAP, il est beaucoup plus facile d’écrire un protocole EAP, car le programmeur n’a plus à résoudre ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="ed4b9-124">PEAP makes it much easier to write an EAP protocol because the programmer no longer has to address these issues.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed4b9-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed4b9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed4b9-126">À propos d’EAP et d’EAPHost</span><span class="sxs-lookup"><span data-stu-id="ed4b9-126">About EAP and EAPHost</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




