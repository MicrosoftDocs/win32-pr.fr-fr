---
description: Comment créer une connexion sécurisée à l’aide de Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Création d’une connexion sécurisée à l’aide de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757293"
---
# <a name="creating-a-secure-connection-using-schannel"></a><span data-ttu-id="449fa-103">Création d’une connexion sécurisée à l’aide de Schannel</span><span class="sxs-lookup"><span data-stu-id="449fa-103">Creating a Secure Connection Using Schannel</span></span>

<span data-ttu-id="449fa-104">Le [*package de sécurité*](/windows/desktop/SecGloss/s-gly) Schannel donne accès à quatre [*protocoles de sécurité*](/windows/desktop/SecGloss/s-gly):</span><span class="sxs-lookup"><span data-stu-id="449fa-104">The Schannel [*security package*](/windows/desktop/SecGloss/s-gly) provides access to four [*security protocols*](/windows/desktop/SecGloss/s-gly):</span></span>

-   [<span data-ttu-id="449fa-105">Transport Layer Security (TLS 1,2)</span><span class="sxs-lookup"><span data-stu-id="449fa-105">Transport Layer Security (TLS 1.2)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="449fa-106">Transport Layer Security (TLS 1,1)</span><span class="sxs-lookup"><span data-stu-id="449fa-106">Transport Layer Security (TLS 1.1)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="449fa-107">Transport Layer Security (TLS 1,0)</span><span class="sxs-lookup"><span data-stu-id="449fa-107">Transport Layer Security (TLS 1.0)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="449fa-108">SSL (Secure Sockets Layer) (SSL 3,0)</span><span class="sxs-lookup"><span data-stu-id="449fa-108">Secure Sockets Layer (SSL 3.0)</span></span>](secure-sockets-layer-protocol.md)
-   [<span data-ttu-id="449fa-109">SSL (Secure Sockets Layer) (SSL 2,0)</span><span class="sxs-lookup"><span data-stu-id="449fa-109">Secure Sockets Layer (SSL 2.0)</span></span>](secure-sockets-layer-protocol.md)

> [!Note]  
> <span data-ttu-id="449fa-110">Les protocoles PCT et SSL 2,0 ont été remplacés par le protocole TLS et ne doivent pas être utilisés pour un nouveau développement.</span><span class="sxs-lookup"><span data-stu-id="449fa-110">The PCT and SSL 2.0 protocols have been superseded by the TLS protocol and should not be used for new development.</span></span>

 

<span data-ttu-id="449fa-111">**Pour configurer une connexion sécurisée entre un client et un serveur**</span><span class="sxs-lookup"><span data-stu-id="449fa-111">**To set up a secure connection between a client and server**</span></span>

1.  <span data-ttu-id="449fa-112">Obtenir des informations d’identification Schannel (en[obtenant des informations d’identification Schannel](obtaining-schannel-credentials.md)).</span><span class="sxs-lookup"><span data-stu-id="449fa-112">Obtain Schannel credentials ([Obtaining Schannel Credentials](obtaining-schannel-credentials.md)).</span></span>
2.  <span data-ttu-id="449fa-113">Créer un contexte de sécurité Schannel ([création d’un contexte de sécurité Schannel](creating-an-schannel-security-context.md)).</span><span class="sxs-lookup"><span data-stu-id="449fa-113">Create an Schannel security context ([Creating an Schannel Security Context](creating-an-schannel-security-context.md)).</span></span>

<span data-ttu-id="449fa-114">Une fois la connexion établie, vous pouvez récupérer des informations sur ses attributs.</span><span class="sxs-lookup"><span data-stu-id="449fa-114">After a connection is established, you can retrieve information about its attributes.</span></span> <span data-ttu-id="449fa-115">Pour plus d’informations, consultez [obtention d’informations sur les connexions Schannel](getting-information-about-schannel-connections.md).</span><span class="sxs-lookup"><span data-stu-id="449fa-115">For details, see [Getting Information About Schannel Connections](getting-information-about-schannel-connections.md).</span></span>

<span data-ttu-id="449fa-116">Si, après avoir établi une connexion, les exigences de sécurité de votre application changent ou la connexion est perdue, vous pouvez renégocier la connexion.</span><span class="sxs-lookup"><span data-stu-id="449fa-116">If, after you have established a connection, the security requirements of your application change or the connection is lost, you can renegotiate the connection.</span></span> <span data-ttu-id="449fa-117">Pour plus d’informations, consultez [renégociation d’une connexion Schannel](renegotiating-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="449fa-117">For details, see [Renegotiating an Schannel Connection](renegotiating-an-schannel-connection.md).</span></span>

<span data-ttu-id="449fa-118">Une fois que vous avez fini d’utiliser une connexion Schannel, vous devez effectuer le nettoyage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="449fa-118">When you have finished using an Schannel connection, you must perform the necessary cleanup.</span></span> <span data-ttu-id="449fa-119">Pour plus d’informations, consultez [arrêt d’une connexion Schannel](shutting-down-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="449fa-119">For details, see [Shutting Down an Schannel Connection](shutting-down-an-schannel-connection.md).</span></span>

<span data-ttu-id="449fa-120">Pour plus d’informations sur les exemples fournis avec le kit de développement logiciel (SDK) de plateforme qui illustrent le [*package de sécurité*](/windows/desktop/SecGloss/s-gly)Schannel, consultez les exemples de SDK à l’aide de Schannel.</span><span class="sxs-lookup"><span data-stu-id="449fa-120">For information about samples shipped with the Platform Software Development Kit (SDK) that demonstrate the Schannel [*security package*](/windows/desktop/SecGloss/s-gly), see the PSDK samples using Schannel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="449fa-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="449fa-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="449fa-122">Spécification des chiffrements Schannel et des forces de chiffrement</span><span class="sxs-lookup"><span data-stu-id="449fa-122">Specifying Schannel Ciphers and Cipher Strengths</span></span>](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
