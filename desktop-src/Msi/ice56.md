---
description: ICE56 vérifie que la structure de répertoire du fichier. msi possède un répertoire racine unique, que la racine est la propriété TARGETDIR et que la valeur de la propriété SourceDir se trouve dans la colonne DefaultDir de la table Directory.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518817"
---
# <a name="ice56"></a><span data-ttu-id="46062-103">ICE56</span><span class="sxs-lookup"><span data-stu-id="46062-103">ICE56</span></span>

<span data-ttu-id="46062-104">ICE56 vérifie que la structure de répertoire du fichier. msi possède un répertoire racine unique, que la racine est la propriété [**targetDir**](targetdir.md) et que la valeur de la propriété [**SourceDir**](sourcedir.md) se trouve dans la colonne DefaultDir de la [table Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="46062-104">ICE56 validates that the directory structure of the .msi file has a single root directory, that the root is the [**TARGETDIR**](targetdir.md) property, and that the [**SourceDir**](sourcedir.md) property value is in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="46062-105">Si un fichier. msi a plusieurs racines ou spécifie une racine autre que [**targetDir**](targetdir.md), une [installation administrative](administrative-installation.md) ne crée pas d’image administrative correcte.</span><span class="sxs-lookup"><span data-stu-id="46062-105">If a .msi file has multiple roots or specifies a root other than [**TARGETDIR**](targetdir.md), an [administrative installation](administrative-installation.md) does not create a correct administrative image.</span></span>

<span data-ttu-id="46062-106">Notez que les répertoires vides ne sont pas vérifiés par ICE56.</span><span class="sxs-lookup"><span data-stu-id="46062-106">Note that empty directories are not checked by ICE56.</span></span> <span data-ttu-id="46062-107">La structure de répertoires est validée avec plusieurs répertoires racine si les répertoires supplémentaires sont vides.</span><span class="sxs-lookup"><span data-stu-id="46062-107">The directory structure passes validation with multiple root directories if the extra directories are empty.</span></span>

## <a name="result"></a><span data-ttu-id="46062-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="46062-108">Result</span></span>

<span data-ttu-id="46062-109">ICE56 publie une erreur si le fichier. msi n’a pas de racine unique, [**targetDir**](targetdir.md)ou si [**SourceDir**](sourcedir.md) n’est pas spécifié dans la colonne DefaultDir de la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="46062-109">ICE56 posts an error if the .msi does not have a single root, [**TARGETDIR**](targetdir.md), or if [**SourceDir**](sourcedir.md) is not specified in the DefaultDir column of the [Directory table](directory-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="46062-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="46062-110">Example</span></span>

<span data-ttu-id="46062-111">ICE56 signale les erreurs suivantes pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="46062-111">ICE56 reports the following errors for the example shown.</span></span>

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[<span data-ttu-id="46062-112">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="46062-112">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="46062-113">Répertoire</span><span class="sxs-lookup"><span data-stu-id="46062-113">Directory</span></span> | <span data-ttu-id="46062-114">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="46062-114">Directory\_Parent</span></span> | <span data-ttu-id="46062-115">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="46062-115">DefaultDir</span></span> |
|-----------|-------------------|------------|
| <span data-ttu-id="46062-116">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="46062-116">TARGETDIR</span></span> |                   | <span data-ttu-id="46062-117">Temp</span><span class="sxs-lookup"><span data-stu-id="46062-117">Temp</span></span>       |
| <span data-ttu-id="46062-118">ROOT2</span><span class="sxs-lookup"><span data-stu-id="46062-118">Root2</span></span>     | <span data-ttu-id="46062-119">ROOT2</span><span class="sxs-lookup"><span data-stu-id="46062-119">Root2</span></span>             | <span data-ttu-id="46062-120">SourceDir</span><span class="sxs-lookup"><span data-stu-id="46062-120">SourceDir</span></span>  |



 

<span data-ttu-id="46062-121">Pour corriger la première erreur, la racine [**targetDir**](targetdir.md) doit avoir une valeur DefaultDir de [**SourceDir**](sourcedir.md).</span><span class="sxs-lookup"><span data-stu-id="46062-121">To fix the first error, the [**TARGETDIR**](targetdir.md) root should have a DefaultDir value of [**SourceDir**](sourcedir.md).</span></span> <span data-ttu-id="46062-122">SOURCEDIR est également accepté.</span><span class="sxs-lookup"><span data-stu-id="46062-122">SOURCEDIR is also accepted.</span></span> <span data-ttu-id="46062-123">Il peut être possible de faire de **targetDir** le parent de la deuxième racine et d’utiliser la valeur'. 'dans la colonne DefaultDir.</span><span class="sxs-lookup"><span data-stu-id="46062-123">It may be possible to make **TARGETDIR** the parent of the second root, and use the '.' value in the DefaultDir column.</span></span> <span data-ttu-id="46062-124">Pour plus d’informations, consultez la [table Directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="46062-124">See the [Directory table](directory-table.md) for more information.</span></span>

<span data-ttu-id="46062-125">Pour corriger la deuxième erreur, la structure de répertoire ne doit avoir qu’une seule racine appelée [**targetDir**](targetdir.md).</span><span class="sxs-lookup"><span data-stu-id="46062-125">To fix the second error, the Directory structure should have only one root called [**TARGETDIR**](targetdir.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46062-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="46062-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46062-127">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="46062-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



