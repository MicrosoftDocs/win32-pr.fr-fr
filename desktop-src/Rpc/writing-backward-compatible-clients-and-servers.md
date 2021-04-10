---
title: Écriture de clients et de serveurs à compatibilité descendante
description: En théorie, le schéma de contrôle de version de RPC permet d’éviter une communication inversée entre les serveurs et les clients modifiés et leurs homologues déployés.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- RPC appel de procédure distante, meilleures pratiques, compatibilité descendante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100665"
---
# <a name="writing-backward-compatible-clients-and-servers"></a><span data-ttu-id="e3e7a-104">Écriture de clients et de serveurs à compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="e3e7a-104">Writing Backward Compatible Clients and Servers</span></span>

<span data-ttu-id="e3e7a-105">En théorie, le schéma de contrôle de version de RPC permet d’éviter une communication inversée entre les serveurs et les clients modifiés et leurs homologues déployés.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-105">In theory, the versioning scheme of RPC helps prevent miscommunication between modified servers and clients and their deployed counterparts.</span></span> <span data-ttu-id="e3e7a-106">En pratique, toutefois, les développeurs doivent souvent introduire des modifications dans les interfaces existantes sans modifier la version, car les clients et les serveurs précédents doivent être en mesure de communiquer avec eux.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-106">In practice, however, developers frequently must introduce changes to existing interfaces without modifying the version, because previous clients and servers must be able to communicate with new ones.</span></span> <span data-ttu-id="e3e7a-107">Il s’agit d’un problème plus important pour RPC standard que pour COM ; l’interrogation est un moyen naturel de rechercher des interfaces prises en charge dans COM, tandis que dans la gestion des exceptions RPC doit être utilisé pour une couverture équivalente.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-107">This is a larger issue for standard RPC than for COM; querying is a natural way of searching for supported interfaces in COM, while in RPC exception handling must be used for equivalent coverage.</span></span>

<span data-ttu-id="e3e7a-108">Cette section décrit les meilleures pratiques de programmation RPC pour traiter ces situations.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-108">This section discusses the best RPC programming practices for addressing these situations.</span></span> <span data-ttu-id="e3e7a-109">Cette section est composée des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3e7a-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="e3e7a-110">La théorie de la gestion des versions pour RPC et COM</span><span class="sxs-lookup"><span data-stu-id="e3e7a-110">The Versioning Theory for RPC and COM</span></span>](the-versioning-theory-for-rpc-and-com.md)
-   [<span data-ttu-id="e3e7a-111">Modification des interfaces d’une manière à compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="e3e7a-111">Changing Interfaces in a Backward Compatible Manner</span></span>](changing-interfaces-in-a-backward-compatible-manner.md)
-   [<span data-ttu-id="e3e7a-112">Exemples de modifications incompatibles</span><span class="sxs-lookup"><span data-stu-id="e3e7a-112">Examples of Incompatible Changes</span></span>](examples-of-incompatible-changes.md)

 

 




