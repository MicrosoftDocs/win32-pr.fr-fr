---
title: Attributs de type de données
description: Vous pouvez appliquer ces attributs aux types de données dans une instruction typedef pour définir plus précisément l’utilisation ou l’effet du type de données.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- IDL MIDL, attributs, type de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675778"
---
# <a name="data-type-attributes"></a><span data-ttu-id="7ad12-104">Attributs de type de données</span><span class="sxs-lookup"><span data-stu-id="7ad12-104">Data Type Attributes</span></span>

<span data-ttu-id="7ad12-105">Vous pouvez appliquer ces attributs aux types de données dans une instruction [**typedef**](typedef.md) pour définir plus précisément l’utilisation ou l’effet du type de données.</span><span class="sxs-lookup"><span data-stu-id="7ad12-105">You can apply these attributes to data types in a [**typedef**](typedef.md) statement to further define the usage or effect of the data type.</span></span>



| <span data-ttu-id="7ad12-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="7ad12-106">Attribute</span></span>                                 | <span data-ttu-id="7ad12-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="7ad12-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ad12-108">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="7ad12-108">**context\_handle**</span></span>](context-handle.md) | <span data-ttu-id="7ad12-109">Identifie un handle de liaison qui gère les informations d’État (contexte) sur un serveur particulier entre les appels de procédure distante d’un client particulier.</span><span class="sxs-lookup"><span data-stu-id="7ad12-109">Identifies a binding handle that maintains state (context) information on a particular server between remote procedure calls from a particular client.</span></span> <span data-ttu-id="7ad12-110">Non valide pour les fonctions d’interface d' [**objet**](object.md) .</span><span class="sxs-lookup"><span data-stu-id="7ad12-110">Not valid for [**object**](object.md) interface functions.</span></span>                                                                                                         |
| [<span data-ttu-id="7ad12-111">**traitée**</span><span class="sxs-lookup"><span data-stu-id="7ad12-111">**handle**</span></span>](handle.md)                  | <span data-ttu-id="7ad12-112">Spécifie un type de handle personnalisé propre à l’application.</span><span class="sxs-lookup"><span data-stu-id="7ad12-112">Specifies a custom handle type specific to the application.</span></span>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="7ad12-113">**MS \_ Union**</span><span class="sxs-lookup"><span data-stu-id="7ad12-113">**ms\_union**</span></span>](-ms-union.md)            | <span data-ttu-id="7ad12-114">Contrôle l’alignement du rapport de non-remise des unions non encapsulées.</span><span class="sxs-lookup"><span data-stu-id="7ad12-114">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="7ad12-115">Utilisez sur [**typedef**](typedef.md)s pour la compatibilité descendante avec les interfaces générées avec MIDL 1,0 ou 2,0.</span><span class="sxs-lookup"><span data-stu-id="7ad12-115">Use on [**typedef**](typedef.md)s for backward compatibility with interfaces built with MIDL 1.0 or 2.0.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="7ad12-116">**canal**</span><span class="sxs-lookup"><span data-stu-id="7ad12-116">**pipe**</span></span>](pipe.md)                      | <span data-ttu-id="7ad12-117">Autorise la transmission d’un flux ouvert de données typées à travers un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="7ad12-117">Allows transmission of an open-ended stream of typed data across a remote procedure call.</span></span> <span data-ttu-id="7ad12-118">Un paramètre [**in**](in.md) pipe permet au serveur d’extraire le flux de données du client pendant un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="7ad12-118">An [**in**](in.md) pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="7ad12-119">Un paramètre de [**sortie**](-out.md) de canal permet au serveur d’envoyer à nouveau le flux de données au client.</span><span class="sxs-lookup"><span data-stu-id="7ad12-119">An [**out**](-out.md) pipe parameter allows the server to push the data stream back to the client.</span></span> |
| [<span data-ttu-id="7ad12-120">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="7ad12-120">**transmit\_as**</span></span>](transmit-as.md)       | <span data-ttu-id="7ad12-121">Spécifie la manière dont un type de données sera transmis sur un réseau, utilisé pour le marshaling personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7ad12-121">Specifies how a data type will be transmitted over a network, used for custom marshaling.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7ad12-122">**\_enum v1**</span><span class="sxs-lookup"><span data-stu-id="7ad12-122">**v1\_enum**</span></span>](v1-enum.md)               | <span data-ttu-id="7ad12-123">Indique que le type énuméré spécifié doit être transmis en tant qu’entité 32 bits, au lieu de la valeur par défaut 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7ad12-123">Directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>                                                                                                                                                                                                              |
| [<span data-ttu-id="7ad12-124">**Marshal de câble \_**</span><span class="sxs-lookup"><span data-stu-id="7ad12-124">**wire\_marshal**</span></span>](wire-marshal.md)     | <span data-ttu-id="7ad12-125">Semblable à [**transmit \_ As**](transmit-as.md) , mais vous implémentez les routines de dimensionnement, de marshaler, de démarshaler et de libération des données.</span><span class="sxs-lookup"><span data-stu-id="7ad12-125">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span>                                                                                                                                                                                              |



 

 

 




