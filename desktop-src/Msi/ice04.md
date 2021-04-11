---
description: ICE04 vérifie que le numéro de séquence de chaque fichier de la table de fichiers est inférieur ou égal au numéro de séquence le plus élevé dans la colonne LastSequence de la table des médias.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952293"
---
# <a name="ice04"></a><span data-ttu-id="db31c-103">ICE04</span><span class="sxs-lookup"><span data-stu-id="db31c-103">ICE04</span></span>

<span data-ttu-id="db31c-104">ICE04 vérifie que le numéro de séquence de chaque fichier de la [table de fichiers](file-table.md) est inférieur ou égal au numéro de séquence le plus élevé dans la colonne LastSequence de la [table des médias](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="db31c-104">ICE04 validates that the sequence number of every file in the [File table](file-table.md) is less than or equal to the largest sequence number in the LastSequence column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="db31c-105">Chaque enregistrement de la table des médias représente un disque sur le support source contenant tous les fichiers dont le numéro de séquence est inférieur ou égal à la valeur de la colonne LastSequence et supérieur à la valeur LastSequence dans l’enregistrement du disque précédent.</span><span class="sxs-lookup"><span data-stu-id="db31c-105">Each record in the Media table represents a disk on the source media containing all the files with a sequence number less than or equal to the value in the LastSequence column and greater than the LastSequence value in the record of the preceding disk.</span></span>

## <a name="result"></a><span data-ttu-id="db31c-106">Résultats</span><span class="sxs-lookup"><span data-stu-id="db31c-106">Result</span></span>

<span data-ttu-id="db31c-107">ICE04 publie un message d’erreur s’il existe un fichier avec un numéro de séquence supérieur au plus grand numéro de LastSequence du support source.</span><span class="sxs-lookup"><span data-stu-id="db31c-107">ICE04 posts an error message if there is a file with a sequence number greater than the largest LastSequence number for the source media.</span></span>

## <a name="example"></a><span data-ttu-id="db31c-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="db31c-108">Example</span></span>

<span data-ttu-id="db31c-109">ICE04 signale l’erreur suivante pour l’exemple ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="db31c-109">ICE04 would report the following error for the example shown:</span></span>

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

<span data-ttu-id="db31c-110">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="db31c-110">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="db31c-111">Fichier</span><span class="sxs-lookup"><span data-stu-id="db31c-111">File</span></span>   | <span data-ttu-id="db31c-112">Séquence</span><span class="sxs-lookup"><span data-stu-id="db31c-112">Sequence</span></span> |
|--------|----------|
| <span data-ttu-id="db31c-113">Monfichier</span><span class="sxs-lookup"><span data-stu-id="db31c-113">MyFile</span></span> | <span data-ttu-id="db31c-114">210</span><span class="sxs-lookup"><span data-stu-id="db31c-114">210</span></span>      |



 

<span data-ttu-id="db31c-115">[Table des médias](media-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="db31c-115">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="db31c-116">DiskId</span><span class="sxs-lookup"><span data-stu-id="db31c-116">DiskId</span></span> | <span data-ttu-id="db31c-117">LastSequence</span><span class="sxs-lookup"><span data-stu-id="db31c-117">LastSequence</span></span> |
|--------|--------------|
| <span data-ttu-id="db31c-118">1</span><span class="sxs-lookup"><span data-stu-id="db31c-118">1</span></span>      | <span data-ttu-id="db31c-119">100</span><span class="sxs-lookup"><span data-stu-id="db31c-119">100</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="db31c-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db31c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db31c-121">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="db31c-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



