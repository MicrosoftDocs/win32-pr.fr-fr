---
description: ICE15 valide le fait que le type de contenu et les références d’extension dans les tables MIME et d’extension soient réciproques. La table MIME doit faire référence à un type de contenu dans une extension que la table d’extension fait référence au même type de contenu.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034791"
---
# <a name="ice15"></a><span data-ttu-id="441d5-104">ICE15</span><span class="sxs-lookup"><span data-stu-id="441d5-104">ICE15</span></span>

<span data-ttu-id="441d5-105">ICE15 valide le fait que le type de contenu et les références d’extension dans les tables [MIME](mime-table.md) et d' [extension](extension-table.md) soient réciproques.</span><span class="sxs-lookup"><span data-stu-id="441d5-105">ICE15 validates that content type and extension references in the [MIME](mime-table.md) and [Extension](extension-table.md) tables are reciprocal.</span></span> <span data-ttu-id="441d5-106">La table MIME doit faire référence à un type de contenu dans une extension que la table d’extension fait référence au même type de contenu.</span><span class="sxs-lookup"><span data-stu-id="441d5-106">The MIME table must reference a content type to an extension that the Extension table references back to the same content type.</span></span>

<span data-ttu-id="441d5-107">Plusieurs extensions peuvent référencer le même type MIME, à condition que le type MIME fasse référence à l’une des extensions.</span><span class="sxs-lookup"><span data-stu-id="441d5-107">Multiple extensions can reference the same MIME type, as long as the MIME type references back to one of the extensions.</span></span> <span data-ttu-id="441d5-108">Plusieurs types MIME peuvent faire référence à la même extension, à condition que l’extension fasse référence à l’un des types MIME.</span><span class="sxs-lookup"><span data-stu-id="441d5-108">Multiple MIME types can reference the same extension, as long as the extension references back to one of the MIME types.</span></span>

<span data-ttu-id="441d5-109">Notez que chaque fois qu’un MIME fait référence à une extension, cette extension ne peut pas avoir la \_ colonne MIME dans la table d’extension définie sur null.</span><span class="sxs-lookup"><span data-stu-id="441d5-109">Note that whenever a MIME references an extension, that extension cannot have the MIME\_ column in the Extension table set to Null.</span></span>

## <a name="result"></a><span data-ttu-id="441d5-110">Résultats</span><span class="sxs-lookup"><span data-stu-id="441d5-110">Result</span></span>

<span data-ttu-id="441d5-111">ICE15 publie une erreur si le type de contenu et les références d’extension ne sont pas réciproques.</span><span class="sxs-lookup"><span data-stu-id="441d5-111">ICE15 posts an error if the content type and extension references are not reciprocal.</span></span>

## <a name="example"></a><span data-ttu-id="441d5-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="441d5-112">Example</span></span>

<span data-ttu-id="441d5-113">ICE15 publie deux messages d’erreur pour l’exemple ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="441d5-113">ICE15 posts two error messages for the example shown:</span></span>

-   <span data-ttu-id="441d5-114">Le type de contenu test/aile x dans la table MIME fait référence à l’extension TST, mais l’extension TST dans la table d’extension fait référence aux rabats/x-rabats.</span><span class="sxs-lookup"><span data-stu-id="441d5-114">The content type test/x-flaps in the MIME table references the extension tst, but the extension tst in the Extension table references flaps/x-flaps.</span></span> <span data-ttu-id="441d5-115">Ce n’est pas réciproque.</span><span class="sxs-lookup"><span data-stu-id="441d5-115">This is not reciprocal.</span></span>
-   <span data-ttu-id="441d5-116">Les rabats de type de contenu/rabats font référence à l’extension FLP, mais cette extension a une entrée null dans la \_ colonne MIME de la table d’extension.</span><span class="sxs-lookup"><span data-stu-id="441d5-116">The content type flaps/x-flaps references the extension flp, but that extension has a Null entry in the MIME\_ column of the Extension table.</span></span>

<span data-ttu-id="441d5-117">[Table MIME](mime-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="441d5-117">[MIME Table](mime-table.md) (partial)</span></span>



| <span data-ttu-id="441d5-118">ContentType</span><span class="sxs-lookup"><span data-stu-id="441d5-118">ContentType</span></span>   | <span data-ttu-id="441d5-119">Extension\_</span><span class="sxs-lookup"><span data-stu-id="441d5-119">Extension\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="441d5-120">test/x-test</span><span class="sxs-lookup"><span data-stu-id="441d5-120">test/x-test</span></span>   | <span data-ttu-id="441d5-121">TST</span><span class="sxs-lookup"><span data-stu-id="441d5-121">tst</span></span>         |
| <span data-ttu-id="441d5-122">rabats/rabats</span><span class="sxs-lookup"><span data-stu-id="441d5-122">flaps/x-flaps</span></span> | <span data-ttu-id="441d5-123">FLP</span><span class="sxs-lookup"><span data-stu-id="441d5-123">flp</span></span>         |



 

<span data-ttu-id="441d5-124">[Table d’extension](extension-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="441d5-124">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="441d5-125">Extension</span><span class="sxs-lookup"><span data-stu-id="441d5-125">Extension</span></span> | <span data-ttu-id="441d5-126">MIME\_</span><span class="sxs-lookup"><span data-stu-id="441d5-126">MIME\_</span></span>        |
|-----------|---------------|
| <span data-ttu-id="441d5-127">TST</span><span class="sxs-lookup"><span data-stu-id="441d5-127">tst</span></span>       | <span data-ttu-id="441d5-128">rabats/rabats</span><span class="sxs-lookup"><span data-stu-id="441d5-128">flaps/x-flaps</span></span> |
| <span data-ttu-id="441d5-129">FLP</span><span class="sxs-lookup"><span data-stu-id="441d5-129">flp</span></span>       | <span data-ttu-id="441d5-130">Null</span><span class="sxs-lookup"><span data-stu-id="441d5-130">Null</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="441d5-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="441d5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="441d5-132">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="441d5-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



