---
description: Options de format de fichier X, de chargement et d’enregistrement.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e230fc08ac4d7f8713959f2025f67262046ecea5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343644"
---
# <a name="d3dxf"></a><span data-ttu-id="062ba-103">D3DXF</span><span class="sxs-lookup"><span data-stu-id="062ba-103">D3DXF</span></span>

<span data-ttu-id="062ba-104">Options de format de fichier X, de chargement et d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="062ba-104">X file format, load, and save options.</span></span>

## <a name="file-formats"></a><span data-ttu-id="062ba-105">Formats de fichier</span><span class="sxs-lookup"><span data-stu-id="062ba-105">File Formats</span></span>

<span data-ttu-id="062ba-106">Le tableau suivant spécifie le type de données de fichier :</span><span class="sxs-lookup"><span data-stu-id="062ba-106">The following table specifies the type of file data:</span></span>



| <span data-ttu-id="062ba-107">\#définit le format de fichier</span><span class="sxs-lookup"><span data-stu-id="062ba-107">\#defines for File Format</span></span>     | <span data-ttu-id="062ba-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="062ba-108">Value</span></span> | <span data-ttu-id="062ba-109">Description</span><span class="sxs-lookup"><span data-stu-id="062ba-109">Description</span></span>                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="062ba-110">D3DXF \_ FILEFORMAT \_ binaire</span><span class="sxs-lookup"><span data-stu-id="062ba-110">D3DXF\_FILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="062ba-111">0</span><span class="sxs-lookup"><span data-stu-id="062ba-111">0</span></span>     | <span data-ttu-id="062ba-112">Fichier binaire au format hérité.</span><span class="sxs-lookup"><span data-stu-id="062ba-112">Legacy-format binary file.</span></span> <span data-ttu-id="062ba-113">Consultez [référence de fichier X (héritée)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="062ba-113">See [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span> |
| <span data-ttu-id="062ba-114">\_Texte du FILEFORMAT D3DXF \_</span><span class="sxs-lookup"><span data-stu-id="062ba-114">D3DXF\_FILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="062ba-115">1</span><span class="sxs-lookup"><span data-stu-id="062ba-115">1</span></span>     | <span data-ttu-id="062ba-116">Fichier texte.</span><span class="sxs-lookup"><span data-stu-id="062ba-116">Text file.</span></span>                                                                                     |
| <span data-ttu-id="062ba-117">D3DXF \_ FILEFORMAT \_ compressé</span><span class="sxs-lookup"><span data-stu-id="062ba-117">D3DXF\_FILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="062ba-118">2</span><span class="sxs-lookup"><span data-stu-id="062ba-118">2</span></span>     | <span data-ttu-id="062ba-119">Fichier compressé.</span><span class="sxs-lookup"><span data-stu-id="062ba-119">Compressed file.</span></span> <span data-ttu-id="062ba-120">Avec cet indicateur, vous devez également spécifier le format binaire ou le format texte.</span><span class="sxs-lookup"><span data-stu-id="062ba-120">With this flag, you must also specify the binary format or the text format.</span></span>   |



 

## <a name="file-load-options"></a><span data-ttu-id="062ba-121">Options de chargement de fichier</span><span class="sxs-lookup"><span data-stu-id="062ba-121">File Load Options</span></span>

<span data-ttu-id="062ba-122">Le tableau suivant spécifie les options de chargement de fichier avec des fichiers. x :</span><span class="sxs-lookup"><span data-stu-id="062ba-122">The following table specifies file load options with .x files:</span></span>



