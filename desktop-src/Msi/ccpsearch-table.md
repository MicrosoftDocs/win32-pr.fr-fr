---
description: La table CCPSearch contient la liste des signatures de fichiers utilisées pour le programme de vérification de la compatibilité (CCP). Au moins l’un de ces fichiers doit être présent sur l’ordinateur d’un utilisateur pour que l’utilisateur soit compatible avec le programme.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Table CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529797"
---
# <a name="ccpsearch-table"></a><span data-ttu-id="e5f71-104">Table CCPSearch</span><span class="sxs-lookup"><span data-stu-id="e5f71-104">CCPSearch Table</span></span>

<span data-ttu-id="e5f71-105">La table CCPSearch contient la liste des signatures de fichiers utilisées pour le programme de vérification de la compatibilité (CCP).</span><span class="sxs-lookup"><span data-stu-id="e5f71-105">The CCPSearch table contains the list of file signatures used for the Compliance Checking Program (CCP).</span></span> <span data-ttu-id="e5f71-106">Au moins l’un de ces fichiers doit être présent sur l’ordinateur d’un utilisateur pour que l’utilisateur soit compatible avec le programme.</span><span class="sxs-lookup"><span data-stu-id="e5f71-106">At least one of these files needs to be present on a user's computer for the user to be in compliance with the program.</span></span>

<span data-ttu-id="e5f71-107">La table CCPSearch contient la colonne suivante.</span><span class="sxs-lookup"><span data-stu-id="e5f71-107">The CCPSearch table has the following column.</span></span>



| <span data-ttu-id="e5f71-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="e5f71-108">Column</span></span>      | <span data-ttu-id="e5f71-109">Type</span><span class="sxs-lookup"><span data-stu-id="e5f71-109">Type</span></span>                         | <span data-ttu-id="e5f71-110">Clé</span><span class="sxs-lookup"><span data-stu-id="e5f71-110">Key</span></span> | <span data-ttu-id="e5f71-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="e5f71-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="e5f71-112">Signature\_</span><span class="sxs-lookup"><span data-stu-id="e5f71-112">Signature\_</span></span> | [<span data-ttu-id="e5f71-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="e5f71-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="e5f71-114">O</span><span class="sxs-lookup"><span data-stu-id="e5f71-114">Y</span></span>   | <span data-ttu-id="e5f71-115">N</span><span class="sxs-lookup"><span data-stu-id="e5f71-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="e5f71-116">Colonne</span><span class="sxs-lookup"><span data-stu-id="e5f71-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="e5f71-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="e5f71-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="e5f71-118">La signature \_ représente une signature de fichier unique et est également la clé externe dans les tables [signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)et [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e5f71-118">The Signature\_ represents a unique file signature and is also the external key into the [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5f71-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e5f71-119">Remarks</span></span>

<span data-ttu-id="e5f71-120">Cette table est référencée lorsque l' [action CCPSearch](ccpsearch-action.md) ou l' [action RMCCPSearch](rmccpsearch-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="e5f71-120">This table is referred to when the [CCPSearch action](ccpsearch-action.md) or the [RMCCPSearch action](rmccpsearch-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="e5f71-121">Validation</span><span class="sxs-lookup"><span data-stu-id="e5f71-121">Validation</span></span>

<dl>

[<span data-ttu-id="e5f71-122">ICE03</span><span class="sxs-lookup"><span data-stu-id="e5f71-122">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e5f71-123">ICE06</span><span class="sxs-lookup"><span data-stu-id="e5f71-123">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e5f71-124">ICE32</span><span class="sxs-lookup"><span data-stu-id="e5f71-124">ICE32</span></span>](ice32.md)  
</dl>

 

 



