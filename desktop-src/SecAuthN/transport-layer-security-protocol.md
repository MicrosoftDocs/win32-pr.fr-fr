---
description: Schannel prend en charge les versions 1,0, 1,1 et 1,2 du protocole TLS (Transport Layer Security).
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Protocole TLS (Transport Layer Security)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532140"
---
# <a name="transport-layer-security-protocol"></a><span data-ttu-id="9ee83-103">Protocole TLS (Transport Layer Security)</span><span class="sxs-lookup"><span data-stu-id="9ee83-103">Transport Layer Security Protocol</span></span>

<span data-ttu-id="9ee83-104">Schannel prend en charge les versions 1,0, 1,1 et 1,2 du [*protocole TLS (Transport Layer Security)*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9ee83-104">Schannel supports versions 1.0, 1.1, and 1.2 of the [*Transport Layer Security (TLS) protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="9ee83-105">Ce protocole est une norme de l’industrie conçue pour protéger la confidentialité des informations communiquées sur Internet.</span><span class="sxs-lookup"><span data-stu-id="9ee83-105">This protocol is an industry standard designed to protect the privacy of information communicated over the Internet.</span></span> <span data-ttu-id="9ee83-106">TLS suppose qu’un transport orienté connexion, généralement TCP, est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9ee83-106">TLS assumes that a connection-oriented transport, typically TCP, is in use.</span></span> <span data-ttu-id="9ee83-107">Le protocole TLS permet aux applications client/serveur de détecter les risques de sécurité suivants :</span><span class="sxs-lookup"><span data-stu-id="9ee83-107">The TLS protocol allows client/server applications to detect the following security risks:</span></span>

-   <span data-ttu-id="9ee83-108">Falsification des messages</span><span class="sxs-lookup"><span data-stu-id="9ee83-108">Message tampering</span></span>
-   <span data-ttu-id="9ee83-109">Interception des messages</span><span class="sxs-lookup"><span data-stu-id="9ee83-109">Message interception</span></span>
-   <span data-ttu-id="9ee83-110">Falsification de message</span><span class="sxs-lookup"><span data-stu-id="9ee83-110">Message forgery</span></span>

<span data-ttu-id="9ee83-111">La spécification complète du protocole TLS est disponible sur le site Web IETF : [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .</span><span class="sxs-lookup"><span data-stu-id="9ee83-111">The full specification of the TLS Protocol is available from the IETF website: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="organization-of-tls"></a><span data-ttu-id="9ee83-112">Organisation du protocole TLS</span><span class="sxs-lookup"><span data-stu-id="9ee83-112">Organization of TLS</span></span>

<span data-ttu-id="9ee83-113">Les étapes suivantes sont impliquées dans l’utilisation du protocole TLS pour la communication client/serveur :</span><span class="sxs-lookup"><span data-stu-id="9ee83-113">The following steps are involved in using TLS for client/server communication:</span></span>

 <span data-ttu-id="9ee83-114">**Pour utiliser TLS pour la communication client/serveur**</span><span class="sxs-lookup"><span data-stu-id="9ee83-114">**To use TLS for client/server communication**</span></span>

1.  <span data-ttu-id="9ee83-115">Négociation de la suite de négociation et de la suite de chiffrement</span><span class="sxs-lookup"><span data-stu-id="9ee83-115">Handshake and cipher suite negotiation</span></span>
2.  <span data-ttu-id="9ee83-116">Authentification des tiers</span><span class="sxs-lookup"><span data-stu-id="9ee83-116">Authentication of parties</span></span>
3.  <span data-ttu-id="9ee83-117">Échange d’informations relatives aux clés</span><span class="sxs-lookup"><span data-stu-id="9ee83-117">Key-related information exchange</span></span>
4.  <span data-ttu-id="9ee83-118">Échange de données d’application</span><span class="sxs-lookup"><span data-stu-id="9ee83-118">Application data exchange</span></span>

<span data-ttu-id="9ee83-119">Les étapes qui composent TLS sont divisées en deux protocoles qui, ensemble, assurent la sécurité de la connexion :</span><span class="sxs-lookup"><span data-stu-id="9ee83-119">The steps that make up TLS are divided into two protocols that, together, provide connection security:</span></span>

-   <span data-ttu-id="9ee83-120">[Protocole de négociation TLS](tls-handshake-protocol.md)— (étapes 1 à 3)</span><span class="sxs-lookup"><span data-stu-id="9ee83-120">[TLS Handshake Protocol](tls-handshake-protocol.md)— (steps 1 – 3)</span></span>
-   <span data-ttu-id="9ee83-121">[Protocole d’enregistrement TLS](tls-record-protocol.md)— (étape 4)</span><span class="sxs-lookup"><span data-stu-id="9ee83-121">[TLS Record Protocol](tls-record-protocol.md)— (step 4)</span></span>

## <a name="sspi-with-tls-implementations"></a><span data-ttu-id="9ee83-122">Implémentations SSPI avec TLS</span><span class="sxs-lookup"><span data-stu-id="9ee83-122">SSPI with TLS implementations</span></span>

<span data-ttu-id="9ee83-123">Dans la mesure où TLS n’a pas de spécification GSSAPI, les implémenteurs TLS ne sont peut-être pas familiers avec les fonctions SSPI.</span><span class="sxs-lookup"><span data-stu-id="9ee83-123">Because TLS does not have a GSSAPI specification, TLS implementers may not be familiar with the SSPI functions.</span></span> <span data-ttu-id="9ee83-124">Les applications appellent les fonctions SSPI pour énumérer les packages disponibles, créer et utiliser des handles pour les informations d’identification, créer des contextes de sécurité et garantir la confidentialité de l’intégrité des messages.</span><span class="sxs-lookup"><span data-stu-id="9ee83-124">Applications call the SSPI functions to enumerate available packages, create and work with handles to credentials, create security contexts and ensure message integrity privacy.</span></span>

<span data-ttu-id="9ee83-125">Pour prendre en charge les fonctions SSPI utilisées par les applications en mode utilisateur, les fonctions listées dans les [fonctions implémentées par SSP/APS en mode utilisateur](/windows/desktop/SecAuthN/authentication-functions) doivent être prises en charge par les implémentations TLS, telles que schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="9ee83-125">To support the SSPI functions used by user mode applications, the functions listed in [Functions Implemented by User-mode SSP/APs](/windows/desktop/SecAuthN/authentication-functions) need to be supported by TLS implementations such as schannel.dll.</span></span>

<span data-ttu-id="9ee83-126">Pour plus d’informations sur les fonctions SSPI et les fonctions SSP, consultez [fonctions d’authentification](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9ee83-126">For details about the SSPI functions and SSP functions, see [Authentication Functions](authentication-functions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ee83-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ee83-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ee83-128">Suites de chiffrement TLS</span><span class="sxs-lookup"><span data-stu-id="9ee83-128">TLS Cipher Suites</span></span>](tls-cipher-suites.md)
</dt> <dt>

[<span data-ttu-id="9ee83-129">TLS et SSL</span><span class="sxs-lookup"><span data-stu-id="9ee83-129">TLS vs. SSL</span></span>](tls-versus-ssl.md)
</dt> </dl>

 

 
