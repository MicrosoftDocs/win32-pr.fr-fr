---
title: Définition de répertoire
description: L’exemple de composant de fournisseur utilise une conception d’annuaire relativement simple pour clarifier la relation entre les composants et pour indiquer les conditions minimales requises pour être un fournisseur ADSI.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6156f2e1ab89b34f009f1a86e5de011c20cf9503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839209"
---
# <a name="directory-definition"></a><span data-ttu-id="4c628-103">Définition de répertoire</span><span class="sxs-lookup"><span data-stu-id="4c628-103">Directory Definition</span></span>

<span data-ttu-id="4c628-104">L’exemple de composant de fournisseur utilise une conception d’annuaire relativement simple pour clarifier la relation entre les composants et pour indiquer les conditions minimales requises pour être un fournisseur ADSI.</span><span class="sxs-lookup"><span data-stu-id="4c628-104">The example provider component uses a relatively simple directory design to clarify the relationship between components and to show the minimum requirements necessary to be an ADSI provider.</span></span>

<span data-ttu-id="4c628-105">Le « répertoire » du composant de fournisseur d’exemple se compose de deux nœuds racine : « Seattle » et « Toronto ».</span><span class="sxs-lookup"><span data-stu-id="4c628-105">The "directory" for the example provider component consists of two root nodes: "Seattle" and "Toronto".</span></span> <span data-ttu-id="4c628-106">Seattle contient deux autres sous-niveaux, « Bellevue » et « Redmond ».</span><span class="sxs-lookup"><span data-stu-id="4c628-106">Seattle contains two more sublevels, "Bellevue" and "Redmond".</span></span> <span data-ttu-id="4c628-107">Chacune de ces entrées contient plusieurs comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c628-107">Each of these entries contains several user accounts.</span></span> <span data-ttu-id="4c628-108">L’entrée « Toronto » n’a pas de sous-niveaux supplémentaires, mais elle contient directement plusieurs comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c628-108">The "Toronto" entry has no further sublevels, but directly contains several user accounts.</span></span> <span data-ttu-id="4c628-109">L’illustration suivante montre ces deux nœuds racines connectés à un réseau.</span><span class="sxs-lookup"><span data-stu-id="4c628-109">The following figure shows these two root nodes connected to a network.</span></span>

![définition de répertoire](images/dssmdo.png)

<span data-ttu-id="4c628-111">En termes hiérarchiques, le nœud d’espace de noms contient « Seattle » et « Toronto ».</span><span class="sxs-lookup"><span data-stu-id="4c628-111">In hierarchical terms, the Namespace node contains "Seattle" and "Toronto".</span></span> <span data-ttu-id="4c628-112">« Seattle » contient « Bellevue » et « Redmond ».</span><span class="sxs-lookup"><span data-stu-id="4c628-112">"Seattle" contains "Bellevue" and "Redmond".</span></span> <span data-ttu-id="4c628-113">« Bellevue » et « Redmond » contiennent chacun un ensemble de comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c628-113">"Bellevue" and "Redmond" each contain a set of user accounts.</span></span> <span data-ttu-id="4c628-114">« Toronto » contient directement les comptes d’utilisateur sans nœuds organisationnels intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="4c628-114">"Toronto" directly contains the user accounts with no intermediate organizational nodes.</span></span>

<span data-ttu-id="4c628-115">Le composant de fournisseur d’exemple représente cette structure avec uniquement deux types d’objets Active Directory : un objet conteneur et un objet feuille.</span><span class="sxs-lookup"><span data-stu-id="4c628-115">The example provider component represents this structure with only two Active Directory object types: a container object and a leaf object.</span></span> <span data-ttu-id="4c628-116">« Seattle », « Toronto », « Bellevue » et « Redmond » sont des objets conteneurs et chaque compte d’utilisateur est un objet feuille.</span><span class="sxs-lookup"><span data-stu-id="4c628-116">"Seattle", "Toronto", "Bellevue", and "Redmond" are container objects and each user account is a leaf object.</span></span>

<span data-ttu-id="4c628-117">L’exemple de composant fournisseur crée une classe de schéma appelée « unité d’organisation » pour un type d’objet conteneur et une classe de schéma appelée « utilisateur » pour un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c628-117">The example provider component creates a schema class called "Organizational Unit" for a container object type and a schema class called "User" for a user account.</span></span>

<span data-ttu-id="4c628-118">Les propriétés de chaque classe de schéma, leurs méthodes et les règles qui régissent les relations d’imbrication pour ces objets sont toutes définies dans la [gestion des schémas](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="4c628-118">The properties for each schema class, their methods, and the rules that govern the containment relationships for these objects are all defined in [Schema Management](schema-management.md).</span></span>

 

 




