---
title: Configuration de RPC pour SPX/IPX
description: Lorsque vous utilisez les \_ transports ncacn SPX et ncadg \_ IPX, le nom du serveur est exactement le même que le nom du serveur sur Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462339"
---
# <a name="configuring-rpc-for-spxipx"></a><span data-ttu-id="0ccd7-103">Configuration de RPC pour SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="0ccd7-103">Configuring RPC for SPX/IPX</span></span>

<span data-ttu-id="0ccd7-104">Lorsque vous utilisez les transports **ncacn \_ SPX** et **ncadg \_ IPX** , le nom du serveur est exactement le même que le nom du serveur sur Windows.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-104">When using the **ncacn\_spx** and **ncadg\_ipx** transports, the server name is exactly the same as the server name on Windows.</span></span> <span data-ttu-id="0ccd7-105">Toutefois, étant donné que les noms sont distribués à l’aide de protocoles Novell, ils doivent être conformes aux conventions de nommage de Novell.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-105">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="0ccd7-106">Si un nom de serveur n’est pas un nom Novell valide, les serveurs ne seront pas en mesure de créer des points de terminaison avec les transports **ncacn \_ SPX** ou **ncadg \_ IPX** .</span><span class="sxs-lookup"><span data-stu-id="0ccd7-106">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** or **ncadg\_ipx** transports.</span></span>

<span data-ttu-id="0ccd7-107">Un nom de serveur Novell valide contient uniquement les caractères compris entre 0x20 et 0x7F.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-107">A valid Novell server name contains only the characters between 0x20 and 0x7f.</span></span> <span data-ttu-id="0ccd7-108">Les caractères minuscules sont remplacés par des majuscules.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-108">Lowercase characters are changed to uppercase.</span></span> <span data-ttu-id="0ccd7-109">Les caractères suivants ne peuvent pas être utilisés :</span><span class="sxs-lookup"><span data-stu-id="0ccd7-109">The following characters cannot be used:</span></span>

<span data-ttu-id="0ccd7-110">" \* ,./ :; <=> ?\[\]\\\|\]</span><span class="sxs-lookup"><span data-stu-id="0ccd7-110">"\*,./:;<=>?\[\]\\\|\]</span></span>

<span data-ttu-id="0ccd7-111">Pour assurer la compatibilité avec la première version de Windows NT, **ncacn \_ SPX** et **ncadg \_ IPX** vous permettent également d’utiliser un format spécial du nom de serveur appelé « nom tilde ».</span><span class="sxs-lookup"><span data-stu-id="0ccd7-111">To maintain compatibility with the first version of Windows NT, **ncacn\_spx** and **ncadg\_ipx** also enable you to use a special format of the server name known as the tilde name.</span></span> <span data-ttu-id="0ccd7-112">Le nom tilde est constitué d’un tilde (~), suivi du numéro de réseau à huit chiffres du serveur, puis de son adresse Ethernet à 12 chiffres.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-112">The tilde name consists of a tilde (~), followed by the server's eight-digit network number, and then followed by its 12-digit Ethernet address.</span></span> <span data-ttu-id="0ccd7-113">Les noms tilde présentent un avantage en ce qu’ils n’ont pas besoin de fonctionnalités de service de noms.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-113">Tilde names have an advantage in that they do not require any name service capabilities.</span></span> <span data-ttu-id="0ccd7-114">Par conséquent, si vous êtes connecté à un serveur, le nom tilde fonctionne.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-114">Thus, if you are connected to a server, the tilde name will work.</span></span>

<span data-ttu-id="0ccd7-115">Les tableaux suivants contiennent deux exemples de configurations qui illustrent les points décrits précédemment.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-115">The following tables contain two sample configurations that illustrate the points previously described.</span></span>



| <span data-ttu-id="0ccd7-116">Composant</span><span class="sxs-lookup"><span data-stu-id="0ccd7-116">Component</span></span>                            | <span data-ttu-id="0ccd7-117">Configuré en tant que</span><span class="sxs-lookup"><span data-stu-id="0ccd7-117">Configured as</span></span>      |
|--------------------------------------|--------------------|
| <span data-ttu-id="0ccd7-118">Windows Server</span><span class="sxs-lookup"><span data-stu-id="0ccd7-118">Windows server</span></span>                       | <span data-ttu-id="0ccd7-119">NWCS</span><span class="sxs-lookup"><span data-stu-id="0ccd7-119">NWCS</span></span>               |
| <span data-ttu-id="0ccd7-120">Client Windows</span><span class="sxs-lookup"><span data-stu-id="0ccd7-120">Windows client</span></span>                       | <span data-ttu-id="0ccd7-121">NWCS</span><span class="sxs-lookup"><span data-stu-id="0ccd7-121">NWCS</span></span>               |
| <span data-ttu-id="0ccd7-122">client Windows 16 bits, client MS-DOS</span><span class="sxs-lookup"><span data-stu-id="0ccd7-122">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="0ccd7-123">Redirecteur NetWare</span><span class="sxs-lookup"><span data-stu-id="0ccd7-123">NetWare Redirector</span></span> |



 

