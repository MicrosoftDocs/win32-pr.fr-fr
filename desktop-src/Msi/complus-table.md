---
description: La table ComPlus contient les informations nécessaires pour installer les applications COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Table ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526286"
---
# <a name="complus-table"></a><span data-ttu-id="ae111-103">Table ComPlus</span><span class="sxs-lookup"><span data-stu-id="ae111-103">Complus Table</span></span>

<span data-ttu-id="ae111-104">La table ComPlus contient les informations nécessaires pour installer les applications COM+.</span><span class="sxs-lookup"><span data-stu-id="ae111-104">The Complus table contains information needed to install COM+ applications.</span></span>

<span data-ttu-id="ae111-105">La table ComPlus contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ae111-105">The Complus table has the following columns.</span></span>



| <span data-ttu-id="ae111-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="ae111-106">Column</span></span>      | <span data-ttu-id="ae111-107">Type</span><span class="sxs-lookup"><span data-stu-id="ae111-107">Type</span></span>                         | <span data-ttu-id="ae111-108">Clé</span><span class="sxs-lookup"><span data-stu-id="ae111-108">Key</span></span> | <span data-ttu-id="ae111-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="ae111-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="ae111-110">-\_</span><span class="sxs-lookup"><span data-stu-id="ae111-110">Component\_</span></span> | [<span data-ttu-id="ae111-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="ae111-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ae111-112">O</span><span class="sxs-lookup"><span data-stu-id="ae111-112">Y</span></span>   | <span data-ttu-id="ae111-113">N</span><span class="sxs-lookup"><span data-stu-id="ae111-113">N</span></span>        |
| <span data-ttu-id="ae111-114">ExpType</span><span class="sxs-lookup"><span data-stu-id="ae111-114">ExpType</span></span>     | [<span data-ttu-id="ae111-115">Integer</span><span class="sxs-lookup"><span data-stu-id="ae111-115">Integer</span></span>](integer.md)       | <span data-ttu-id="ae111-116">N</span><span class="sxs-lookup"><span data-stu-id="ae111-116">N</span></span>   | <span data-ttu-id="ae111-117">O</span><span class="sxs-lookup"><span data-stu-id="ae111-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ae111-118">Colonnes</span><span class="sxs-lookup"><span data-stu-id="ae111-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ae111-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="ae111-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="ae111-120">Clé externe dans la première colonne de la [table de composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae111-120">An external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="ae111-121">Il s’agit du composant qui contient l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="ae111-121">This is the component that contains the COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="ae111-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span><span class="sxs-lookup"><span data-stu-id="ae111-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span></span>
</dt> <dd>

<span data-ttu-id="ae111-123">Exportez les indicateurs utilisés lors de la génération du fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="ae111-123">Export flags used during the generation of the .msi file.</span></span> <span data-ttu-id="ae111-124">Pour plus d’informations, consultez la documentation COM+ dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ae111-124">For more information see the COM+ documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae111-125">Notes</span><span class="sxs-lookup"><span data-stu-id="ae111-125">Remarks</span></span>

<span data-ttu-id="ae111-126">Consultez l’action [RegisterComPlus](registercomplus-action.md) et l' [action UnregisterComPlus](unregistercomplus-action.md).</span><span class="sxs-lookup"><span data-stu-id="ae111-126">See the [RegisterComPlus action](registercomplus-action.md) and [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

<span data-ttu-id="ae111-127">Consultez [installation d’une application com+ avec l’Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="ae111-127">See [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span></span>

## <a name="validation"></a><span data-ttu-id="ae111-128">Validation</span><span class="sxs-lookup"><span data-stu-id="ae111-128">Validation</span></span>

<dl>

[<span data-ttu-id="ae111-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="ae111-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ae111-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="ae111-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ae111-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="ae111-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ae111-132">ICE66</span><span class="sxs-lookup"><span data-stu-id="ae111-132">ICE66</span></span>](ice66.md)  
</dl>

 

 



