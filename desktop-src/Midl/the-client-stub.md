---
title: Stub client
description: Le module stub client fournit des points d’entrée de substitution sur le client pour chacune des opérations définies dans le fichier IDL d’entrée.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL et RPC MIDL, interfaces, stub client
- interfaces MIDL
- interfaces MIDL, MIDL et RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310729"
---
# <a name="the-client-stub"></a><span data-ttu-id="423ff-106">Stub client</span><span class="sxs-lookup"><span data-stu-id="423ff-106">The Client Stub</span></span>

<span data-ttu-id="423ff-107">Le module stub client fournit des points d’entrée de substitution sur le client pour chacune des opérations définies dans le fichier IDL d’entrée.</span><span class="sxs-lookup"><span data-stu-id="423ff-107">The client stub module provides surrogate entry points on the client for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="423ff-108">Lorsque l’application cliente effectue un appel à la procédure distante, son appel passe tout d’abord à la routine de substitution dans le fichier stub client.</span><span class="sxs-lookup"><span data-stu-id="423ff-108">When the client application makes a call to the remote procedure, its call first goes to the surrogate routine in the client stub file.</span></span> <span data-ttu-id="423ff-109">La routine stub cliente exécute les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="423ff-109">The client stub routine performs the following functions:</span></span>

-   <span data-ttu-id="423ff-110">Marshale les arguments.</span><span class="sxs-lookup"><span data-stu-id="423ff-110">Marshals arguments.</span></span> <span data-ttu-id="423ff-111">Le stub client empaquette des arguments d’entrée dans un format qui peut être transmis au serveur.</span><span class="sxs-lookup"><span data-stu-id="423ff-111">The client stub packages input arguments into a form that can be transmitted to the server.</span></span>
-   <span data-ttu-id="423ff-112">Appelle la bibliothèque Runtime du client pour transmettre des arguments à l’espace d’adressage distant et appelle la procédure distante dans l’espace d’adressage du serveur.</span><span class="sxs-lookup"><span data-stu-id="423ff-112">Calls the client run-time library to transmit arguments to the remote address space and invokes the remote procedure in the server address space.</span></span>
-   <span data-ttu-id="423ff-113">Démarshale les arguments de sortie.</span><span class="sxs-lookup"><span data-stu-id="423ff-113">Unmarshals output arguments.</span></span> <span data-ttu-id="423ff-114">Le stub client décompresse les arguments de sortie et retourne à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="423ff-114">The client stub unpacks output arguments and returns to the caller.</span></span>

<span data-ttu-id="423ff-115">Le compilateur MIDL bascule [**/client**](-client.md), [**/cstub**](-cstub.md)et [**/out**](-out.md) sur le fichier stub client.</span><span class="sxs-lookup"><span data-stu-id="423ff-115">The MIDL compiler switches [**/client**](-client.md), [**/cstub**](-cstub.md), and [**/out**](-out.md) affect the client stub file.</span></span>

 

 