<span data-ttu-id="0ccd7-124">La configuration du tableau précédent nécessite que vous disposiez de serveurs de fichiers NetWare ou de routeurs sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-124">The configuration in the previous table requires that you have NetWare file servers or routers on your network.</span></span> <span data-ttu-id="0ccd7-125">Les performances sont optimales, car les noms de serveurs sont stockés dans le Bindery NetWare.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-125">It will produce the best performance because the server names are stored in the NetWare Bindery.</span></span>



| <span data-ttu-id="0ccd7-126">Composant</span><span class="sxs-lookup"><span data-stu-id="0ccd7-126">Component</span></span>                            | <span data-ttu-id="0ccd7-127">Configuré en tant que</span><span class="sxs-lookup"><span data-stu-id="0ccd7-127">Configured as</span></span> |
|--------------------------------------|---------------|
| <span data-ttu-id="0ccd7-128">Windows Server</span><span class="sxs-lookup"><span data-stu-id="0ccd7-128">Windows server</span></span>                       | <span data-ttu-id="0ccd7-129">Agent SAP</span><span class="sxs-lookup"><span data-stu-id="0ccd7-129">SAP Agent</span></span>     |
| <span data-ttu-id="0ccd7-130">Client Windows</span><span class="sxs-lookup"><span data-stu-id="0ccd7-130">Windows client</span></span>                       | <span data-ttu-id="0ccd7-131">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="0ccd7-131">IPX/SPX</span></span>       |
| <span data-ttu-id="0ccd7-132">client Windows 16 bits, client MS-DOS</span><span class="sxs-lookup"><span data-stu-id="0ccd7-132">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="0ccd7-133">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="0ccd7-133">IPX/SPX</span></span>       |



 

<span data-ttu-id="0ccd7-134">La deuxième configuration fonctionne dans un environnement qui ne contient pas de serveurs de fichiers NetWare ou de routeurs (par exemple, un réseau de deux ordinateurs : un serveur Windows et un client MS-DOS).</span><span class="sxs-lookup"><span data-stu-id="0ccd7-134">The second configuration works in an environment that does not contain NetWare file servers or routers (for example, a network of two computers: a Windows server and an MS-DOS client).</span></span> <span data-ttu-id="0ccd7-135">La résolution de noms, qui est effectuée lors du premier appel sur un handle de liaison, sera légèrement plus lente que dans la première configuration.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-135">Name resolution, which is accomplished during the first call over a binding handle, will be slightly slower than in the first configuration.</span></span> <span data-ttu-id="0ccd7-136">En outre, la deuxième configuration entraîne la génération d’un plus grand trafic sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-136">In addition, the second configuration results in more traffic generated over the network.</span></span>

<span data-ttu-id="0ccd7-137">Pour implémenter la résolution de noms, lorsqu’un serveur RPC utilise un point de terminaison SPX ou IPX, le nom du serveur et le point de terminaison sont enregistrés en tant que serveur SAP (Service Advertising Protocol) de type 640 (hexadécimal).</span><span class="sxs-lookup"><span data-stu-id="0ccd7-137">To implement name resolution, when an RPC server uses an SPX or IPX endpoint, the server name and endpoint are registered as a Service Advertising Protocol (SAP) server of type 640 (hexadecimal).</span></span> <span data-ttu-id="0ccd7-138">Pour résoudre un nom de serveur, le client RPC envoie une requête SAP pour tous les services du même type, puis analyse la liste des réponses pour le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-138">To resolve a server name, the RPC client sends a SAP request for all services of the same type, and then scans the list of responses for the name of the server.</span></span> <span data-ttu-id="0ccd7-139">Ce processus se produit pendant le premier appel RPC sur chaque handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-139">This process occurs during the first RPC call over each binding handle.</span></span> <span data-ttu-id="0ccd7-140">Pour plus d’informations sur le protocole SAP pour Novell, consultez la documentation de NetWare.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-140">For additional information on the SAP protocol for Novell, see your NetWare documentation.</span></span>

> [!Note]  
> <span data-ttu-id="0ccd7-141">Les applications clientes Windows 16 bits qui utilisent les transports **ncacn \_ SPX** ou **ncadg \_ IPX** requièrent que le fichier Nwipxspx.dll être installé pour pouvoir s’exécuter sous le sous-système wow.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-141">The 16-bit Windows client applications that use the **ncacn\_spx** or **ncadg\_ipx** transports require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="0ccd7-142">Contactez Novell pour obtenir ce fichier.</span><span class="sxs-lookup"><span data-stu-id="0ccd7-142">Contact Novell to obtain this file.</span></span>

 

 

 




