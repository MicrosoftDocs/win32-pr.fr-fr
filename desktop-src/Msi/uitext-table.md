---
description: La table UIText contient les versions localisées de certaines chaînes utilisées dans l’interface utilisateur. Ces chaînes ne font pas partie d’une autre table. La table UIText est destinée aux chaînes qui n’ont pas d’emplacement logique dans une autre table.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: Table UIText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111983"
---
# <a name="uitext-table"></a><span data-ttu-id="1a326-105">Table UIText</span><span class="sxs-lookup"><span data-stu-id="1a326-105">UIText Table</span></span>

<span data-ttu-id="1a326-106">La table UIText contient les versions localisées de certaines chaînes utilisées dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a326-106">The UIText table contains the localized versions of some of the strings used in the user interface.</span></span> <span data-ttu-id="1a326-107">Ces chaînes ne font pas partie d’une autre table.</span><span class="sxs-lookup"><span data-stu-id="1a326-107">These strings are not part of any other table.</span></span> <span data-ttu-id="1a326-108">La table UIText est destinée aux chaînes qui n’ont pas d’emplacement logique dans une autre table.</span><span class="sxs-lookup"><span data-stu-id="1a326-108">The UIText table is for strings that have no logical place in any other table.</span></span>

<span data-ttu-id="1a326-109">La table UIText contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1a326-109">The UIText table has the following columns.</span></span>



| <span data-ttu-id="1a326-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="1a326-110">Column</span></span> | <span data-ttu-id="1a326-111">Type</span><span class="sxs-lookup"><span data-stu-id="1a326-111">Type</span></span>                         | <span data-ttu-id="1a326-112">Clé</span><span class="sxs-lookup"><span data-stu-id="1a326-112">Key</span></span> | <span data-ttu-id="1a326-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="1a326-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="1a326-114">Clé</span><span class="sxs-lookup"><span data-stu-id="1a326-114">Key</span></span>    | [<span data-ttu-id="1a326-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="1a326-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="1a326-116">O</span><span class="sxs-lookup"><span data-stu-id="1a326-116">Y</span></span>   | <span data-ttu-id="1a326-117">N</span><span class="sxs-lookup"><span data-stu-id="1a326-117">N</span></span>        |
| <span data-ttu-id="1a326-118">Texte</span><span class="sxs-lookup"><span data-stu-id="1a326-118">Text</span></span>   | [<span data-ttu-id="1a326-119">Text</span><span class="sxs-lookup"><span data-stu-id="1a326-119">Text</span></span>](text.md)             | <span data-ttu-id="1a326-120">N</span><span class="sxs-lookup"><span data-stu-id="1a326-120">N</span></span>   | <span data-ttu-id="1a326-121">O</span><span class="sxs-lookup"><span data-stu-id="1a326-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1a326-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="1a326-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1a326-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel</span><span class="sxs-lookup"><span data-stu-id="1a326-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="1a326-124">Clé unique qui identifie la chaîne particulière.</span><span class="sxs-lookup"><span data-stu-id="1a326-124">A unique key that identifies the particular string.</span></span>

</dd> <dt>

<span data-ttu-id="1a326-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière</span><span class="sxs-lookup"><span data-stu-id="1a326-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="1a326-126">Version localisée du type de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="1a326-126">The localized version of the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a326-127">Notes</span><span class="sxs-lookup"><span data-stu-id="1a326-127">Remarks</span></span>

<span data-ttu-id="1a326-128">Certains contrôles utilisent la table UIText comme source de chaînes.</span><span class="sxs-lookup"><span data-stu-id="1a326-128">Some controls use the UIText table as a source of strings.</span></span> <span data-ttu-id="1a326-129">Pour plus d’informations sur les chaînes requises dans ce tableau pour chaque contrôle particulier, consultez les contrôles individuels dans la référence de l' [interface utilisateur](user-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1a326-129">For information about which strings are required in this table for each particular control, see the individual controls in the [User Interface Reference](user-interface-reference.md).</span></span>

## <a name="validation"></a><span data-ttu-id="1a326-130">Validation</span><span class="sxs-lookup"><span data-stu-id="1a326-130">Validation</span></span>

<dl>

[<span data-ttu-id="1a326-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="1a326-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1a326-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="1a326-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



