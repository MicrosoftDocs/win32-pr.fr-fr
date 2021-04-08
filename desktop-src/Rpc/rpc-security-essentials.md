---
title: Notions fondamentales de la sécurité RPC
description: Pour effectuer un appel de procédure distante, toutes les applications distribuées doivent créer une liaison entre le client et le serveur.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840650"
---
# <a name="rpc-security-essentials"></a><span data-ttu-id="92090-103">Notions fondamentales de la sécurité RPC</span><span class="sxs-lookup"><span data-stu-id="92090-103">RPC Security Essentials</span></span>

<span data-ttu-id="92090-104">Pour effectuer un appel de procédure distante, toutes les applications distribuées doivent créer une liaison entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="92090-104">To complete any remote procedure call, all distributed applications must create a binding between the client and the server.</span></span> <span data-ttu-id="92090-105">Pour plus d’informations sur les liaisons, consultez [liaison et Handles](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="92090-105">For more information on bindings, see [Binding and Handles](binding-and-handles.md).</span></span> <span data-ttu-id="92090-106">Pour effectuer un appel de procédure distante sécurisé, des étapes supplémentaires sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="92090-106">To complete a secure remote procedure call, additional steps are necessary.</span></span> <span data-ttu-id="92090-107">Tout d’abord, le serveur doit choisir un fournisseur de sécurité (service d’authentification dans la terminologie DCE).</span><span class="sxs-lookup"><span data-stu-id="92090-107">First, the server must choose a security provider (authentication service in DCE terminology).</span></span> <span data-ttu-id="92090-108">Il doit ensuite décider de son mécanisme d’authentification.</span><span class="sxs-lookup"><span data-stu-id="92090-108">Then it must decide on its authentication mechanism.</span></span> <span data-ttu-id="92090-109">Après cela, le client obtient une liaison au serveur et demande un appel de procédure distante sécurisé à partir de l’exécution RPC, et spécifie différentes options de sécurité, telles que le fournisseur de sécurité, les options QOS de sécurité, etc.</span><span class="sxs-lookup"><span data-stu-id="92090-109">After that, the client obtains a binding to the server, and requests a secure remote procedure call from the RPC run time, and specifies various security options, such as security provider, security QOS options, and so on.</span></span>

<span data-ttu-id="92090-110">Cette section explique les concepts et les informations essentiels nécessaires à l’utilisation des fonctions RPC pour créer un client et un serveur pour une application distribuée authentifiée.</span><span class="sxs-lookup"><span data-stu-id="92090-110">This section explains the essential concepts and information required to use the RPC functions to create a client and server for an authenticated distributed application.</span></span> <span data-ttu-id="92090-111">Elle est organisée dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="92090-111">It is organized into the following topics:</span></span>

-   [<span data-ttu-id="92090-112">Noms principaux</span><span class="sxs-lookup"><span data-stu-id="92090-112">Principal Names</span></span>](principal-names.md)
-   [<span data-ttu-id="92090-113">Niveaux d’authentification</span><span class="sxs-lookup"><span data-stu-id="92090-113">Authentication Levels</span></span>](authentication-levels.md)
-   [<span data-ttu-id="92090-114">Services d’authentification</span><span class="sxs-lookup"><span data-stu-id="92090-114">Authentication Services</span></span>](authentication-services.md)
-   [<span data-ttu-id="92090-115">Informations d’identification d’authentification du client</span><span class="sxs-lookup"><span data-stu-id="92090-115">Client Authentication Credentials</span></span>](client-authentication-credentials.md)
-   [<span data-ttu-id="92090-116">Services d’autorisation</span><span class="sxs-lookup"><span data-stu-id="92090-116">Authorization Services</span></span>](authorization-services.md)
-   [<span data-ttu-id="92090-117">Qualité de service</span><span class="sxs-lookup"><span data-stu-id="92090-117">Quality of Service</span></span>](quality-of-service.md)
-   [<span data-ttu-id="92090-118">Fonctions d’autorisation</span><span class="sxs-lookup"><span data-stu-id="92090-118">Authorization Functions</span></span>](authorization-functions.md)
-   [<span data-ttu-id="92090-119">Fonctions d’acquisition de clé</span><span class="sxs-lookup"><span data-stu-id="92090-119">Key Acquisition Functions</span></span>](key-acquisition-functions.md)
-   [<span data-ttu-id="92090-120">Emprunt d'identité de client</span><span class="sxs-lookup"><span data-stu-id="92090-120">Client Impersonation</span></span>](client-impersonation.md)

 

 