| <span data-ttu-id="062ba-123">\#définition</span><span class="sxs-lookup"><span data-stu-id="062ba-123">\#define</span></span>                      | <span data-ttu-id="062ba-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="062ba-124">Value</span></span> | <span data-ttu-id="062ba-125">Description</span><span class="sxs-lookup"><span data-stu-id="062ba-125">Description</span></span>                |
|-------------------------------|-------|----------------------------|
| <span data-ttu-id="062ba-126">D3DXF \_ FILELOAD \_ FromFile</span><span class="sxs-lookup"><span data-stu-id="062ba-126">D3DXF\_FILELOAD\_FromFile</span></span>     | <span data-ttu-id="062ba-127">0</span><span class="sxs-lookup"><span data-stu-id="062ba-127">0</span></span>     | <span data-ttu-id="062ba-128">Charger des données à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="062ba-128">Load data from a file.</span></span>     |
| <span data-ttu-id="062ba-129">D3DXF \_ FILELOAD \_ FROMWFILE</span><span class="sxs-lookup"><span data-stu-id="062ba-129">D3DXF\_FILELOAD\_FROMWFILE</span></span>    | <span data-ttu-id="062ba-130">1</span><span class="sxs-lookup"><span data-stu-id="062ba-130">1</span></span>     | <span data-ttu-id="062ba-131">Charger des données à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="062ba-131">Load data from a file.</span></span>     |
| <span data-ttu-id="062ba-132">D3DXF \_ FILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="062ba-132">D3DXF\_FILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="062ba-133">2</span><span class="sxs-lookup"><span data-stu-id="062ba-133">2</span></span>     | <span data-ttu-id="062ba-134">Charger des données à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="062ba-134">Load data from a resource.</span></span> |
| <span data-ttu-id="062ba-135">D3DXF \_ FILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="062ba-135">D3DXF\_FILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="062ba-136">3</span><span class="sxs-lookup"><span data-stu-id="062ba-136">3</span></span>     | <span data-ttu-id="062ba-137">Chargez des données à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="062ba-137">Load data from memory.</span></span>     |



 

## <a name="file-save-options"></a><span data-ttu-id="062ba-138">Options d’enregistrement de fichier</span><span class="sxs-lookup"><span data-stu-id="062ba-138">File Save Options</span></span>

<span data-ttu-id="062ba-139">Le tableau suivant spécifie les options d’enregistrement et de chargement de fichiers avec des fichiers. x :</span><span class="sxs-lookup"><span data-stu-id="062ba-139">The following table specifies file save and load options with .x files:</span></span>



| <span data-ttu-id="062ba-140">\#définition</span><span class="sxs-lookup"><span data-stu-id="062ba-140">\#define</span></span>                 | <span data-ttu-id="062ba-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="062ba-141">Value</span></span> | <span data-ttu-id="062ba-142">Description</span><span class="sxs-lookup"><span data-stu-id="062ba-142">Description</span></span>                    |
|--------------------------|-------|--------------------------------|
| <span data-ttu-id="062ba-143">D3DXF \_ FichierEnregistrer \_ TOFILE</span><span class="sxs-lookup"><span data-stu-id="062ba-143">D3DXF\_FILESAVE\_TOFILE</span></span>  | <span data-ttu-id="062ba-144">0</span><span class="sxs-lookup"><span data-stu-id="062ba-144">0</span></span>     | <span data-ttu-id="062ba-145">Enregistrer dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="062ba-145">Save to a file.</span></span>                |
| <span data-ttu-id="062ba-146">D3DXF \_ FichierEnregistrer \_ TOWFILE</span><span class="sxs-lookup"><span data-stu-id="062ba-146">D3DXF\_FILESAVE\_TOWFILE</span></span> | <span data-ttu-id="062ba-147">1</span><span class="sxs-lookup"><span data-stu-id="062ba-147">1</span></span>     | <span data-ttu-id="062ba-148">Enregistrez dans un fichier à caractères larges.</span><span class="sxs-lookup"><span data-stu-id="062ba-148">Save to a wide-character file.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="062ba-149">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="062ba-149">Constant Information</span></span>



| <span data-ttu-id="062ba-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="062ba-150">Requirement</span></span>                         | <span data-ttu-id="062ba-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="062ba-151">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="062ba-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="062ba-152">Header</span></span>                   | <span data-ttu-id="062ba-153">d3dx9xof. h</span><span class="sxs-lookup"><span data-stu-id="062ba-153">d3dx9xof.h</span></span> |
| <span data-ttu-id="062ba-154">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="062ba-154">Minimum operating system</span></span> | <span data-ttu-id="062ba-155">Windows 98</span><span class="sxs-lookup"><span data-stu-id="062ba-155">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="062ba-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="062ba-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="062ba-157">Constantes de fichier D3DX X</span><span class="sxs-lookup"><span data-stu-id="062ba-157">D3DX X File Constants</span></span>](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[<span data-ttu-id="062ba-158">**D3DXSaveMeshToX**</span><span class="sxs-lookup"><span data-stu-id="062ba-158">**D3DXSaveMeshToX**</span></span>](d3dxsavemeshtox.md)
</dt> </dl>

 

 



