---
description: La table ODBCSourceAttribute contient des informations sur les attributs des sources de données.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Table ODBCSourceAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52dd9636ac19eae0fb3a9e41d1a1c8389753e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525773"
---
# <a name="odbcsourceattribute-table"></a><span data-ttu-id="ef624-103">Table ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="ef624-103">ODBCSourceAttribute Table</span></span>

<span data-ttu-id="ef624-104">La table ODBCSourceAttribute contient des informations sur les attributs des sources de données.</span><span class="sxs-lookup"><span data-stu-id="ef624-104">The ODBCSourceAttribute table contains information about the attributes of data sources.</span></span>

<span data-ttu-id="ef624-105">La table ODBCSourceAttribute contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef624-105">The ODBCSourceAttribute table has the following columns.</span></span>



| <span data-ttu-id="ef624-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="ef624-106">Column</span></span>       | <span data-ttu-id="ef624-107">Type</span><span class="sxs-lookup"><span data-stu-id="ef624-107">Type</span></span>                         | <span data-ttu-id="ef624-108">Clé</span><span class="sxs-lookup"><span data-stu-id="ef624-108">Key</span></span> | <span data-ttu-id="ef624-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="ef624-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="ef624-110">DataSource\_</span><span class="sxs-lookup"><span data-stu-id="ef624-110">DataSource\_</span></span> | [<span data-ttu-id="ef624-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="ef624-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ef624-112">O</span><span class="sxs-lookup"><span data-stu-id="ef624-112">Y</span></span>   | <span data-ttu-id="ef624-113">N</span><span class="sxs-lookup"><span data-stu-id="ef624-113">N</span></span>        |
| <span data-ttu-id="ef624-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="ef624-114">Attribute</span></span>    | [<span data-ttu-id="ef624-115">Text</span><span class="sxs-lookup"><span data-stu-id="ef624-115">Text</span></span>](text.md)             | <span data-ttu-id="ef624-116">O</span><span class="sxs-lookup"><span data-stu-id="ef624-116">Y</span></span>   | <span data-ttu-id="ef624-117">N</span><span class="sxs-lookup"><span data-stu-id="ef624-117">N</span></span>        |
| <span data-ttu-id="ef624-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef624-118">Value</span></span>        | [<span data-ttu-id="ef624-119">Correct</span><span class="sxs-lookup"><span data-stu-id="ef624-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="ef624-120">N</span><span class="sxs-lookup"><span data-stu-id="ef624-120">N</span></span>   | <span data-ttu-id="ef624-121">O</span><span class="sxs-lookup"><span data-stu-id="ef624-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ef624-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="ef624-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ef624-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>Mustek\_</span><span class="sxs-lookup"><span data-stu-id="ef624-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span></span>
</dt> <dd>

<span data-ttu-id="ef624-124">Nom de jeton interne de la source de données.</span><span class="sxs-lookup"><span data-stu-id="ef624-124">Internal token name for data source.</span></span> <span data-ttu-id="ef624-125">Clé primaire pour la table.</span><span class="sxs-lookup"><span data-stu-id="ef624-125">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="ef624-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut</span><span class="sxs-lookup"><span data-stu-id="ef624-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="ef624-127">Nom de l’attribut de source de données.</span><span class="sxs-lookup"><span data-stu-id="ef624-127">Name of data source attribute.</span></span> <span data-ttu-id="ef624-128">Clé primaire pour la table.</span><span class="sxs-lookup"><span data-stu-id="ef624-128">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="ef624-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="ef624-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="ef624-130">Valeur de chaîne localisable pour l’attribut.</span><span class="sxs-lookup"><span data-stu-id="ef624-130">The localizable string value for the attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef624-131">Notes</span><span class="sxs-lookup"><span data-stu-id="ef624-131">Remarks</span></span>

<span data-ttu-id="ef624-132">Les actions [InstallODBC](installodbc-action.md) et [RemoveODBC](removeodbc-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="ef624-132">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="ef624-133">Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef624-133">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="ef624-134">Validation</span><span class="sxs-lookup"><span data-stu-id="ef624-134">Validation</span></span>

<dl>

[<span data-ttu-id="ef624-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="ef624-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ef624-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="ef624-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ef624-137">ICE32</span><span class="sxs-lookup"><span data-stu-id="ef624-137">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ef624-138">ICE46</span><span class="sxs-lookup"><span data-stu-id="ef624-138">ICE46</span></span>](ice46.md)  
</dl>

 

 



