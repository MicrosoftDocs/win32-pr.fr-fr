---
title: C (RPC)
description: Mots commençant par C dans le glossaire de l’appel de procédure distante (RPC).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: da1ee843-c33e-42a1-bcaf-6cdb4834e70b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15eb37af87fd36dd31f3e9e106904b4ce734c15
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103941604"
---
# <a name="c-rpc"></a><span data-ttu-id="b3977-103">C (RPC)</span><span class="sxs-lookup"><span data-stu-id="b3977-103">C (RPC)</span></span>

<span data-ttu-id="b3977-104">[A](a-glos.md) [B](b-glos.md) C [D](d-glos.md) [e](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="b3977-104">[A](a-glos.md) [B](b-glos.md) C [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="b3977-105"><span id="_rpc_cds_glos"></span><span id="_RPC_CDS_GLOS"></span>**Service d’annuaire de cellules/service d’annuaires de cellules (CDS)**</span><span class="sxs-lookup"><span data-stu-id="b3977-105"><span id="_rpc_cds_glos"></span><span id="_RPC_CDS_GLOS"></span>**Cell Directory Service (CDS)**</span></span>
</dt> <dd>

<span data-ttu-id="b3977-106">Nom : fournisseur de services de l’environnement informatique distribué Open Software Foundation.</span><span class="sxs-lookup"><span data-stu-id="b3977-106">Name-service provider for the Open Software Foundation's Distributed Computing Environment.</span></span>

</dd> <dt>

<span data-ttu-id="b3977-107"><span id="_rpc_client_stub_glos"></span><span id="_RPC_CLIENT_STUB_GLOS"></span>**stub client**</span><span class="sxs-lookup"><span data-stu-id="b3977-107"><span id="_rpc_client_stub_glos"></span><span id="_RPC_CLIENT_STUB_GLOS"></span>**client stub**</span></span>
</dt> <dd>

<span data-ttu-id="b3977-108">Code source du langage C généré par MIDL.</span><span class="sxs-lookup"><span data-stu-id="b3977-108">MIDL-generated C-language source code.</span></span> <span data-ttu-id="b3977-109">Il contient toutes les fonctions nécessaires à l’application cliente pour effectuer des appels de procédure distante à l’aide du modèle d’appel de fonction traditionnel dans une application autonome.</span><span class="sxs-lookup"><span data-stu-id="b3977-109">It contains all the functions necessary for the client application to make remote procedure calls using the model of a traditional function call in a standalone application.</span></span> <span data-ttu-id="b3977-110">Le stub client est chargé de marshaler les paramètres d’entrée et de démarshaler les paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="b3977-110">The client stub is responsible for marshaling input parameters and unmarshaling output parameters.</span></span> <span data-ttu-id="b3977-111">Voir aussi [*stub de serveur*](s-glos.md), [*stub proxy*](p-glos.md).</span><span class="sxs-lookup"><span data-stu-id="b3977-111">See also [*server stub*](s-glos.md), [*proxy stub*](p-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3977-112"><span id="_rpc_conformant_array_glos"></span><span id="_RPC_CONFORMANT_ARRAY_GLOS"></span>**Tableau conforme**</span><span class="sxs-lookup"><span data-stu-id="b3977-112"><span id="_rpc_conformant_array_glos"></span><span id="_RPC_CONFORMANT_ARRAY_GLOS"></span>**conformant array**</span></span>
</dt> <dd>

<span data-ttu-id="b3977-113">Tableau dont la taille est déterminée au moment de l’exécution par un autre paramètre, un champ de structure ou une expression.</span><span class="sxs-lookup"><span data-stu-id="b3977-113">Array whose size is determined at run time by another parameter, structure field, or expression.</span></span>

</dd> <dt>

<span data-ttu-id="b3977-114"><span id="_rpc_connection_oriented_glos"></span><span id="_RPC_CONNECTION_ORIENTED_GLOS"></span>**orienté connexion**</span><span class="sxs-lookup"><span data-stu-id="b3977-114"><span id="_rpc_connection_oriented_glos"></span><span id="_RPC_CONNECTION_ORIENTED_GLOS"></span>**connection-oriented**</span></span>
</dt> <dd>

<span data-ttu-id="b3977-115">Protocole ou transport de communication qui fournit un circuit virtuel par le biais duquel les paquets de données sont reçus dans le même ordre que celui dans lequel ils ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="b3977-115">Communications protocol or transport that provides a virtual circuit through which data packets are received in the same order as they were transmitted.</span></span> <span data-ttu-id="b3977-116">Si la connexion entre les ordinateurs échoue, l’application est avertie.</span><span class="sxs-lookup"><span data-stu-id="b3977-116">If the connection between computers fails, the application is notified.</span></span> <span data-ttu-id="b3977-117">[*TCP*](t-glos.md) et [*SPX*](s-glos.md) sont des exemples de protocoles orientés connexion.</span><span class="sxs-lookup"><span data-stu-id="b3977-117">[*TCP*](t-glos.md) and [*SPX*](s-glos.md) are examples of connection-oriented protocols.</span></span> <span data-ttu-id="b3977-118">Voir aussi [*datagramme*](d-glos.md).</span><span class="sxs-lookup"><span data-stu-id="b3977-118">See also [*datagram*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3977-119"><span id="_rpc_connectionless_glos"></span><span id="_RPC_CONNECTIONLESS_GLOS"></span>**sans connexion**</span><span class="sxs-lookup"><span data-stu-id="b3977-119"><span id="_rpc_connectionless_glos"></span><span id="_RPC_CONNECTIONLESS_GLOS"></span>**connectionless**</span></span>
</dt> <dd>

<span data-ttu-id="b3977-120">Consultez [*datagramme*](d-glos.md).</span><span class="sxs-lookup"><span data-stu-id="b3977-120">See [*datagram*](d-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3977-121"><span id="_rpc_context_rundown_glos"></span><span id="_RPC_CONTEXT_RUNDOWN_GLOS"></span>**arrêt du contexte**</span><span class="sxs-lookup"><span data-stu-id="b3977-121"><span id="_rpc_context_rundown_glos"></span><span id="_RPC_CONTEXT_RUNDOWN_GLOS"></span>**context rundown**</span></span>
</dt> <dd>

<span data-ttu-id="b3977-122">Notification de serveur qui résulte d’une fin inattendue de la liaison entre les applications client et serveur.</span><span class="sxs-lookup"><span data-stu-id="b3977-122">Server notification that results from an unexpected termination of the binding between client and server applications.</span></span>

</dd> </dl>

 

 




