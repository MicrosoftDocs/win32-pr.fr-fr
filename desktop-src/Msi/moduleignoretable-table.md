---
description: Si une table du module de fusion est listée dans le tableau ModuleIgnoreTable, elle n’est pas fusionnée dans le fichier. msi.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Table ModuleIgnoreTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210252"
---
# <a name="moduleignoretable-table"></a><span data-ttu-id="d3a28-103">Table ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="d3a28-103">ModuleIgnoreTable Table</span></span>

<span data-ttu-id="d3a28-104">Si une table du module de fusion est listée dans le tableau ModuleIgnoreTable, elle n’est pas fusionnée dans le fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="d3a28-104">If a table in the merge module is listed in the ModuleIgnoreTable table, it is not merged into the .msi file.</span></span> <span data-ttu-id="d3a28-105">Si la table existe déjà dans le fichier. msi, elle n’est pas modifiée par la fusion.</span><span class="sxs-lookup"><span data-stu-id="d3a28-105">If the table already exists in the .msi file, it is not modified by the merge.</span></span> <span data-ttu-id="d3a28-106">Les tables dans ModuleIgnoreTable peuvent donc contenir des données qui ne sont pas nécessaires après la fusion.</span><span class="sxs-lookup"><span data-stu-id="d3a28-106">The tables in the ModuleIgnoreTable can therefore contain data that is unneeded after the merge.</span></span>

<span data-ttu-id="d3a28-107">La table ModuleIgnoreTable contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d3a28-107">The ModuleIgnoreTable table has the following columns.</span></span>



| <span data-ttu-id="d3a28-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="d3a28-108">Column</span></span> | <span data-ttu-id="d3a28-109">Type</span><span class="sxs-lookup"><span data-stu-id="d3a28-109">Type</span></span>                         | <span data-ttu-id="d3a28-110">Clé</span><span class="sxs-lookup"><span data-stu-id="d3a28-110">Key</span></span> | <span data-ttu-id="d3a28-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="d3a28-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="d3a28-112">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="d3a28-112">Table</span></span>  | [<span data-ttu-id="d3a28-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="d3a28-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="d3a28-114">O</span><span class="sxs-lookup"><span data-stu-id="d3a28-114">Y</span></span>   | <span data-ttu-id="d3a28-115">Non</span><span class="sxs-lookup"><span data-stu-id="d3a28-115">No</span></span>       |



 

## <a name="columns"></a><span data-ttu-id="d3a28-116">Colonnes</span><span class="sxs-lookup"><span data-stu-id="d3a28-116">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d3a28-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau</span><span class="sxs-lookup"><span data-stu-id="d3a28-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="d3a28-118">Nom de la table dans le module de fusion qui ne doit pas être fusionnée dans le fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="d3a28-118">Name of the table in the merge module that is not to be merged into the .msi file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3a28-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d3a28-119">Remarks</span></span>

<span data-ttu-id="d3a28-120">Pour réduire la taille du fichier. msm, il est recommandé aux développeurs de supprimer les tables inutilisées des modules destinés à la redistribution plutôt que de répertorier ces tables dans la table ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="d3a28-120">To minimize the size of the .msm file, it is recommended that developers remove unused tables from modules intended for redistribution rather than listing these tables in the ModuleIgnoreTable table.</span></span>

 

 



