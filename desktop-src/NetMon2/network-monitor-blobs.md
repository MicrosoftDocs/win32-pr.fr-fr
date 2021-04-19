---
description: Le Moniteur réseau objet BLOB (Binary Large Object) est une structure de données générique qui contient des informations de configuration et d’emplacement de cartes d’interface réseau (NIC).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: Objets BLOB Moniteur réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538950"
---
# <a name="network-monitor-blobs"></a><span data-ttu-id="79567-103">Objets BLOB Moniteur réseau</span><span class="sxs-lookup"><span data-stu-id="79567-103">Network Monitor BLOBs</span></span>

<span data-ttu-id="79567-104">Le Moniteur réseau objet BLOB (Binary Large Object) est une structure de données générique qui contient des informations de configuration et d’emplacement de cartes d’interface réseau (NIC).</span><span class="sxs-lookup"><span data-stu-id="79567-104">The Network Monitor binary large object (BLOB) is a generic data structure that contains configuration and location information of network interface cards (NICs).</span></span> <span data-ttu-id="79567-105">Utilisez des objets BLOB pour représenter des cartes réseau et filtrer les entrées d’une liste de cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="79567-105">Use BLOBs to represent NICs and to filter entries in a list of NICs.</span></span> <span data-ttu-id="79567-106">Les objets BLOB peuvent également contenir des données spécifiques à l’application sans affecter les autres données qu’ils contiennent.</span><span class="sxs-lookup"><span data-stu-id="79567-106">BLOBS can also contain application-specific data without affecting the other data that they hold.</span></span> <span data-ttu-id="79567-107">L’implémentation d’objet BLOB est opaque à tous les niveaux qui doivent accéder aux objets BLOB avec les API d’objets BLOB.</span><span class="sxs-lookup"><span data-stu-id="79567-107">BLOB implementation is opaque to all levels that must access BLOBs with BLOB APIs.</span></span>

## <a name="blob-structure"></a><span data-ttu-id="79567-108">Structure d’objet BLOB</span><span class="sxs-lookup"><span data-stu-id="79567-108">BLOB Structure</span></span>

<span data-ttu-id="79567-109">Un objet BLOB peut être considéré comme une arborescence hiérarchique utilisée pour désigner des chaînes.</span><span class="sxs-lookup"><span data-stu-id="79567-109">A BLOB can be considered as a hierarchical tree used to designate strings.</span></span> <span data-ttu-id="79567-110">Cette arborescence comporte trois couches : propriétaire, catégorie et étiquette.</span><span class="sxs-lookup"><span data-stu-id="79567-110">This tree has three layers: Owner, Category, and Tag.</span></span> <span data-ttu-id="79567-111">Owner est une chaîne qui indique, en général, qui lit une entrée.</span><span class="sxs-lookup"><span data-stu-id="79567-111">Owner is a string that indicates, in general, who reads an entry.</span></span> <span data-ttu-id="79567-112">La catégorie est également une chaîne, qui désigne un regroupement fonctionnel général de balises sous le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="79567-112">The Category is also a string, which designates a general functional grouping of tags under the owner.</span></span> <span data-ttu-id="79567-113">La balise est le nom réel de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="79567-113">The Tag is the actual name of the entry.</span></span>

<span data-ttu-id="79567-114">Les caractéristiques structurelles des objets BLOB sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="79567-114">The structural characteristics of BLOBs include:</span></span>

-   <span data-ttu-id="79567-115">Les applications auxiliaires d’objets BLOB dans un processus sont protégées les unes des autres par un mutex intégré à chaque objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="79567-115">BLOB helpers within one process are protected from one another by a mutex built into each BLOB.</span></span>
-   <span data-ttu-id="79567-116">Chaque objet BLOB a un numéro de version interne afin que les applications d’assistance puissent gérer à la fois les formulaires BLOB présents et futurs.</span><span class="sxs-lookup"><span data-stu-id="79567-116">Each BLOB has an internal version number so that the helpers can handle both present and future BLOB forms.</span></span> <span data-ttu-id="79567-117">Des conflits de version peuvent se produire si vous envoyez un objet BLOB à un autre ordinateur par le biais d’un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="79567-117">Version conflicts may occur if you send a BLOB to another computer via a remote procedure call.</span></span>
-   <span data-ttu-id="79567-118">L’objet BLOB lui-même est un pointeur vers une valeur void.</span><span class="sxs-lookup"><span data-stu-id="79567-118">The BLOB itself is a pointer to a void.</span></span> <span data-ttu-id="79567-119">Sachez que les applications doivent allouer des objets BLOB avec le modificateur **const** pour éviter de modifier le contenu.</span><span class="sxs-lookup"><span data-stu-id="79567-119">Be aware that applications should allocate BLOBs with the **const** modifier to avoid altering the contents.</span></span>
-   <span data-ttu-id="79567-120">Chacun des indicateurs, ainsi que leurs valeurs, sont des chaînes.</span><span class="sxs-lookup"><span data-stu-id="79567-120">Each of the designators, as well as their values, are strings.</span></span> <span data-ttu-id="79567-121">N’oubliez pas que les chaînes retournées par les fonctions **GetString** sont en fait des pointeurs dans l’objet BLOB et qu’elles ne doivent pas être modifiées.</span><span class="sxs-lookup"><span data-stu-id="79567-121">Be aware that the strings returned by **GetString** functions are actually pointers into the BLOB and should not be changed.</span></span> <span data-ttu-id="79567-122">Pour cette raison, ces chaînes doivent être spécifiées en tant que **const char** _ \_ PX \* pour empêcher les applications de les modifier accidentellement.</span><span class="sxs-lookup"><span data-stu-id="79567-122">For this reason, these strings must be specified as **const char** _\_pX\* to keep applications from accidentally changing them.</span></span>

<span data-ttu-id="79567-123">En général, tous les paramètres avec le désignateur **const** encouragent l’appelant à s’abstenir de modifier les valeurs plutôt que d’interdire la modification des fonctions d’assistance.</span><span class="sxs-lookup"><span data-stu-id="79567-123">In general, all parameters with the **const** designator encourage the caller to refrain from changing the values rather than prohibit the helper functions from changing them.</span></span> <span data-ttu-id="79567-124">En fait, les fonctions d’assistance modifient généralement ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="79567-124">In fact, the helper functions will usually change those values.</span></span>

 

 



