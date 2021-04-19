---
description: Le langage de requête de recherche Microsoft Windows est basé sur langage SQL (SQL); Toutefois, il n’effectue pas de recherches dans une base de données relationnelle avec des tables ou des index définis par l’utilisateur.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Fonctionnalités SQL non disponibles dans Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514587"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a><span data-ttu-id="3d91d-103">Fonctionnalités SQL non disponibles dans Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="3d91d-103">SQL Features Unavailable in Microsoft Windows Search</span></span>

<span data-ttu-id="3d91d-104">Le langage de requête de recherche Microsoft Windows est basé sur langage SQL (SQL); Toutefois, il n’effectue pas de recherches dans une base de données relationnelle avec des tables ou des index définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3d91d-104">Microsoft Windows Search query language is based on Structured Query Language (SQL); however, it does not search in a relational database with user-defined tables or indexes.</span></span> <span data-ttu-id="3d91d-105">Pour cette raison, de nombreuses instructions SQL standard et fonctionnalités de syntaxe ne s’appliquent pas.</span><span class="sxs-lookup"><span data-stu-id="3d91d-105">Because of this, many standard SQL statements and syntax features do not apply.</span></span> <span data-ttu-id="3d91d-106">La liste suivante répertorie les fonctionnalités SQL les plus significatives qui ne sont pas prises en charge dans Windows Search.</span><span class="sxs-lookup"><span data-stu-id="3d91d-106">The following is a list of the more significant SQL features that are not supported in Windows Search.</span></span>


-   <span data-ttu-id="3d91d-107">Instructions BATCH</span><span class="sxs-lookup"><span data-stu-id="3d91d-107">BATCH statements</span></span>
-   <span data-ttu-id="3d91d-108">\_Fonction de table COALESCE</span><span class="sxs-lookup"><span data-stu-id="3d91d-108">COALESCE\_TABLE function</span></span>
-   <span data-ttu-id="3d91d-109">CONVERT, fonction (utilisez à la place les fonctions CAST)</span><span class="sxs-lookup"><span data-stu-id="3d91d-109">CONVERT function (use the CAST functions instead)</span></span>
-   <span data-ttu-id="3d91d-110">CREATE VIEW (instruction)</span><span class="sxs-lookup"><span data-stu-id="3d91d-110">CREATE VIEW statement</span></span>
-   <span data-ttu-id="3d91d-111">Langage de définition de données</span><span class="sxs-lookup"><span data-stu-id="3d91d-111">Data definition language</span></span>
-   <span data-ttu-id="3d91d-112">DATASOURCE (instruction)</span><span class="sxs-lookup"><span data-stu-id="3d91d-112">DATASOURCE statement</span></span>
-   <span data-ttu-id="3d91d-113">Formats de date et d’heure autres que l’horodatage ISO</span><span class="sxs-lookup"><span data-stu-id="3d91d-113">Date and Time formats other than ISO date and time stamp</span></span>
-   <span data-ttu-id="3d91d-114">Instruction DELETE</span><span class="sxs-lookup"><span data-stu-id="3d91d-114">DELETE statement</span></span>
-   <span data-ttu-id="3d91d-115">GRANT, instruction</span><span class="sxs-lookup"><span data-stu-id="3d91d-115">GRANT statement</span></span>
-   <span data-ttu-id="3d91d-116">Schéma d’informations</span><span class="sxs-lookup"><span data-stu-id="3d91d-116">Information schema</span></span>
-   <span data-ttu-id="3d91d-117">Instruction INSERT</span><span class="sxs-lookup"><span data-stu-id="3d91d-117">INSERT statement</span></span>
-   <span data-ttu-id="3d91d-118">Types de données OLE DB</span><span class="sxs-lookup"><span data-stu-id="3d91d-118">OLE DB data types</span></span>
-   <span data-ttu-id="3d91d-119">Expressions régulières standard SQL (utilisez CONTAINs ou LIKE à la place)</span><span class="sxs-lookup"><span data-stu-id="3d91d-119">SQL-standard regular expressions (use CONTAINS or LIKE instead)</span></span>
-   <span data-ttu-id="3d91d-120">Paramètres pour les requêtes SQL</span><span class="sxs-lookup"><span data-stu-id="3d91d-120">Parameters to SQL queries</span></span>
-   <span data-ttu-id="3d91d-121">Comparaison des colonnes relationnelles</span><span class="sxs-lookup"><span data-stu-id="3d91d-121">Relational column comparison</span></span>
-   <span data-ttu-id="3d91d-122">En-tête ID de révision</span><span class="sxs-lookup"><span data-stu-id="3d91d-122">Revision ID header</span></span>
-   <span data-ttu-id="3d91d-123">REVOKE, instruction</span><span class="sxs-lookup"><span data-stu-id="3d91d-123">REVOKE statement</span></span>
-   <span data-ttu-id="3d91d-124">Alias d’étendue ou numéros de révision</span><span class="sxs-lookup"><span data-stu-id="3d91d-124">SCOPE aliases or revision numbers</span></span>
-   <span data-ttu-id="3d91d-125">Sélectionner tout (supprime automatiquement les doublons)</span><span class="sxs-lookup"><span data-stu-id="3d91d-125">SELECT ALL (removes duplicates automatically)</span></span>
-   <span data-ttu-id="3d91d-126">Procédures stockées</span><span class="sxs-lookup"><span data-stu-id="3d91d-126">Stored procedures</span></span>
-   <span data-ttu-id="3d91d-127">Développement de documents structurés</span><span class="sxs-lookup"><span data-stu-id="3d91d-127">Structured document expansion</span></span>
-   <span data-ttu-id="3d91d-128">UNION ALL</span><span class="sxs-lookup"><span data-stu-id="3d91d-128">UNION ALL</span></span>
-   <span data-ttu-id="3d91d-129">Mot clé Unknown</span><span class="sxs-lookup"><span data-stu-id="3d91d-129">UNKNOWN keyword</span></span>
-   <span data-ttu-id="3d91d-130">Instruction UPDATE</span><span class="sxs-lookup"><span data-stu-id="3d91d-130">UPDATE statement</span></span>

<span data-ttu-id="3d91d-131">Windows Search ne prend pas en charge les dictionnaires des synonymes et les mots parasites.</span><span class="sxs-lookup"><span data-stu-id="3d91d-131">Windows Search does not support Thesaurus and Noise Words.</span></span>

 

 



