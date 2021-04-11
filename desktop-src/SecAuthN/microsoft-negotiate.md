---
description: Microsoft Negotiate est un fournisseur de support de sécurité qui agit comme une couche application entre l’interface du fournisseur de support de sécurité et les autres ssp.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Négociation Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951121"
---
# <a name="microsoft-negotiate"></a><span data-ttu-id="eb7d9-103">Négociation Microsoft</span><span class="sxs-lookup"><span data-stu-id="eb7d9-103">Microsoft Negotiate</span></span>

<span data-ttu-id="eb7d9-104">Microsoft Negotiate est un [*fournisseur SSP (Security Support Provider*](../secgloss/s-gly.md) ) qui agit comme une couche application entre l’interface [SSPI](sspi.md)( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) et les autres ssp.</span><span class="sxs-lookup"><span data-stu-id="eb7d9-104">Microsoft Negotiate is a [*security support provider*](../secgloss/s-gly.md) (SSP) that acts as an application layer between [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) and the other SSPs.</span></span> <span data-ttu-id="eb7d9-105">Lorsqu'une application appelle un SSPI à se connecter à un réseau, il peut spécifier un SSP pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="eb7d9-105">When an application calls into SSPI to log on to a network, it can specify an SSP to process the request.</span></span> <span data-ttu-id="eb7d9-106">Si l’application spécifie Negotiate, Negotiate analyse la demande et choisit le SSP le plus approprié pour gérer la demande en fonction de la stratégie de sécurité configurée par le client.</span><span class="sxs-lookup"><span data-stu-id="eb7d9-106">If the application specifies Negotiate, Negotiate analyzes the request and picks the best SSP to handle the request based on customer-configured security policy.</span></span>

<span data-ttu-id="eb7d9-107">Actuellement, le package de sécurité Negotiate choisit entre [Kerberos](microsoft-kerberos.md) et [NTLM](microsoft-ntlm.md).</span><span class="sxs-lookup"><span data-stu-id="eb7d9-107">Currently, the Negotiate security package selects between [Kerberos](microsoft-kerberos.md) and [NTLM](microsoft-ntlm.md).</span></span> <span data-ttu-id="eb7d9-108">Negotiate sélectionne Kerberos, sauf s’il ne peut pas être utilisé par l’un des systèmes impliqués dans l’authentification ou si l’application appelante n’a pas fourni suffisamment d’informations pour utiliser Kerberos.</span><span class="sxs-lookup"><span data-stu-id="eb7d9-108">Negotiate selects Kerberos unless it cannot be used by one of the systems involved in the authentication or the calling application did not provide sufficient information to use Kerberos.</span></span>

<span data-ttu-id="eb7d9-109">Pour permettre à Negotiate de sélectionner le fournisseur de sécurité [Kerberos](microsoft-kerberos.md) , l’application cliente doit fournir un [*nom de principal du service*](../secgloss/s-gly.md) (SPN), un nom d’utilisateur principal (UPN) ou un nom de compte NetBIOS comme nom de cible.</span><span class="sxs-lookup"><span data-stu-id="eb7d9-109">To allow Negotiate to select the [Kerberos](microsoft-kerberos.md) security provider, the client application must provide a [*service principal name*](../secgloss/s-gly.md) (SPN), a user principal name (UPN), or a NetBIOS account name as the target name.</span></span> <span data-ttu-id="eb7d9-110">Dans le cas contraire, Negotiate sélectionne toujours le fournisseur de sécurité [NTLM](microsoft-ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="eb7d9-110">Otherwise, Negotiate always selects the [NTLM](microsoft-ntlm.md) security provider.</span></span>

<span data-ttu-id="eb7d9-111">Un serveur qui utilise le package Negotiate peut répondre aux applications clientes qui sélectionnent spécifiquement le fournisseur de sécurité [Kerberos](microsoft-kerberos.md) ou [NTLM](microsoft-ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="eb7d9-111">A server that uses the Negotiate package is able to respond to client applications that specifically select either the [Kerberos](microsoft-kerberos.md) or [NTLM](microsoft-ntlm.md) security provider.</span></span> <span data-ttu-id="eb7d9-112">Toutefois, une application cliente doit savoir qu’un serveur prend en charge le package Negotiate pour demander l’authentification à l’aide de Negotiate.</span><span class="sxs-lookup"><span data-stu-id="eb7d9-112">However, a client application must know that a server supports the Negotiate package to request authentication using Negotiate.</span></span> <span data-ttu-id="eb7d9-113">Un serveur qui ne prend pas en charge Negotiate ne peut pas toujours répondre aux demandes des clients qui spécifient Negotiate comme SSP.</span><span class="sxs-lookup"><span data-stu-id="eb7d9-113">A server that does not support Negotiate cannot always respond to requests from clients that specify Negotiate as the SSP.</span></span>

## <a name="reasons-to-use-the-negotiate-package"></a><span data-ttu-id="eb7d9-114">Raisons pour utiliser le package Negotiate</span><span class="sxs-lookup"><span data-stu-id="eb7d9-114">Reasons to Use the Negotiate Package</span></span>

-   <span data-ttu-id="eb7d9-115">Permet au système d’utiliser le protocole disponible le plus fort (le plus sécurisé).</span><span class="sxs-lookup"><span data-stu-id="eb7d9-115">Allows the system to use the strongest (most secure) available protocol.</span></span>
-   <span data-ttu-id="eb7d9-116">Garantit la compatibilité ascendante de votre application.</span><span class="sxs-lookup"><span data-stu-id="eb7d9-116">Ensures forward compatibility for your application.</span></span>
-   <span data-ttu-id="eb7d9-117">Garantit que votre application présente un comportement conforme à la stratégie de sécurité définie par le client.</span><span class="sxs-lookup"><span data-stu-id="eb7d9-117">Ensures that your application exhibits behavior that is in accordance with the security policy set by the customer.</span></span>

 

 
