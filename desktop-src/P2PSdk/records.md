---
description: Les enregistrements sont un moyen de communiquer entre les nœuds d’un graphique ou les membres d’un groupe.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Enregistrements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952510"
---
# <a name="records"></a><span data-ttu-id="a77e4-103">Enregistrements</span><span class="sxs-lookup"><span data-stu-id="a77e4-103">Records</span></span>

<span data-ttu-id="a77e4-104">Les enregistrements sont un moyen de communiquer entre les nœuds d’un graphique ou les membres d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="a77e4-104">Records are a way to communicate between nodes in a graph or members in a group.</span></span> <span data-ttu-id="a77e4-105">Un enregistrement se compose des deux parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="a77e4-105">A record consists of the following two parts:</span></span>

-   <span data-ttu-id="a77e4-106">En-tête d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="a77e4-106">Record header</span></span>
-   <span data-ttu-id="a77e4-107">Contenu de données opaque spécifique</span><span class="sxs-lookup"><span data-stu-id="a77e4-107">Specific opaque data content</span></span>

<span data-ttu-id="a77e4-108">L’en-tête contient des informations sur l’enregistrement, notamment la version, le créateur et le type de données publiées.</span><span class="sxs-lookup"><span data-stu-id="a77e4-108">The header contains information about the record, including the version, creator, and type of data being published.</span></span> <span data-ttu-id="a77e4-109">L’en-tête contient également un champ d’attributs XML qui permet aux applications d’ajouter des attributs nom-valeur qui décrivent les données, et de rechercher efficacement dans la base de données d’enregistrement des enregistrements spécifiques qui ont été publiés précédemment.</span><span class="sxs-lookup"><span data-stu-id="a77e4-109">The header also contains an XML attributes field that allows applications to add name-value attributes that describe the data, and to efficiently search the record database for specific records that have previously been published.</span></span> <span data-ttu-id="a77e4-110">Le contenu est les données définies par l’application et est opaque pour l’infrastructure de l’homologue.</span><span class="sxs-lookup"><span data-stu-id="a77e4-110">The content is the application-defined data, and is opaque to the Peer Infrastructure.</span></span>

<span data-ttu-id="a77e4-111">Lorsqu’un enregistrement est publié, il (en-tête et données) est inondé dans le graphique ou le groupe.</span><span class="sxs-lookup"><span data-stu-id="a77e4-111">When a record is published, it (both header and data) is flooded throughout the graph or group.</span></span> <span data-ttu-id="a77e4-112">Les homologues synchronisés reçoivent ces données et les stockent dans une base de données locale.</span><span class="sxs-lookup"><span data-stu-id="a77e4-112">Synchronized peers receive this data and store it in a local database.</span></span> <span data-ttu-id="a77e4-113">Les homologues non synchronisés et hors connexion reçoivent les données la prochaine fois qu’ils se connectent et se synchronisent avec le graphique ou le groupe d’homologues.</span><span class="sxs-lookup"><span data-stu-id="a77e4-113">Unsynchronized and offline peers receive the data the next time they connect and synchronize with the peer graph or group.</span></span>

<span data-ttu-id="a77e4-114">Pour plus d’informations sur l’utilisation des enregistrements, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a77e4-114">For information about working with records, see the following topics:</span></span>

-   [<span data-ttu-id="a77e4-115">Dépendances d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="a77e4-115">Record Dependencies</span></span>](record-dependencies.md)
-   [<span data-ttu-id="a77e4-116">Gestion des enregistrements</span><span class="sxs-lookup"><span data-stu-id="a77e4-116">Record Management</span></span>](record-management.md)
-   [<span data-ttu-id="a77e4-117">Schéma d’attribut d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="a77e4-117">Record Attribute Schema</span></span>](record-attribute-schema.md)
-   [<span data-ttu-id="a77e4-118">Format de requête de recherche d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="a77e4-118">Record Search Query Format</span></span>](record-search-query-format.md)

 

 



