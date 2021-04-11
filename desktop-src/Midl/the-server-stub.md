---
title: Stub serveur
description: Le stub serveur fournit des points d’entrée de substitution sur le serveur pour chacune des opérations définies dans le fichier IDL d’entrée.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL du compilateur MIDL, MIDL et RPC MIDL, interfaces, stub serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029644"
---
# <a name="the-server-stub"></a><span data-ttu-id="3c02f-104">Stub serveur</span><span class="sxs-lookup"><span data-stu-id="3c02f-104">The Server Stub</span></span>

<span data-ttu-id="3c02f-105">Le stub serveur fournit des points d’entrée de substitution sur le serveur pour chacune des opérations définies dans le fichier IDL d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3c02f-105">The server stub provides surrogate entry points on the server for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="3c02f-106">Quand une routine de stub serveur est appelée par la bibliothèque Runtime RPC, elle exécute les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c02f-106">When a server stub routine is invoked by the RPC run-time library, it performs the following functions:</span></span>

-   <span data-ttu-id="3c02f-107">Démarshale les arguments d’entrée (décompresse les arguments à partir de leurs formats transmis).</span><span class="sxs-lookup"><span data-stu-id="3c02f-107">Unmarshals input arguments (unpacks the arguments from their transmitted formats).</span></span>
-   <span data-ttu-id="3c02f-108">Appelle l’implémentation réelle de la procédure sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="3c02f-108">Calls the actual implementation of the procedure on the server.</span></span>
-   <span data-ttu-id="3c02f-109">Marshale les arguments de sortie (empaquette les arguments dans les formulaires transmis).</span><span class="sxs-lookup"><span data-stu-id="3c02f-109">Marshals output arguments (packages the arguments into the transmitted forms).</span></span>

<span data-ttu-id="3c02f-110">Le compilateur MIDL bascule [**/Server**](-server.md), [**/sstub**](-sstub.md)et [**/out**](-out.md) sur le fichier stub du serveur.</span><span class="sxs-lookup"><span data-stu-id="3c02f-110">The MIDL compiler switches [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

 

 




