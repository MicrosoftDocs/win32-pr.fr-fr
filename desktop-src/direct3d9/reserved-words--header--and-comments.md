---
description: Le tableau ci-dessous montre les mots qui sont réservés et qui ne doivent pas être utilisés.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Mots réservés, en-tête et commentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343654"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="0f7c4-103">Mots réservés, en-tête et commentaires</span><span class="sxs-lookup"><span data-stu-id="0f7c4-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="0f7c4-104">Le tableau ci-dessous montre les mots qui sont réservés et qui ne doivent pas être utilisés.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-104">The table below shows which words are reserved and must not be used.</span></span>

| <span data-ttu-id="0f7c4-105">Mots réservés</span><span class="sxs-lookup"><span data-stu-id="0f7c4-105">Reserved Words</span></span> | <span data-ttu-id="0f7c4-106">Mots réservés</span><span class="sxs-lookup"><span data-stu-id="0f7c4-106">Reserved Words</span></span> | <span data-ttu-id="0f7c4-107">Mots réservés</span><span class="sxs-lookup"><span data-stu-id="0f7c4-107">Reserved Words</span></span>|
|------------------|----------|-----------|
| <span data-ttu-id="0f7c4-108">ARRAY</span><span class="sxs-lookup"><span data-stu-id="0f7c4-108">ARRAY</span></span>            | <span data-ttu-id="0f7c4-109">DWORD</span><span class="sxs-lookup"><span data-stu-id="0f7c4-109">DWORD</span></span>    | <span data-ttu-id="0f7c4-110">UCHAR</span><span class="sxs-lookup"><span data-stu-id="0f7c4-110">UCHAR</span></span>     |
| <span data-ttu-id="0f7c4-111">BINARY</span><span class="sxs-lookup"><span data-stu-id="0f7c4-111">BINARY</span></span>           | <span data-ttu-id="0f7c4-112">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0f7c4-112">FLOAT</span></span>    | <span data-ttu-id="0f7c4-113">ULONGLONG</span><span class="sxs-lookup"><span data-stu-id="0f7c4-113">ULONGLONG</span></span> |
| <span data-ttu-id="0f7c4-114">\_ressource binaire</span><span class="sxs-lookup"><span data-stu-id="0f7c4-114">BINARY\_RESOURCE</span></span> | <span data-ttu-id="0f7c4-115">SDWORD</span><span class="sxs-lookup"><span data-stu-id="0f7c4-115">SDWORD</span></span>   | <span data-ttu-id="0f7c4-116">UNICODE</span><span class="sxs-lookup"><span data-stu-id="0f7c4-116">UNICODE</span></span>   |
| <span data-ttu-id="0f7c4-117">CHAR</span><span class="sxs-lookup"><span data-stu-id="0f7c4-117">CHAR</span></span>             | <span data-ttu-id="0f7c4-118">STRING</span><span class="sxs-lookup"><span data-stu-id="0f7c4-118">STRING</span></span>   | <span data-ttu-id="0f7c4-119">WORD</span><span class="sxs-lookup"><span data-stu-id="0f7c4-119">WORD</span></span>      |
| <span data-ttu-id="0f7c4-120">CSTRING</span><span class="sxs-lookup"><span data-stu-id="0f7c4-120">CSTRING</span></span>          | <span data-ttu-id="0f7c4-121">SWORD</span><span class="sxs-lookup"><span data-stu-id="0f7c4-121">SWORD</span></span>    |           |
| <span data-ttu-id="0f7c4-122">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="0f7c4-122">DOUBLE</span></span>           | <span data-ttu-id="0f7c4-123">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="0f7c4-123">TEMPLATE</span></span> |           |



 

<span data-ttu-id="0f7c4-124">L’en-tête de longueur variable est obligatoire et doit se trouver au début du flux de données.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-124">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="0f7c4-125">L’en-tête contient les données suivantes.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-125">The header contains the following data.</span></span>



