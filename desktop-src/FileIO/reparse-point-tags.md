---
description: Chaque point d’analyse a une balise d’identificateur, ce qui vous permet de distinguer efficacement les différents types de points d’analyse, sans avoir à examiner les données définies par l’utilisateur dans le point d’analyse.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Étiquettes de point d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536792"
---
# <a name="reparse-point-tags"></a><span data-ttu-id="e4c88-103">Étiquettes de point d’analyse</span><span class="sxs-lookup"><span data-stu-id="e4c88-103">Reparse Point Tags</span></span>

<span data-ttu-id="e4c88-104">Chaque point d’analyse a une balise d’identificateur, ce qui vous permet de distinguer efficacement les différents types de points d’analyse, sans avoir à examiner les données définies par l’utilisateur dans le point d’analyse.</span><span class="sxs-lookup"><span data-stu-id="e4c88-104">Each reparse point has an identifier tag so that you can efficiently differentiate between the different types of reparse points, without having to examine the user-defined data in the reparse point.</span></span> <span data-ttu-id="e4c88-105">Le système utilise un ensemble de balises prédéfinies et une plage de balises réservées pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e4c88-105">The system uses a set of predefined tags and a range of tags reserved for Microsoft.</span></span> <span data-ttu-id="e4c88-106">Si vous utilisez l’une des balises réservées lors de la définition d’un point d’analyse, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="e4c88-106">If you use any of the reserved tags when setting a reparse point, the operation fails.</span></span> <span data-ttu-id="e4c88-107">Les balises qui ne sont pas incluses dans ces plages ne sont pas réservées et sont disponibles pour votre application.</span><span class="sxs-lookup"><span data-stu-id="e4c88-107">Tags not included in these ranges are not reserved and are available for your application.</span></span>

<span data-ttu-id="e4c88-108">Lorsque vous définissez un point d’analyse, vous devez baliser les données à placer dans le point d’analyse.</span><span class="sxs-lookup"><span data-stu-id="e4c88-108">When you set a reparse point, you must tag the data to be placed in the reparse point.</span></span> <span data-ttu-id="e4c88-109">Une fois que le point d’analyse a été établi, une nouvelle opération set échoue si la balise pour les nouvelles données ne correspond pas à la balise pour les données existantes.</span><span class="sxs-lookup"><span data-stu-id="e4c88-109">After the reparse point has been established, a new set operation fails if the tag for the new data does not match the tag for the existing data.</span></span> <span data-ttu-id="e4c88-110">Si les balises correspondent, l’opération ensembliste remplace le point d’analyse existant.</span><span class="sxs-lookup"><span data-stu-id="e4c88-110">If the tags match, the set operation overwrites the existing reparse point.</span></span>

<span data-ttu-id="e4c88-111">Pour récupérer la balise de point d’analyse, utilisez la fonction [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) .</span><span class="sxs-lookup"><span data-stu-id="e4c88-111">To retrieve the reparse point tag, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) function.</span></span> <span data-ttu-id="e4c88-112">Si le membre **dwFileAttributes** contient l’attribut de point d' **analyse d’attribut de fichier \_ \_ \_** , le membre **dwReserved0** spécifie le point d’analyse.</span><span class="sxs-lookup"><span data-stu-id="e4c88-112">If the **dwFileAttributes** member includes the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute, then the **dwReserved0** member specifies the reparse point.</span></span>

## <a name="tag-contents"></a><span data-ttu-id="e4c88-113">Contenu de la balise</span><span class="sxs-lookup"><span data-stu-id="e4c88-113">Tag Contents</span></span>

<span data-ttu-id="e4c88-114">Les étiquettes d’analyse sont stockées sous forme de valeurs **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e4c88-114">Reparse tags are stored as **DWORD** values.</span></span> <span data-ttu-id="e4c88-115">Les bits définissent certains attributs, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="e4c88-115">The bits define certain attributes, as shown in the following diagram.</span></span>

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

<span data-ttu-id="e4c88-116">Les 16 bits de poids faible déterminent le type de point d’analyse.</span><span class="sxs-lookup"><span data-stu-id="e4c88-116">The low 16 bits determine the kind of reparse point.</span></span> <span data-ttu-id="e4c88-117">Les 16 bits de poids fort ont 12 bits réservés pour une utilisation future et 4 bits qui désignent des attributs spécifiques des balises et les données représentées par le point d’analyse.</span><span class="sxs-lookup"><span data-stu-id="e4c88-117">The high 16 bits have 12 bits reserved for future use and 4 bits that denote specific attributes of the tags and the data represented by the reparse point.</span></span> <span data-ttu-id="e4c88-118">Le tableau suivant décrit ces bits.</span><span class="sxs-lookup"><span data-stu-id="e4c88-118">The following table describes these bits.</span></span>



