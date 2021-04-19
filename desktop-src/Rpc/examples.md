---
title: Exemples (RPC)
description: Exemples qui illustrent les concepts de l’appel de procédure distante (RPC).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- Appel de procédure distante RPC, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a814d78afbfc7fefa979c890cbbb8c3d4ce0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106510105"
---
# <a name="examples-rpc"></a><span data-ttu-id="f83bb-104">Exemples (RPC)</span><span class="sxs-lookup"><span data-stu-id="f83bb-104">Examples (RPC)</span></span>

<span data-ttu-id="f83bb-105">Le kit de développement logiciel (SDK) de la plateforme contient des exemples qui illustrent un grand nombre de concepts de l’appel de procédure distante (RPC), comme suit :</span><span class="sxs-lookup"><span data-stu-id="f83bb-105">The Platform Software Development Kit (SDK) includes examples that demonstrate a variety of Remote Procedure Call (RPC) concepts, as follows:</span></span>

-   <span data-ttu-id="f83bb-106">ASYNCRPC illustre la structure d’une application RPC qui utilise des appels de procédure distante asynchrones.</span><span class="sxs-lookup"><span data-stu-id="f83bb-106">ASYNCRPC illustrates the structure of an RPC application that uses asynchronous remote procedure calls.</span></span> <span data-ttu-id="f83bb-107">Il montre également différentes méthodes de notification de la fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f83bb-107">It also demonstrates various methods of notification of the call's completion.</span></span>
-   <span data-ttu-id="f83bb-108">CLUUID illustre l’utilisation de l’UUID de l’objet client pour permettre à un client de sélectionner plusieurs implémentations d’une procédure distante.</span><span class="sxs-lookup"><span data-stu-id="f83bb-108">CLUUID demonstrates use of the client-object UUID to enable a client to select from multiple implementations of a remote procedure.</span></span>
-   <span data-ttu-id="f83bb-109">Le répertoire de données contient quatre programmes : DUNION illustre les unions discriminées (qui ne sont pas encapsulées). INOUT montre [ \[ dans \] ](../midl/in.md), [ \[ les \] paramètres out](../midl/out-idl.md) ; REPAS montre l’attribut [dereprésente \_ comme](/windows/desktop/Midl/represent-as) Attribute ; La transmission illustre l’attribut [transmit \_ As](/windows/desktop/Midl/transmit-as) .</span><span class="sxs-lookup"><span data-stu-id="f83bb-109">DATA directory contains four programs: DUNION illustrates discriminated (nonencapsulated) unions; INOUT demonstrates [\[in\]](../midl/in.md), [\[out\]](../midl/out-idl.md) parameters; REPAS demonstrates the [represent\_as](/windows/desktop/Midl/represent-as) attribute; XMIT demonstrates the [transmit\_as](/windows/desktop/Midl/transmit-as) attribute.</span></span>
-   <span data-ttu-id="f83bb-110">DYNEPT illustre une application cliente qui gère sa connexion au serveur via des points de terminaison dynamiques.</span><span class="sxs-lookup"><span data-stu-id="f83bb-110">DYNEPT demonstrates a client application managing its connection to the server through dynamic endpoints.</span></span>
-   <span data-ttu-id="f83bb-111">Le répertoire FILEREP contient quatre exemples illustrant comment les développeurs peuvent écrire un service de réplication de fichiers simple, un service de réplication de fichiers multi-utilisateur, un service prenant en charge les fonctionnalités de sécurité et un service utilisant des canaux RPC asynchrones.</span><span class="sxs-lookup"><span data-stu-id="f83bb-111">FILEREP directory contains four samples illustrating how developers can write a simple file replication service, a multi-user file replication service, a service supporting security features, and a service using RPC asynchronous pipes.</span></span>
-   <span data-ttu-id="f83bb-112">Le répertoire HANDles contient trois programmes, AUTO, CXHNDL, USRDEF, qui illustrent respectivement le descripteur [automatique \_ ](/windows/desktop/Midl/auto-handle), le \[ handle de contexte \_ \] et les handles génériques (définis par l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="f83bb-112">HANDLES directory contains three programs, AUTO, CXHNDL, USRDEF, which demonstrate [auto\_handle](/windows/desktop/Midl/auto-handle), \[context\_handle\], and generic (user-defined) handles, respectively.</span></span>
-   <span data-ttu-id="f83bb-113">HELLO est une implémentation client/serveur de « Hello, World ».</span><span class="sxs-lookup"><span data-stu-id="f83bb-113">HELLO is a client/server implementation of "Hello, world."</span></span>
-   <span data-ttu-id="f83bb-114">Le répertoire PICKLE contient deux programmes : PICKLP illustre la sérialisation des procédures de données ; La liste déroulante illustre la sérialisation des types de données. les deux programmes utilisent les attributs [ \[ encode \] ](../midl/encode.md) et [ \[ Decode \] ](../midl/decode.md) .</span><span class="sxs-lookup"><span data-stu-id="f83bb-114">PICKLE directory contains two programs: PICKLP demonstrates data procedure serialization; PICKLT demonstrates data type serialization; both programs use the [\[encode\]](../midl/encode.md) and [\[decode\]](../midl/decode.md) attributes.</span></span>
-   <span data-ttu-id="f83bb-115">Les canaux illustrent l’utilisation du constructeur de type pipe.</span><span class="sxs-lookup"><span data-stu-id="f83bb-115">PIPES demonstrates the use of the pipe-type constructor.</span></span>
-   <span data-ttu-id="f83bb-116">RPCSVC illustre l’implémentation d’un service avec RPC.</span><span class="sxs-lookup"><span data-stu-id="f83bb-116">RPCSVC demonstrates the implementation of a service with RPC.</span></span>
-   <span data-ttu-id="f83bb-117">STROUT montre comment allouer de la mémoire sur un serveur pour un objet à deux dimensions (un tableau de pointeurs) et le retourner au client en tant \[ que \] paramètre en sortie seule.</span><span class="sxs-lookup"><span data-stu-id="f83bb-117">STROUT demonstrates how to allocate memory at a server for a two-dimensional object (an array of pointers) and pass it back to the client as an \[out\]-only parameter.</span></span> <span data-ttu-id="f83bb-118">Le client libère ensuite la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f83bb-118">The client then frees the memory.</span></span> <span data-ttu-id="f83bb-119">Cette technique permet au stub d’appeler le serveur sans savoir à l’avance la quantité de données qui sera retournée.</span><span class="sxs-lookup"><span data-stu-id="f83bb-119">This technique allows the stub to call the server without knowing in advance how much data will be returned.</span></span>

    <span data-ttu-id="f83bb-120">Ce programme permet également à l’utilisateur d’effectuer une compilation pour UNICODE ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="f83bb-120">This program also allows the user to compile either for UNICODE or ANSI.</span></span>

<span data-ttu-id="f83bb-121">Tous les fichiers sources et makefiles pour ces programmes se trouvent dans le kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="f83bb-121">All of the source files and makefiles for these programs are located in the Platform SDK.</span></span>

<span data-ttu-id="f83bb-122">Pour un développement d’applications RPC de base et des exemples plus simples, consultez les rubriques du [didacticiel](tutorial.md) .</span><span class="sxs-lookup"><span data-stu-id="f83bb-122">For basic RPC application development and simpler examples, please see the [Tutorial](tutorial.md) topics.</span></span>

 

 
