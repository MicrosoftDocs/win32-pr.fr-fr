---
title: Interfaces dans les objets distribués
description: Dans l’informatique distribuée, une interface est une collection de définitions et de fonctions distantes qui permettent à plusieurs programmes d’interagir entre différents contextes.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- interfaces MIDL, dans les objets distribués
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314993"
---
# <a name="interfaces-in-distributed-objects"></a><span data-ttu-id="2bb41-104">Interfaces dans les objets distribués</span><span class="sxs-lookup"><span data-stu-id="2bb41-104">Interfaces in Distributed Objects</span></span>

<span data-ttu-id="2bb41-105">Dans l’informatique distribuée, une interface est une collection de définitions et de fonctions distantes qui permettent à plusieurs programmes d’interagir entre différents contextes.</span><span class="sxs-lookup"><span data-stu-id="2bb41-105">In distributed computing, an interface is a collection of definitions and remote functions that enables two or more programs to interoperate between different contexts.</span></span> <span data-ttu-id="2bb41-106">Dans une application RPC, une interface spécifie les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2bb41-106">In an RPC application, an interface specifies:</span></span>

-   <span data-ttu-id="2bb41-107">Comment les applications client et serveur s’identifient les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="2bb41-107">How client and server applications identify themselves to each other.</span></span>
-   <span data-ttu-id="2bb41-108">Mode de transmission des données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="2bb41-108">How data is transmitted between client and server.</span></span>
-   <span data-ttu-id="2bb41-109">Procédures distantes que l’application cliente peut appeler.</span><span class="sxs-lookup"><span data-stu-id="2bb41-109">Remote procedures that the client application can call.</span></span>
-   <span data-ttu-id="2bb41-110">Types de données pour les paramètres et les valeurs de retour des procédures distantes.</span><span class="sxs-lookup"><span data-stu-id="2bb41-110">Data types for the parameters and return values of the remote procedures.</span></span>

<span data-ttu-id="2bb41-111">Le Microsoft Interface Definition Language (MIDL) est destiné à l’implémentation des interfaces utilisées dans les applications distribuées.</span><span class="sxs-lookup"><span data-stu-id="2bb41-111">The Microsoft Interface Definition Language (MIDL) is for implementing interfaces used in distributed applications.</span></span> <span data-ttu-id="2bb41-112">Avec MIDL, une application peut avoir une interface ou plusieurs.</span><span class="sxs-lookup"><span data-stu-id="2bb41-112">With MIDL, an application can have one interface or many.</span></span> <span data-ttu-id="2bb41-113">Chaque interface spécifie un contrat distribué unique entre les programmes client et serveur.</span><span class="sxs-lookup"><span data-stu-id="2bb41-113">Each interface specifies a unique distributed contract between the client and server programs.</span></span> <span data-ttu-id="2bb41-114">Les applications basées sur des appels de procédure distante (RPC), COM (Component Object Model) et DCOM (Distributed Component Object Model) spécifient leurs interfaces à l’aide de MIDL.</span><span class="sxs-lookup"><span data-stu-id="2bb41-114">Applications based on remote procedure calls (RPC), Component Object Model (COM), and Distributed Component Object Model (DCOM) specify their interfaces using MIDL.</span></span>

<span data-ttu-id="2bb41-115">MIDL ressemble à C et C++ de nombreuses façons.</span><span class="sxs-lookup"><span data-stu-id="2bb41-115">MIDL resembles C and C++ in many ways.</span></span> <span data-ttu-id="2bb41-116">Pour obtenir une vue d’ensemble de l’écriture d’interfaces MIDL, consultez [développement de l’interface](/windows/desktop/Rpc/developing-the-interface).</span><span class="sxs-lookup"><span data-stu-id="2bb41-116">For an overview of writing MIDL interfaces, see [Developing the Interface](/windows/desktop/Rpc/developing-the-interface).</span></span>

 

 