---
description: ICE52 vérifie les propriétés privées dans la table AppSearch. Consultez à propos des propriétés.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867290"
---
# <a name="ice52"></a><span data-ttu-id="e908d-104">ICE52</span><span class="sxs-lookup"><span data-stu-id="e908d-104">ICE52</span></span>

<span data-ttu-id="e908d-105">ICE52 vérifie les propriétés privées dans la [table AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="e908d-105">ICE52 checks for private properties in the [AppSearch table](appsearch-table.md).</span></span> <span data-ttu-id="e908d-106">Consultez [à propos des propriétés](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e908d-106">See [About Properties](about-properties.md).</span></span>

<span data-ttu-id="e908d-107">Quand vous utilisez Windows 2000, toutes les propriétés définies dans la colonne propriété de la table AppSearch doivent être des propriétés publiques.</span><span class="sxs-lookup"><span data-stu-id="e908d-107">When using Windows 2000 all properties set in the Property column of the AppSearch table must be public properties.</span></span>

## <a name="result"></a><span data-ttu-id="e908d-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="e908d-108">Result</span></span>

<span data-ttu-id="e908d-109">ICE52 publie un avertissement s’il existe une propriété privée dans la table AppSearch.</span><span class="sxs-lookup"><span data-stu-id="e908d-109">ICE52 posts a warning if there is a private property in the AppSearch table.</span></span>

## <a name="example"></a><span data-ttu-id="e908d-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="e908d-110">Example</span></span>

<span data-ttu-id="e908d-111">ICE52 publie l’avertissement suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="e908d-111">ICE52 posts the following warning for the example shown.</span></span>

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[<span data-ttu-id="e908d-112">Table AppSearch</span><span class="sxs-lookup"><span data-stu-id="e908d-112">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="e908d-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="e908d-113">Property</span></span>  | <span data-ttu-id="e908d-114">Signature</span><span class="sxs-lookup"><span data-stu-id="e908d-114">Signature</span></span>  |
|-----------|------------|
| <span data-ttu-id="e908d-115">PROPERTY1</span><span class="sxs-lookup"><span data-stu-id="e908d-115">PROPERTY1</span></span> | <span data-ttu-id="e908d-116">Signature1</span><span class="sxs-lookup"><span data-stu-id="e908d-116">Signature1</span></span> |
| <span data-ttu-id="e908d-117">Property2</span><span class="sxs-lookup"><span data-stu-id="e908d-117">Property2</span></span> | <span data-ttu-id="e908d-118">Signature2</span><span class="sxs-lookup"><span data-stu-id="e908d-118">Signature2</span></span> |



 

<span data-ttu-id="e908d-119">Pour corriger cet avertissement, passez à la propriété publique personnalisée : PROPERTY2.</span><span class="sxs-lookup"><span data-stu-id="e908d-119">To fix this warning change to the custom public property: PROPERTY2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e908d-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e908d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e908d-121">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="e908d-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



