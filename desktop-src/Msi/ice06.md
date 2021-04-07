---
description: ICE06 vérifie chaque table pour valider que toutes les colonnes répertoriées dans le \_ tableau de validation sont présentes dans la table. Si une table n’existe pas, toutes les \_ entrées de validation pour cette table sont ignorées.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952292"
---
# <a name="ice06"></a><span data-ttu-id="44df3-104">ICE06</span><span class="sxs-lookup"><span data-stu-id="44df3-104">ICE06</span></span>

<span data-ttu-id="44df3-105">ICE06 vérifie chaque table pour valider que toutes les colonnes répertoriées dans le [ \_ tableau de validation](-validation-table.md) sont présentes dans la table.</span><span class="sxs-lookup"><span data-stu-id="44df3-105">ICE06 checks every table to validate that all the columns listed in the [\_Validation table](-validation-table.md) are present in the table.</span></span> <span data-ttu-id="44df3-106">Si une table n’existe pas, toutes les \_ entrées de validation pour cette table sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="44df3-106">If a table does not exist, any \_Validation entries for that table are ignored.</span></span>

<span data-ttu-id="44df3-107">L’objectif de ICE06 est de détecter les instances dans lesquelles un auteur tente d’utiliser une nouvelle \_ table de validation qui reflète une modification de schéma avec une ancienne base de données qui n’a pas été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="44df3-107">The purpose of ICE06 is to detect instances in which an author tries to use a new \_Validation table that reflects a schema change with an old database that has not been updated.</span></span> <span data-ttu-id="44df3-108">ICE06 détecte également le cas inverse d’une ancienne \_ table de validation utilisée avec une base de données modifiée.</span><span class="sxs-lookup"><span data-stu-id="44df3-108">ICE06 also detects the reverse case of an old \_Validation table being used with an altered database.</span></span>

<span data-ttu-id="44df3-109">Notez que la validation interne effectuée par [ICE03](ice03.md) intercepte l’instance d’une colonne de table non définie dans la \_ table de validation qui est indiquée dans le catalogue de colonnes.</span><span class="sxs-lookup"><span data-stu-id="44df3-109">Note that the internal validation performed by [ICE03](ice03.md) catches the instance of a table column not defined in the \_Validation table being listed in the columns catalog.</span></span> <span data-ttu-id="44df3-110">L’utilisation de ICE03 et ICE06 garantit donc que chaque colonne de la base de données est testée.</span><span class="sxs-lookup"><span data-stu-id="44df3-110">The use of both ICE03 and ICE06 therefore ensures every column in the database is tested.</span></span>

## <a name="result"></a><span data-ttu-id="44df3-111">Résultats</span><span class="sxs-lookup"><span data-stu-id="44df3-111">Result</span></span>

<span data-ttu-id="44df3-112">ICE06 publie une erreur quand une colonne de table définie dans la table de \_ validation n’est pas listée dans la \_ Table Columns.</span><span class="sxs-lookup"><span data-stu-id="44df3-112">ICE06 posts an error when there is a table column defined in the \_Validation table that is not listed in the \_Columns table.</span></span>

## <a name="example"></a><span data-ttu-id="44df3-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="44df3-113">Example</span></span>

<span data-ttu-id="44df3-114">Dans l’exemple suivant, ICE06 publie le message</span><span class="sxs-lookup"><span data-stu-id="44df3-114">For the following example ICE06 posts the message</span></span>

<span data-ttu-id="44df3-115">Colonne : version de la table : la ModuleSignature n’est pas définie dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="44df3-115">Column: Version of Table: ModuleSignature is not defined in database.</span></span>

<span data-ttu-id="44df3-116">[ \_ Table de validation](-validation-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="44df3-116">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="44df3-117">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="44df3-117">Table</span></span>           | <span data-ttu-id="44df3-118">Colonne</span><span class="sxs-lookup"><span data-stu-id="44df3-118">Column</span></span>   |
|-----------------|----------|
| <span data-ttu-id="44df3-119">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="44df3-119">ModuleSignature</span></span> | <span data-ttu-id="44df3-120">ModuleID</span><span class="sxs-lookup"><span data-stu-id="44df3-120">ModuleID</span></span> |
| <span data-ttu-id="44df3-121">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="44df3-121">ModuleSignature</span></span> | <span data-ttu-id="44df3-122">Version</span><span class="sxs-lookup"><span data-stu-id="44df3-122">Version</span></span>  |



 

<span data-ttu-id="44df3-123">[ \_ Table Columns](-columns-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="44df3-123">[\_Columns Table](-columns-table.md) (partial)</span></span>



| <span data-ttu-id="44df3-124">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="44df3-124">Table</span></span>           | <span data-ttu-id="44df3-125">Number</span><span class="sxs-lookup"><span data-stu-id="44df3-125">Number</span></span> | <span data-ttu-id="44df3-126">Nom</span><span class="sxs-lookup"><span data-stu-id="44df3-126">Name</span></span>     |
|-----------------|--------|----------|
| <span data-ttu-id="44df3-127">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="44df3-127">ModuleSignature</span></span> | <span data-ttu-id="44df3-128">1</span><span class="sxs-lookup"><span data-stu-id="44df3-128">1</span></span>      | <span data-ttu-id="44df3-129">ModuleID</span><span class="sxs-lookup"><span data-stu-id="44df3-129">ModuleID</span></span> |



 

<span data-ttu-id="44df3-130">La colonne version de la table ModuleSignature n’est pas dans la base de données ou n’est pas indiquée dans la \_ Table Columns.</span><span class="sxs-lookup"><span data-stu-id="44df3-130">The Version column of the ModuleSignature table is not in the database or listed in the \_Columns table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44df3-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44df3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44df3-132">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="44df3-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



