---
description: TLS est une norme étroitement liée à SSL 3,0 et est parfois appelée &\# 0034 ; SSL 3,1&\# 0034 ;.
ms.assetid: 92b1b486-7e10-48a2-b1d2-56d4e472dbe4
title: TLS et SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac1a2e783b6f3355127a3148f1575f73119f6604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545024"
---
# <a name="tls-vs-ssl"></a><span data-ttu-id="6f798-103">TLS et SSL</span><span class="sxs-lookup"><span data-stu-id="6f798-103">TLS vs. SSL</span></span>

<span data-ttu-id="6f798-104">TLS est une norme étroitement liée à SSL 3,0 et est parfois appelée « SSL 3,1 ».</span><span class="sxs-lookup"><span data-stu-id="6f798-104">TLS is a standard closely related to SSL 3.0, and is sometimes referred to as "SSL 3.1".</span></span> <span data-ttu-id="6f798-105">TLS remplace SSL 2,0 et doit être utilisé dans un nouveau développement.</span><span class="sxs-lookup"><span data-stu-id="6f798-105">TLS supersedes SSL 2.0 and should be used in new development.</span></span> <span data-ttu-id="6f798-106">À partir de Windows 10, version 1607 et Windows Server 2016, SSL 2,0 a été supprimé et n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6f798-106">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

<span data-ttu-id="6f798-107">Les applications qui requièrent un haut niveau d’interopérabilité doivent prendre en charge SSL 3,0 et TLS.</span><span class="sxs-lookup"><span data-stu-id="6f798-107">Applications that require a high level of interoperability should support SSL 3.0 and TLS.</span></span> <span data-ttu-id="6f798-108">En raison des similarités entre ces deux protocoles, les détails SSL ne sont pas inclus dans cette documentation, sauf lorsqu’ils diffèrent de TLS.</span><span class="sxs-lookup"><span data-stu-id="6f798-108">Because of the similarities between these two protocols, SSL details are not included in this documentation, except where they differ from TLS.</span></span> <span data-ttu-id="6f798-109">Les éléments suivants proviennent de [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span><span class="sxs-lookup"><span data-stu-id="6f798-109">The following is from [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span></span>

<span data-ttu-id="6f798-110">« Les différences entre ce protocole et SSL 3,0 ne sont pas spectaculaires, mais elles sont suffisamment significatives pour que TLS 1,0 et SSL 3,0 n’interopèrent pas (bien que TLS 1,0 intègre un mécanisme par lequel une implémentation TLS peut revenir à SSL 3,0). »</span><span class="sxs-lookup"><span data-stu-id="6f798-110">"The differences between this protocol and SSL 3.0 are not dramatic, but they are significant enough that TLS 1.0 and SSL 3.0 do not interoperate (although TLS 1.0 does incorporate a mechanism by which a TLS implementation can back down to SSL 3.0)."</span></span>

 

 