| <span data-ttu-id="0f7c4-126">Type</span><span class="sxs-lookup"><span data-stu-id="0f7c4-126">Type</span></span>           | <span data-ttu-id="0f7c4-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0f7c4-127">Required</span></span> | <span data-ttu-id="0f7c4-128">Taille (en octets)</span><span class="sxs-lookup"><span data-stu-id="0f7c4-128">Size (in bytes)</span></span> | <span data-ttu-id="0f7c4-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f7c4-129">Value</span></span> | <span data-ttu-id="0f7c4-130">Description</span><span class="sxs-lookup"><span data-stu-id="0f7c4-130">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="0f7c4-131">Nombre magique</span><span class="sxs-lookup"><span data-stu-id="0f7c4-131">Magic Number</span></span>   | <span data-ttu-id="0f7c4-132">x</span><span class="sxs-lookup"><span data-stu-id="0f7c4-132">x</span></span>        | <span data-ttu-id="0f7c4-133">4</span><span class="sxs-lookup"><span data-stu-id="0f7c4-133">4</span></span>               | <span data-ttu-id="0f7c4-134">xof</span><span class="sxs-lookup"><span data-stu-id="0f7c4-134">xof</span></span>   |                              |
| <span data-ttu-id="0f7c4-135">Numéro de version</span><span class="sxs-lookup"><span data-stu-id="0f7c4-135">Version Number</span></span> | <span data-ttu-id="0f7c4-136">x</span><span class="sxs-lookup"><span data-stu-id="0f7c4-136">x</span></span>        | <span data-ttu-id="0f7c4-137">2</span><span class="sxs-lookup"><span data-stu-id="0f7c4-137">2</span></span>               | <span data-ttu-id="0f7c4-138">03</span><span class="sxs-lookup"><span data-stu-id="0f7c4-138">03</span></span>    | <span data-ttu-id="0f7c4-139">Version majeure 3</span><span class="sxs-lookup"><span data-stu-id="0f7c4-139">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="0f7c4-140">03</span><span class="sxs-lookup"><span data-stu-id="0f7c4-140">03</span></span>    | <span data-ttu-id="0f7c4-141">Version mineure 3</span><span class="sxs-lookup"><span data-stu-id="0f7c4-141">Minor version 3</span></span>              |
| <span data-ttu-id="0f7c4-142">Type de format</span><span class="sxs-lookup"><span data-stu-id="0f7c4-142">Format Type</span></span>    | <span data-ttu-id="0f7c4-143">x</span><span class="sxs-lookup"><span data-stu-id="0f7c4-143">x</span></span>        | <span data-ttu-id="0f7c4-144">4</span><span class="sxs-lookup"><span data-stu-id="0f7c4-144">4</span></span>               | <span data-ttu-id="0f7c4-145">txt</span><span class="sxs-lookup"><span data-stu-id="0f7c4-145">txt</span></span>   | <span data-ttu-id="0f7c4-146">Fichier texte</span><span class="sxs-lookup"><span data-stu-id="0f7c4-146">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="0f7c4-147">bin</span><span class="sxs-lookup"><span data-stu-id="0f7c4-147">bin</span></span>   | <span data-ttu-id="0f7c4-148">Fichier binaire</span><span class="sxs-lookup"><span data-stu-id="0f7c4-148">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="0f7c4-149">tzip</span><span class="sxs-lookup"><span data-stu-id="0f7c4-149">tzip</span></span>  | <span data-ttu-id="0f7c4-150">Fichier texte compressé MSZip</span><span class="sxs-lookup"><span data-stu-id="0f7c4-150">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="0f7c4-151">bzip</span><span class="sxs-lookup"><span data-stu-id="0f7c4-151">bzip</span></span>  | <span data-ttu-id="0f7c4-152">Fichier binaire compressé MSZip</span><span class="sxs-lookup"><span data-stu-id="0f7c4-152">MSZip compressed binary file</span></span> |
| <span data-ttu-id="0f7c4-153">Taille de la virgule flottante</span><span class="sxs-lookup"><span data-stu-id="0f7c4-153">Float Size</span></span>     | <span data-ttu-id="0f7c4-154">x</span><span class="sxs-lookup"><span data-stu-id="0f7c4-154">x</span></span>        | <span data-ttu-id="0f7c4-155">0064</span><span class="sxs-lookup"><span data-stu-id="0f7c4-155">0064</span></span>            |       | <span data-ttu-id="0f7c4-156">virgule flottante 64 bits</span><span class="sxs-lookup"><span data-stu-id="0f7c4-156">64-bit floats</span></span>                |
|                | <span data-ttu-id="0f7c4-157">x</span><span class="sxs-lookup"><span data-stu-id="0f7c4-157">x</span></span>        | <span data-ttu-id="0f7c4-158">« 0032 »</span><span class="sxs-lookup"><span data-stu-id="0f7c4-158">"0032"</span></span>          |       | <span data-ttu-id="0f7c4-159">virgule flottante 32 bits</span><span class="sxs-lookup"><span data-stu-id="0f7c4-159">32-bit floats</span></span>                |



 

<span data-ttu-id="0f7c4-160">Les valeurs de la table sont délimitées par des guillemets pour attirer l’attention sur le nombre de caractères de chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-160">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="0f7c4-161">Ceux qui comportent 4 octets contiennent quatre caractères, ceux avec 2 octets contiennent deux caractères.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-161">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="0f7c4-162">Les commentaires s’appliquent uniquement aux fichiers texte.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-162">Comments are applicable only in text files.</span></span> <span data-ttu-id="0f7c4-163">Des commentaires peuvent apparaître n’importe où dans le flux de données.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-163">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="0f7c4-164">Un commentaire commence par deux barres obliques (//) de style C++ ou par un signe dièse ( \# ).</span><span class="sxs-lookup"><span data-stu-id="0f7c4-164">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="0f7c4-165">Le commentaire s’exécute jusqu’à la nouvelle ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-165">The comment runs to the next new line.</span></span> <span data-ttu-id="0f7c4-166">L’exemple suivant montre des commentaires valides.</span><span class="sxs-lookup"><span data-stu-id="0f7c4-166">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="0f7c4-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0f7c4-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f7c4-168">Encodage de texte</span><span class="sxs-lookup"><span data-stu-id="0f7c4-168">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