| <span data-ttu-id="e4c88-119">bit</span><span class="sxs-lookup"><span data-stu-id="e4c88-119">Bit</span></span> | <span data-ttu-id="e4c88-120">Description</span><span class="sxs-lookup"><span data-stu-id="e4c88-120">Description</span></span>                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c88-121">M</span><span class="sxs-lookup"><span data-stu-id="e4c88-121">M</span></span>   | <span data-ttu-id="e4c88-122">Microsoft bit.</span><span class="sxs-lookup"><span data-stu-id="e4c88-122">Microsoft bit.</span></span> <span data-ttu-id="e4c88-123">Si ce bit est défini, la balise est la propriété de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e4c88-123">If this bit is set, the tag is owned by Microsoft.</span></span> <span data-ttu-id="e4c88-124">Toutes les autres balises doivent utiliser la valeur zéro pour ce bit.</span><span class="sxs-lookup"><span data-stu-id="e4c88-124">All other tags must use zero for this bit.</span></span> |
| <span data-ttu-id="e4c88-125">R</span><span class="sxs-lookup"><span data-stu-id="e4c88-125">R</span></span>   | <span data-ttu-id="e4c88-126">Réservé doit être égal à zéro pour toutes les balises non-Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e4c88-126">Reserved; must be zero for all non-Microsoft tags.</span></span>                                                           |
| <span data-ttu-id="e4c88-127">N</span><span class="sxs-lookup"><span data-stu-id="e4c88-127">N</span></span>   | <span data-ttu-id="e4c88-128">Bit de substitution de nom.</span><span class="sxs-lookup"><span data-stu-id="e4c88-128">Name surrogate bit.</span></span> <span data-ttu-id="e4c88-129">Si ce bit est défini, le fichier ou le répertoire représente une autre entité nommée dans le système.</span><span class="sxs-lookup"><span data-stu-id="e4c88-129">If this bit is set, the file or directory represents another named entity in the system.</span></span> |



 

<span data-ttu-id="e4c88-130">Les macros suivantes permettent de tester les balises :</span><span class="sxs-lookup"><span data-stu-id="e4c88-130">The following macros exist to assist in testing tags:</span></span>

