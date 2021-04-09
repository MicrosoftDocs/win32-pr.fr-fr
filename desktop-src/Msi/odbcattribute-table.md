---
description: La table ODBCAttribute contient des informations sur les attributs des pilotes et des traducteurs de Open Database Connectivity (ODBC).
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Table ODBCAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114170"
---
# <a name="odbcattribute-table"></a><span data-ttu-id="5cfb1-103">Table ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="5cfb1-103">ODBCAttribute Table</span></span>

<span data-ttu-id="5cfb1-104">La table ODBCAttribute contient des informations sur les attributs des pilotes et des traducteurs de Open Database Connectivity (ODBC).</span><span class="sxs-lookup"><span data-stu-id="5cfb1-104">The ODBCAttribute table contains information about the attributes of Open Database Connectivity (ODBC) drivers and translators.</span></span>

<span data-ttu-id="5cfb1-105">La table ODBCAttribute contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="5cfb1-105">The ODBCAttribute table has the following columns.</span></span>



| <span data-ttu-id="5cfb1-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="5cfb1-106">Column</span></span>    | <span data-ttu-id="5cfb1-107">Type</span><span class="sxs-lookup"><span data-stu-id="5cfb1-107">Type</span></span>                         | <span data-ttu-id="5cfb1-108">Clé</span><span class="sxs-lookup"><span data-stu-id="5cfb1-108">Key</span></span> | <span data-ttu-id="5cfb1-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="5cfb1-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="5cfb1-110">Pilote\_</span><span class="sxs-lookup"><span data-stu-id="5cfb1-110">Driver\_</span></span>  | [<span data-ttu-id="5cfb1-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="5cfb1-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="5cfb1-112">O</span><span class="sxs-lookup"><span data-stu-id="5cfb1-112">Y</span></span>   | <span data-ttu-id="5cfb1-113">N</span><span class="sxs-lookup"><span data-stu-id="5cfb1-113">N</span></span>        |
| <span data-ttu-id="5cfb1-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="5cfb1-114">Attribute</span></span> | [<span data-ttu-id="5cfb1-115">Text</span><span class="sxs-lookup"><span data-stu-id="5cfb1-115">Text</span></span>](text.md)             | <span data-ttu-id="5cfb1-116">O</span><span class="sxs-lookup"><span data-stu-id="5cfb1-116">Y</span></span>   | <span data-ttu-id="5cfb1-117">N</span><span class="sxs-lookup"><span data-stu-id="5cfb1-117">N</span></span>        |
| <span data-ttu-id="5cfb1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cfb1-118">Value</span></span>     | [<span data-ttu-id="5cfb1-119">Correct</span><span class="sxs-lookup"><span data-stu-id="5cfb1-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="5cfb1-120">N</span><span class="sxs-lookup"><span data-stu-id="5cfb1-120">N</span></span>   | <span data-ttu-id="5cfb1-121">O</span><span class="sxs-lookup"><span data-stu-id="5cfb1-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5cfb1-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="5cfb1-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5cfb1-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Pilote\_</span><span class="sxs-lookup"><span data-stu-id="5cfb1-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Driver\_</span></span>
</dt> <dd>

<span data-ttu-id="5cfb1-124">Nom de jeton interne pour un pilote.</span><span class="sxs-lookup"><span data-stu-id="5cfb1-124">Internal token name for a driver.</span></span> <span data-ttu-id="5cfb1-125">Clé primaire pour la table.</span><span class="sxs-lookup"><span data-stu-id="5cfb1-125">A primary key for the table.</span></span> <span data-ttu-id="5cfb1-126">Clé étrangère dans la [table ODBCDriver](odbcdriver-table.md).</span><span class="sxs-lookup"><span data-stu-id="5cfb1-126">A foreign key into the [ODBCDriver table](odbcdriver-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cfb1-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut</span><span class="sxs-lookup"><span data-stu-id="5cfb1-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="5cfb1-128">Nom de l’attribut de pilote.</span><span class="sxs-lookup"><span data-stu-id="5cfb1-128">Name of the driver attribute.</span></span> <span data-ttu-id="5cfb1-129">Clé primaire pour la table.</span><span class="sxs-lookup"><span data-stu-id="5cfb1-129">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="5cfb1-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="5cfb1-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="5cfb1-131">Valeur de chaîne localisable pour l’attribut.</span><span class="sxs-lookup"><span data-stu-id="5cfb1-131">Localizable string value for attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cfb1-132">Notes</span><span class="sxs-lookup"><span data-stu-id="5cfb1-132">Remarks</span></span>

<span data-ttu-id="5cfb1-133">Les actions [InstallODBC](installodbc-action.md) et [RemoveODBC](removeodbc-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="5cfb1-133">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="5cfb1-134">Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="5cfb1-134">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="5cfb1-135">Validation</span><span class="sxs-lookup"><span data-stu-id="5cfb1-135">Validation</span></span>

<dl>

[<span data-ttu-id="5cfb1-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="5cfb1-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5cfb1-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="5cfb1-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="5cfb1-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="5cfb1-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="5cfb1-139">ICE46</span><span class="sxs-lookup"><span data-stu-id="5cfb1-139">ICE46</span></span>](ice46.md)  
</dl>

 

 



