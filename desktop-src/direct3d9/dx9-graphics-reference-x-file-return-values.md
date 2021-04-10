---
description: Les méthodes utilisées pour travailler avec des fichiers DirectX. x peuvent retourner les valeurs suivantes en plus des valeurs de retour COM standard. Action déconseillée.
ms.assetid: a91168bc-966a-47b5-ba83-fc480593228d
title: Valeurs de retour (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Return
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 7d465b9759d958cba06bf0b950bc67772fbb84a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762133"
---
# <a name="return-values-dxfileh"></a><span data-ttu-id="1e724-104">Valeurs de retour (DXFile. h)</span><span class="sxs-lookup"><span data-stu-id="1e724-104">Return Values (DXFile.h)</span></span>

<span data-ttu-id="1e724-105">Les méthodes utilisées pour travailler avec des fichiers DirectX. x peuvent retourner les valeurs suivantes en plus des valeurs de retour COM standard.</span><span class="sxs-lookup"><span data-stu-id="1e724-105">The methods used to work with DirectX .x files can return the following values in addition to the standard COM return values.</span></span> <span data-ttu-id="1e724-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="1e724-106">Deprecated.</span></span>

<dl> <dt>

<span data-ttu-id="1e724-107"><span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE \_ OK**</span><span class="sxs-lookup"><span data-stu-id="1e724-107"><span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-108">Command completed successfully.</span><span class="sxs-lookup"><span data-stu-id="1e724-108">Command completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-109"><span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**DXFILEERR \_ BADALLOC**</span><span class="sxs-lookup"><span data-stu-id="1e724-109"><span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**DXFILEERR\_BADALLOC**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-110">L'allocation de mémoire a échoué.</span><span class="sxs-lookup"><span data-stu-id="1e724-110">Memory allocation failed.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-111"><span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**DXFILEERR \_ BADARRAYSIZE**</span><span class="sxs-lookup"><span data-stu-id="1e724-111"><span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**DXFILEERR\_BADARRAYSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-112">La taille du tableau n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-112">Array size is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-113"><span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**DXFILEERR \_ BADCACHEFILE**</span><span class="sxs-lookup"><span data-stu-id="1e724-113"><span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**DXFILEERR\_BADCACHEFILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-114">Le fichier cache contenant la date du fichier. x n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-114">The cache file containing the .x file date is invalid.</span></span> <span data-ttu-id="1e724-115">Un fichier cache contient les données extraites du réseau, mises en cache sur le disque dur et récupérées dans les demandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e724-115">A cache file contains data retrieved from the network, cached on the hard disk, and retrieved in subsequent requests.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-116"><span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**DXFILEERR \_ BADDataReference**</span><span class="sxs-lookup"><span data-stu-id="1e724-116"><span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**DXFILEERR\_BADDataReference**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-117">La référence de données n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-117">Data reference is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-118"><span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**DXFILEERR \_ BadFile**</span><span class="sxs-lookup"><span data-stu-id="1e724-118"><span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**DXFILEERR\_BADFILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-119">Le fichier n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-119">File is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-120"><span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**DXFILEERR \_ BADFILECOMPRESSIONTYPE**</span><span class="sxs-lookup"><span data-stu-id="1e724-120"><span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**DXFILEERR\_BADFILECOMPRESSIONTYPE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-121">Le type de compression de fichier n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-121">File compression type is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-122"><span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**DXFILEERR \_ BADFILEFLOATSIZE**</span><span class="sxs-lookup"><span data-stu-id="1e724-122"><span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**DXFILEERR\_BADFILEFLOATSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-123">La taille à virgule flottante n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-123">Floating-point size is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-124"><span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**DXFILEERR \_ BADFILETYPE**</span><span class="sxs-lookup"><span data-stu-id="1e724-124"><span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**DXFILEERR\_BADFILETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-125">Le fichier n’est pas un fichier DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="1e724-125">File is not a DirectX .x file.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-126"><span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**DXFILEERR \_ BADFILEVERSION**</span><span class="sxs-lookup"><span data-stu-id="1e724-126"><span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**DXFILEERR\_BADFILEVERSION**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-127">La version du fichier n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-127">File version is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-128"><span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**DXFILEERR \_ BADINTRINSICS**</span><span class="sxs-lookup"><span data-stu-id="1e724-128"><span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**DXFILEERR\_BADINTRINSICS**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-129">Les intrinsèques ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="1e724-129">Intrinsics are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-130"><span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**DXFILEERR \_ BADOBJECT**</span><span class="sxs-lookup"><span data-stu-id="1e724-130"><span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**DXFILEERR\_BADOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-131">L'objet n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-131">Object is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-132"><span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**DXFILEERR \_ BADRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="1e724-132"><span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**DXFILEERR\_BADRESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-133">La ressource n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-133">Resource is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-134"><span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**DXFILEERR \_ BADSTREAMHANDLE**</span><span class="sxs-lookup"><span data-stu-id="1e724-134"><span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**DXFILEERR\_BADSTREAMHANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-135">Le descripteur de flux n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-135">Stream handle is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-136"><span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**DXFILEERR \_ BADTYPE**</span><span class="sxs-lookup"><span data-stu-id="1e724-136"><span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**DXFILEERR\_BADTYPE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-137">Le type d’objet n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-137">Object type is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-138"><span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**DXFILEERR \_ BADVALUE**</span><span class="sxs-lookup"><span data-stu-id="1e724-138"><span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**DXFILEERR\_BADVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-139">Le paramètre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1e724-139">Parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-140"><span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**DXFILEERR \_ FILENOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="1e724-140"><span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**DXFILEERR\_FILENOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-141">Fichier introuvable.</span><span class="sxs-lookup"><span data-stu-id="1e724-141">File could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-142"><span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**DXFILEERR \_ INTERNALERROR**</span><span class="sxs-lookup"><span data-stu-id="1e724-142"><span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**DXFILEERR\_INTERNALERROR**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-143">Une erreur interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1e724-143">Internal error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-144"><span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR \_ NOinternet**</span><span class="sxs-lookup"><span data-stu-id="1e724-144"><span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR\_NOINTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-145">Connexion Internet introuvable.</span><span class="sxs-lookup"><span data-stu-id="1e724-145">Internet connection not found.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-146"><span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**DXFILEERR \_ NOMOREDATA**</span><span class="sxs-lookup"><span data-stu-id="1e724-146"><span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**DXFILEERR\_NOMOREDATA**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-147">Aucune autre donnée n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="1e724-147">No further data is available.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-148"><span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**DXFILEERR \_ NOMOREOBJECTS**</span><span class="sxs-lookup"><span data-stu-id="1e724-148"><span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**DXFILEERR\_NOMOREOBJECTS**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-149">Tous les objets ont été énumérés.</span><span class="sxs-lookup"><span data-stu-id="1e724-149">All objects have been enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-150"><span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**DXFILEERR \_ NOMORESTREAMHANDLES**</span><span class="sxs-lookup"><span data-stu-id="1e724-150"><span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**DXFILEERR\_NOMORESTREAMHANDLES**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-151">Aucun handle de flux n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="1e724-151">No stream handles are available.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-152"><span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**DXFILEERR \_ NOTDONEYET**</span><span class="sxs-lookup"><span data-stu-id="1e724-152"><span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**DXFILEERR\_NOTDONEYET**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-153">L’opération n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="1e724-153">Operation has not completed.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-154"><span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**DXFILEERR \_ NotFound**</span><span class="sxs-lookup"><span data-stu-id="1e724-154"><span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**DXFILEERR\_NOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-155">Objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="1e724-155">Object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-156"><span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR \_ PARSEERROR**</span><span class="sxs-lookup"><span data-stu-id="1e724-156"><span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR\_PARSEERROR**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-157">Impossible d’analyser le fichier.</span><span class="sxs-lookup"><span data-stu-id="1e724-157">File could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-158"><span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**DXFILEERR \_ RESOURCENOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="1e724-158"><span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**DXFILEERR\_RESOURCENOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-159">Ressource introuvable.</span><span class="sxs-lookup"><span data-stu-id="1e724-159">Resource could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-160"><span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**DXFILEERR \_ NOtemplate**</span><span class="sxs-lookup"><span data-stu-id="1e724-160"><span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**DXFILEERR\_NOTEMPLATE**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-161">Aucun modèle disponible.</span><span class="sxs-lookup"><span data-stu-id="1e724-161">No template available.</span></span>

</dd> <dt>

<span data-ttu-id="1e724-162"><span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**DXFILEERR \_ URLNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="1e724-162"><span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**DXFILEERR\_URLNOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="1e724-163">URL introuvable.</span><span class="sxs-lookup"><span data-stu-id="1e724-163">URL could not be found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e724-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e724-164">Requirements</span></span>



| <span data-ttu-id="1e724-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e724-165">Requirement</span></span> | <span data-ttu-id="1e724-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e724-166">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1e724-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e724-167">Header</span></span><br/> | <dl> <span data-ttu-id="1e724-168"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e724-168"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e724-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e724-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e724-170">Référence de fichier X (héritée)</span><span class="sxs-lookup"><span data-stu-id="1e724-170">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 




