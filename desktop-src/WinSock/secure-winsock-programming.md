---
description: Vous trouverez ci-dessous un guide de sécurisation de la programmation Windows Sockets.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Programmation Winsock sécurisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d7a0710a4446486835ec14435fa7d7ba1458c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755076"
---
# <a name="secure-winsock-programming"></a><span data-ttu-id="53c18-103">Programmation Winsock sécurisée</span><span class="sxs-lookup"><span data-stu-id="53c18-103">Secure Winsock Programming</span></span>

<span data-ttu-id="53c18-104">Vous trouverez ci-dessous un guide de sécurisation de la programmation Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="53c18-104">The following is a guide to secure Windows Sockets programming.</span></span> <span data-ttu-id="53c18-105">Il est conçu pour fournir une compréhension de la sécurité Winsock et des options disponibles pour le développeur d’applications réseau sécurisées.</span><span class="sxs-lookup"><span data-stu-id="53c18-105">It is designed to provide an understanding of Winsock security and the options available to the secure network application developer.</span></span>

-   [<span data-ttu-id="53c18-106">Utilisation \_ de so REUSEADDR et so \_ EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="53c18-106">Using SO\_REUSEADDR and SO\_EXCLUSIVEADDRUSE</span></span>](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [<span data-ttu-id="53c18-107">Extensions Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="53c18-107">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)

<span data-ttu-id="53c18-108">Les communications à l’aide de sockets peuvent également être chiffrées à l’aide des normes SSL/TLS utilisant un canal sécurisé, également appelé technologie Schannel.</span><span class="sxs-lookup"><span data-stu-id="53c18-108">Communications using sockets can also be encrypted using the SSL/TLS standards using Secure Channel, also known as Schannel technology.</span></span> <span data-ttu-id="53c18-109">Schannel est un fournisseur SSP (Security Support Provider) qui contient un ensemble de protocoles de sécurité qui assurent l’authentification des identités et la communication privée sécurisée via le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="53c18-109">Schannel is a security support provider (SSP) that contains a set of security protocols that provide identity authentication and secure, private communication through encryption.</span></span> <span data-ttu-id="53c18-110">Schannel est principalement utilisé pour les applications Internet qui nécessitent des communications HTTP (Secure Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="53c18-110">Schannel is primarily used for Internet applications that require secure Hypertext Transfer Protocol (HTTP) communications.</span></span> <span data-ttu-id="53c18-111">Pour plus d’informations, consultez [canal sécurisé](../secauthn/secure-channel.md).</span><span class="sxs-lookup"><span data-stu-id="53c18-111">For more information, please see [Secure Channel](../secauthn/secure-channel.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="53c18-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53c18-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53c18-113">Canal sécurisé</span><span class="sxs-lookup"><span data-stu-id="53c18-113">Secure Channel</span></span>](../secauthn/secure-channel.md)
</dt> </dl>

 

 
