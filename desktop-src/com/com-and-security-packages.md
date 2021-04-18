---
title: Packages COM et de sécurité
description: Windows prend en charge NTLMSSP (fournisseur de support de sécurité LAN Manager), le protocole d’authentification Kerberos V5 et le package de sécurité Schannel, qui fournit les protocoles PCT 1,0, SSL 2,0, SSL 3,0 et TLS 1,0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509375"
---
# <a name="com-and-security-packages"></a><span data-ttu-id="cfbf9-103">Packages COM et de sécurité</span><span class="sxs-lookup"><span data-stu-id="cfbf9-103">COM and Security Packages</span></span>

<span data-ttu-id="cfbf9-104">Windows prend en charge NTLMSSP (fournisseur de support de sécurité LAN Manager), le protocole d’authentification Kerberos V5 et le package de sécurité Schannel, qui fournit les protocoles PCT 1,0, SSL 2,0, SSL 3,0 et TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="cfbf9-104">Windows supports NTLMSSP (LAN Manager Security Support Provider), the Kerberos v5 authentication protocol, and the Schannel security package, which provides the PCT 1.0, SSL 2.0, SSL 3.0, and TLS 1.0 protocols.</span></span> <span data-ttu-id="cfbf9-105">Le Snego est également pris en charge, qui recherche les packages de sécurité disponibles et sélectionne celui qui convient le mieux.</span><span class="sxs-lookup"><span data-stu-id="cfbf9-105">Also supported is Snego, which checks for available security packages and selects the most appropriate one.</span></span>

<span data-ttu-id="cfbf9-106">Le tableau suivant indique les niveaux d’authentification pris en charge par les différents packages de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cfbf9-106">The following table shows the levels of authentication supported by the various security packages.</span></span>



| <span data-ttu-id="cfbf9-107">Authentification serveur/client</span><span class="sxs-lookup"><span data-stu-id="cfbf9-107">Server/Client Authentication</span></span>                                                                                           | <span data-ttu-id="cfbf9-108">Prise en charge des packages de sécurité</span><span class="sxs-lookup"><span data-stu-id="cfbf9-108">Security Package Support</span></span>                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="cfbf9-109">Ni le nom de l’autre.</span><span class="sxs-lookup"><span data-stu-id="cfbf9-109">Neither can get the name of the other.</span></span><br/>                                                                      | <span data-ttu-id="cfbf9-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="cfbf9-110">None</span></span><br/>                                                  |
| <span data-ttu-id="cfbf9-111">Le client peut authentifier le serveur, mais pas l’inverse.</span><span class="sxs-lookup"><span data-stu-id="cfbf9-111">The client can authenticate the server, but not vice versa.</span></span><br/>                                                 | <span data-ttu-id="cfbf9-112">Schannel</span><span class="sxs-lookup"><span data-stu-id="cfbf9-112">Schannel</span></span><br/>                                              |
| <span data-ttu-id="cfbf9-113">Le client ne peut pas détecter le serveur, mais le serveur peut obtenir l’ID d’utilisateur du client.</span><span class="sxs-lookup"><span data-stu-id="cfbf9-113">The client cannot discover the server, but the server can get the user ID of the client.</span></span><br/>                    | <span data-ttu-id="cfbf9-114">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="cfbf9-114">NTLMSSP</span></span><br/>                                               |
| <span data-ttu-id="cfbf9-115">Authentification mutuelle : le client et le serveur peuvent tous les deux connaître le nom de l’autre, si l’autorisation est accordée.</span><span class="sxs-lookup"><span data-stu-id="cfbf9-115">Mutual authentication: Both the client and server can know the name of the other, if permission is granted.</span></span><br/> | <span data-ttu-id="cfbf9-116">NTLMSSP (localement), protocole Kerberos V5 et Schannel</span><span class="sxs-lookup"><span data-stu-id="cfbf9-116">NTLMSSP (locally), Kerberos v5 protocol, and Schannel</span></span><br/> |



 

<span data-ttu-id="cfbf9-117">Pour plus d’informations sur ces packages de sécurité, consultez les rubriques suivantes dans cette section :</span><span class="sxs-lookup"><span data-stu-id="cfbf9-117">For more information about these security packages, see the following topics in this section:</span></span>

-   [<span data-ttu-id="cfbf9-118">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="cfbf9-118">NTLMSSP</span></span>](ntlmssp.md)
-   [<span data-ttu-id="cfbf9-119">Protocole Kerberos V5</span><span class="sxs-lookup"><span data-stu-id="cfbf9-119">Kerberos v5 Protocol</span></span>](kerberos-v5-protocol.md)
-   [<span data-ttu-id="cfbf9-120">Schannel</span><span class="sxs-lookup"><span data-stu-id="cfbf9-120">Schannel</span></span>](schannel.md)
-   [<span data-ttu-id="cfbf9-121">Snego</span><span class="sxs-lookup"><span data-stu-id="cfbf9-121">Snego</span></span>](snego.md)

## <a name="related-topics"></a><span data-ttu-id="cfbf9-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cfbf9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfbf9-123">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="cfbf9-123">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 