-   [<span data-ttu-id="e4c88-131">**IsReparseTagMicrosoft**</span><span class="sxs-lookup"><span data-stu-id="e4c88-131">**IsReparseTagMicrosoft**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [<span data-ttu-id="e4c88-132">**IsReparseTagNameSurrogate**</span><span class="sxs-lookup"><span data-stu-id="e4c88-132">**IsReparseTagNameSurrogate**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

<span data-ttu-id="e4c88-133">Chaque macro retourne une valeur différente de zéro si le bit associé est défini.</span><span class="sxs-lookup"><span data-stu-id="e4c88-133">Each macro returns a nonzero value if the associated bit is set.</span></span>

<span data-ttu-id="e4c88-134">Les éléments suivants sont des valeurs de balise de réanalyse prédéfinies de Microsoft ; ils sont définis dans Winnt. h :</span><span class="sxs-lookup"><span data-stu-id="e4c88-134">The following are Microsoft's predefined reparse tag values; they are defined in WinNT.h:</span></span>

-   <span data-ttu-id="e4c88-135">**IO_REPARSE_TAG_AF_UNIX**</span><span class="sxs-lookup"><span data-stu-id="e4c88-135">**IO_REPARSE_TAG_AF_UNIX**</span></span>
-   <span data-ttu-id="e4c88-136">**IO_REPARSE_TAG_APPEXECLINK**</span><span class="sxs-lookup"><span data-stu-id="e4c88-136">**IO_REPARSE_TAG_APPEXECLINK**</span></span>
-   <span data-ttu-id="e4c88-137">**IO_REPARSE_TAG_CLOUD**</span><span class="sxs-lookup"><span data-stu-id="e4c88-137">**IO_REPARSE_TAG_CLOUD**</span></span>
-   <span data-ttu-id="e4c88-138">**IO_REPARSE_TAG_CLOUD_1**</span><span class="sxs-lookup"><span data-stu-id="e4c88-138">**IO_REPARSE_TAG_CLOUD_1**</span></span>
-   <span data-ttu-id="e4c88-139">**IO_REPARSE_TAG_CLOUD_2**</span><span class="sxs-lookup"><span data-stu-id="e4c88-139">**IO_REPARSE_TAG_CLOUD_2**</span></span>
-   <span data-ttu-id="e4c88-140">**IO_REPARSE_TAG_CLOUD_3**</span><span class="sxs-lookup"><span data-stu-id="e4c88-140">**IO_REPARSE_TAG_CLOUD_3**</span></span>
-   <span data-ttu-id="e4c88-141">**IO_REPARSE_TAG_CLOUD_4**</span><span class="sxs-lookup"><span data-stu-id="e4c88-141">**IO_REPARSE_TAG_CLOUD_4**</span></span>
-   <span data-ttu-id="e4c88-142">**IO_REPARSE_TAG_CLOUD_5**</span><span class="sxs-lookup"><span data-stu-id="e4c88-142">**IO_REPARSE_TAG_CLOUD_5**</span></span>
-   <span data-ttu-id="e4c88-143">**IO_REPARSE_TAG_CLOUD_6**</span><span class="sxs-lookup"><span data-stu-id="e4c88-143">**IO_REPARSE_TAG_CLOUD_6**</span></span>
-   <span data-ttu-id="e4c88-144">**IO_REPARSE_TAG_CLOUD_7**</span><span class="sxs-lookup"><span data-stu-id="e4c88-144">**IO_REPARSE_TAG_CLOUD_7**</span></span>
-   <span data-ttu-id="e4c88-145">**IO_REPARSE_TAG_CLOUD_8**</span><span class="sxs-lookup"><span data-stu-id="e4c88-145">**IO_REPARSE_TAG_CLOUD_8**</span></span>
-   <span data-ttu-id="e4c88-146">**IO_REPARSE_TAG_CLOUD_9**</span><span class="sxs-lookup"><span data-stu-id="e4c88-146">**IO_REPARSE_TAG_CLOUD_9**</span></span>
-   <span data-ttu-id="e4c88-147">**IO_REPARSE_TAG_CLOUD_A**</span><span class="sxs-lookup"><span data-stu-id="e4c88-147">**IO_REPARSE_TAG_CLOUD_A**</span></span>
-   <span data-ttu-id="e4c88-148">**IO_REPARSE_TAG_CLOUD_B**</span><span class="sxs-lookup"><span data-stu-id="e4c88-148">**IO_REPARSE_TAG_CLOUD_B**</span></span>
-   <span data-ttu-id="e4c88-149">**IO_REPARSE_TAG_CLOUD_C**</span><span class="sxs-lookup"><span data-stu-id="e4c88-149">**IO_REPARSE_TAG_CLOUD_C**</span></span>
-   <span data-ttu-id="e4c88-150">**IO_REPARSE_TAG_CLOUD_D**</span><span class="sxs-lookup"><span data-stu-id="e4c88-150">**IO_REPARSE_TAG_CLOUD_D**</span></span>
-   <span data-ttu-id="e4c88-151">**IO_REPARSE_TAG_CLOUD_E**</span><span class="sxs-lookup"><span data-stu-id="e4c88-151">**IO_REPARSE_TAG_CLOUD_E**</span></span>
-   <span data-ttu-id="e4c88-152">**IO_REPARSE_TAG_CLOUD_F**</span><span class="sxs-lookup"><span data-stu-id="e4c88-152">**IO_REPARSE_TAG_CLOUD_F**</span></span>
-   <span data-ttu-id="e4c88-153">**IO_REPARSE_TAG_CLOUD_MASK**</span><span class="sxs-lookup"><span data-stu-id="e4c88-153">**IO_REPARSE_TAG_CLOUD_MASK**</span></span>
-   <span data-ttu-id="e4c88-154">**IO_REPARSE_TAG_CSV**</span><span class="sxs-lookup"><span data-stu-id="e4c88-154">**IO_REPARSE_TAG_CSV**</span></span>
-   <span data-ttu-id="e4c88-155">**IO_REPARSE_TAG_DEDUP**</span><span class="sxs-lookup"><span data-stu-id="e4c88-155">**IO_REPARSE_TAG_DEDUP**</span></span>
-   <span data-ttu-id="e4c88-156">**IO_REPARSE_TAG_DFS**</span><span class="sxs-lookup"><span data-stu-id="e4c88-156">**IO_REPARSE_TAG_DFS**</span></span>
-   <span data-ttu-id="e4c88-157">**IO_REPARSE_TAG_DFSR**</span><span class="sxs-lookup"><span data-stu-id="e4c88-157">**IO_REPARSE_TAG_DFSR**</span></span>
-   <span data-ttu-id="e4c88-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span><span class="sxs-lookup"><span data-stu-id="e4c88-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span></span>
-   <span data-ttu-id="e4c88-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span><span class="sxs-lookup"><span data-stu-id="e4c88-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span></span>
-   <span data-ttu-id="e4c88-160">**IO_REPARSE_TAG_HSM**</span><span class="sxs-lookup"><span data-stu-id="e4c88-160">**IO_REPARSE_TAG_HSM**</span></span>
-   <span data-ttu-id="e4c88-161">**IO_REPARSE_TAG_HSM2**</span><span class="sxs-lookup"><span data-stu-id="e4c88-161">**IO_REPARSE_TAG_HSM2**</span></span>
-   <span data-ttu-id="e4c88-162">**IO_REPARSE_TAG_MOUNT_POINT**</span><span class="sxs-lookup"><span data-stu-id="e4c88-162">**IO_REPARSE_TAG_MOUNT_POINT**</span></span>
-   <span data-ttu-id="e4c88-163">**IO_REPARSE_TAG_NFS**</span><span class="sxs-lookup"><span data-stu-id="e4c88-163">**IO_REPARSE_TAG_NFS**</span></span>
-   <span data-ttu-id="e4c88-164">**IO_REPARSE_TAG_ONEDRIVE**</span><span class="sxs-lookup"><span data-stu-id="e4c88-164">**IO_REPARSE_TAG_ONEDRIVE**</span></span>
-   <span data-ttu-id="e4c88-165">**IO_REPARSE_TAG_PROJFS**</span><span class="sxs-lookup"><span data-stu-id="e4c88-165">**IO_REPARSE_TAG_PROJFS**</span></span>
-   <span data-ttu-id="e4c88-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="e4c88-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span></span>
-   <span data-ttu-id="e4c88-167">**IO_REPARSE_TAG_SIS**</span><span class="sxs-lookup"><span data-stu-id="e4c88-167">**IO_REPARSE_TAG_SIS**</span></span>
-   <span data-ttu-id="e4c88-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span><span class="sxs-lookup"><span data-stu-id="e4c88-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span></span>
-   <span data-ttu-id="e4c88-169">**IO_REPARSE_TAG_SYMLINK**</span><span class="sxs-lookup"><span data-stu-id="e4c88-169">**IO_REPARSE_TAG_SYMLINK**</span></span>
-   <span data-ttu-id="e4c88-170">**IO_REPARSE_TAG_UNHANDLED**</span><span class="sxs-lookup"><span data-stu-id="e4c88-170">**IO_REPARSE_TAG_UNHANDLED**</span></span>
-   <span data-ttu-id="e4c88-171">**IO_REPARSE_TAG_WCI**</span><span class="sxs-lookup"><span data-stu-id="e4c88-171">**IO_REPARSE_TAG_WCI**</span></span>
-   <span data-ttu-id="e4c88-172">**IO_REPARSE_TAG_WCI_1**</span><span class="sxs-lookup"><span data-stu-id="e4c88-172">**IO_REPARSE_TAG_WCI_1**</span></span>
-   <span data-ttu-id="e4c88-173">**IO_REPARSE_TAG_WCI_LINK**</span><span class="sxs-lookup"><span data-stu-id="e4c88-173">**IO_REPARSE_TAG_WCI_LINK**</span></span>
-   <span data-ttu-id="e4c88-174">**IO_REPARSE_TAG_WCI_LINK_1**</span><span class="sxs-lookup"><span data-stu-id="e4c88-174">**IO_REPARSE_TAG_WCI_LINK_1**</span></span>
-   <span data-ttu-id="e4c88-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="e4c88-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span></span>
-   <span data-ttu-id="e4c88-176">**IO_REPARSE_TAG_WIM**</span><span class="sxs-lookup"><span data-stu-id="e4c88-176">**IO_REPARSE_TAG_WIM**</span></span>
-   <span data-ttu-id="e4c88-177">**IO_REPARSE_TAG_WOF**</span><span class="sxs-lookup"><span data-stu-id="e4c88-177">**IO_REPARSE_TAG_WOF**</span></span>

<span data-ttu-id="e4c88-178">Pour garantir l’unicité des balises, Microsoft fournit un mécanisme permettant de distribuer de nouvelles balises.</span><span class="sxs-lookup"><span data-stu-id="e4c88-178">To ensure uniqueness of tags, Microsoft provides a mechanism to distribute new tags.</span></span> <span data-ttu-id="e4c88-179">Pour plus d’informations, consultez le [Kit IFS (Installable File System)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span><span class="sxs-lookup"><span data-stu-id="e4c88-179">For more information, see the [Installable File System (IFS) Kit](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span></span>

 

 



