---
title: Structure DRM_LICENSE_STATE_DATA (Drmexternals. h)
description: La \_ structure des \_ données d’état de licence DRM contient des informations de \_ licence sur un droit DRM spécifié.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- Structure DRM_LICENSE_STATE_DATA format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536915"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a><span data-ttu-id="e0dde-105">Structure DRM_LICENSE_STATE_DATA (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="e0dde-105">DRM_LICENSE_STATE_DATA structure (Drmexternals.h)</span></span>

<span data-ttu-id="e0dde-106">La structure des **données d’état de \_ licence \_ \_ DRM** contient des informations de [*licence*](wmformat-glossary.md) sur un droit [*DRM*](wmformat-glossary.md) spécifié.</span><span class="sxs-lookup"><span data-stu-id="e0dde-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains [*license*](wmformat-glossary.md) information about a specified [*DRM*](wmformat-glossary.md) right.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0dde-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0dde-107">Syntax</span></span>


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a><span data-ttu-id="e0dde-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e0dde-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0dde-109">**dwStreamId**</span><span class="sxs-lookup"><span data-stu-id="e0dde-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="e0dde-110">Numéro de flux auquel la licence s’applique.</span><span class="sxs-lookup"><span data-stu-id="e0dde-110">Stream number to which the license applies.</span></span> <span data-ttu-id="e0dde-111">Doit avoir la valeur 0, ce qui indique que la licence s’applique à tous les flux du fichier.</span><span class="sxs-lookup"><span data-stu-id="e0dde-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="e0dde-112">**dwCategory**</span><span class="sxs-lookup"><span data-stu-id="e0dde-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="e0dde-113">Catégorie de chaîne à afficher.</span><span class="sxs-lookup"><span data-stu-id="e0dde-113">Category of string to be displayed.</span></span> <span data-ttu-id="e0dde-114">Consultez [**\_ catégorie d' \_ état \_ de licence DRM**](drm-license-state-category.md) pour connaître les valeurs possibles et leur signification.</span><span class="sxs-lookup"><span data-stu-id="e0dde-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="e0dde-115">**dwNumCounts**</span><span class="sxs-lookup"><span data-stu-id="e0dde-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="e0dde-116">Nombre d’éléments fournis dans **dwCount**.</span><span class="sxs-lookup"><span data-stu-id="e0dde-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="e0dde-117">Cette valeur est généralement 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="e0dde-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="e0dde-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="e0dde-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="e0dde-119">Tableau de 0 ou 1 ou plusieurs **DWORD** s qui représentent le nombre de fois que l’action spécifiée dans **dwCategory** peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="e0dde-119">An array of 0 or 1 or more **DWORD** s that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="e0dde-120">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="e0dde-120">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e0dde-121">**dwNumDates**</span><span class="sxs-lookup"><span data-stu-id="e0dde-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="e0dde-122">Nombre d’éléments fournis dans **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="e0dde-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="e0dde-123">En règle générale, il n’est pas possible d’utiliser plus de deux dates, par exemple avec une licence valide à partir d’une date jusqu’à une autre date.</span><span class="sxs-lookup"><span data-stu-id="e0dde-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="e0dde-124">**DATEHEURE \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="e0dde-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="e0dde-125">Tableau d’une ou de plusieurs structures FILETIME représentant une ou plusieurs dates dans la licence.</span><span class="sxs-lookup"><span data-stu-id="e0dde-125">An array of one or more FILETIME structures representing one or more dates in the license.</span></span> <span data-ttu-id="e0dde-126">La signification d’une date particulière dépend de la valeur de **dwCategory**.</span><span class="sxs-lookup"><span data-stu-id="e0dde-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="e0dde-127">**dwVague**</span><span class="sxs-lookup"><span data-stu-id="e0dde-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="e0dde-128">Zéro, un ou plusieurs des indicateurs suivants combinés avec une **opération or** au niveau du bit :</span><span class="sxs-lookup"><span data-stu-id="e0dde-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="e0dde-129">Indicateur</span><span class="sxs-lookup"><span data-stu-id="e0dde-129">Flag</span></span>                                    | <span data-ttu-id="e0dde-130">Description</span><span class="sxs-lookup"><span data-stu-id="e0dde-130">Description</span></span>                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0dde-131">données d’état de la \_ licence DRM \_ \_ \_ vague</span><span class="sxs-lookup"><span data-stu-id="e0dde-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="e0dde-132">Si cette valeur est définie, il peut y avoir plus de licences qui s’appliquent au contenu.</span><span class="sxs-lookup"><span data-stu-id="e0dde-132">If set, there may be more licenses that apply to the content.</span></span>                                                                                         |
| <span data-ttu-id="e0dde-133">\_OPL de données d’état de licence DRM \_ \_ \_ \_ présent</span><span class="sxs-lookup"><span data-stu-id="e0dde-133">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="e0dde-134">Si cette option est définie, la licence comprend des niveaux de protection de sortie (OPLs) qui doivent être récupérés et vérifiés par rapport à la destination de la sortie de votre application.</span><span class="sxs-lookup"><span data-stu-id="e0dde-134">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span> |
| <span data-ttu-id="e0dde-135">données d’état de la \_ licence DRM \_ \_ \_ \_ présentes</span><span class="sxs-lookup"><span data-stu-id="e0dde-135">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="e0dde-136">S’il est défini, le contenu doit être remis à l’aide d’un chemin d’accès audio sécurisé (SAP).</span><span class="sxs-lookup"><span data-stu-id="e0dde-136">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0dde-137">Notes</span><span class="sxs-lookup"><span data-stu-id="e0dde-137">Remarks</span></span>

<span data-ttu-id="e0dde-138">Cette structure est retournée (encapsulée dans une structure de [**\_ données d' \_ état \_ de licence WM**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) ) à partir d’un appel à [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) lorsque vous spécifiez l’une des propriétés d’état de licence DRM.</span><span class="sxs-lookup"><span data-stu-id="e0dde-138">This structure is returned (encapsulated in a [**WM\_LICENSE\_STATE\_DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) structure) from a call to [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) when you specify one of the DRM license state properties.</span></span> <span data-ttu-id="e0dde-139">Ces propriétés sont :</span><span class="sxs-lookup"><span data-stu-id="e0dde-139">These properties are:</span></span>

-   [<span data-ttu-id="e0dde-140">**\_Lecture DRM LicenseState \_**</span><span class="sxs-lookup"><span data-stu-id="e0dde-140">**DRM\_LicenseState\_Playback**</span></span>](drm-licensestate-playback.md)
-   [<span data-ttu-id="e0dde-141">**\_LICENSESTATE DRM \_ CopyToCD**</span><span class="sxs-lookup"><span data-stu-id="e0dde-141">**DRM\_LicenseState\_CopyToCD**</span></span>](drm-licensestate-copytocd.md)
-   [<span data-ttu-id="e0dde-142">**\_LICENSESTATE DRM \_ CopyToSDMIDevice**</span><span class="sxs-lookup"><span data-stu-id="e0dde-142">**DRM\_LicenseState\_CopyToSDMIDevice**</span></span>](drm-licensestate-copytosdmidevice.md)
-   [<span data-ttu-id="e0dde-143">**\_LICENSESTATE DRM \_ CopyToNonSDMIDevice**</span><span class="sxs-lookup"><span data-stu-id="e0dde-143">**DRM\_LicenseState\_CopyToNonSDMIDevice**</span></span>](drm-licensestate-copytononsdmidevice.md)
-   [<span data-ttu-id="e0dde-144">**\_LICENSESTATE DRM \_ CollaborativePlay**</span><span class="sxs-lookup"><span data-stu-id="e0dde-144">**DRM\_LicenseState\_CollaborativePlay**</span></span>](drm-licensestate-collaborativeplay.md)
-   [<span data-ttu-id="e0dde-145">**\_Copie DRM LicenseState \_**</span><span class="sxs-lookup"><span data-stu-id="e0dde-145">**DRM\_LicenseState\_Copy**</span></span>](drm-licensestate-copy.md)
-   [<span data-ttu-id="e0dde-146">**\_LICENSESTATE DRM \_ PlaylistBurn**</span><span class="sxs-lookup"><span data-stu-id="e0dde-146">**DRM\_LicenseState\_PlaylistBurn**</span></span>](drm-licensestate-playlistburn.md)

<span data-ttu-id="e0dde-147">Si **dwCategory** est **le \_ \_ \_ nombre d’États de licence WM DRM \_ \_ de \_ until,** le tableau **DateTime** contient généralement deux dates, une date « from » et une date « until ».</span><span class="sxs-lookup"><span data-stu-id="e0dde-147">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL,** then the **datetime** array will typically contain two dates, a "from" date and an "until" date.</span></span> <span data-ttu-id="e0dde-148">Il est également possible de spécifier deux paires de dates pour créer des licences plus complexes.</span><span class="sxs-lookup"><span data-stu-id="e0dde-148">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="e0dde-149">Les éléments du tableau **dwCount** correspondent aux dates ou aux plages de dates spécifiées dans le tableau **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="e0dde-149">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="e0dde-150">Si **dwCategory** est **le \_ \_ \_ nombre d’États de licence WM DRM \_ \_ de \_ until et que** **DateTime** contient une paire de dates, **dwCount** contient un élément.</span><span class="sxs-lookup"><span data-stu-id="e0dde-150">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="e0dde-151">Si **DateTime** contient deux paires de dates (quatre éléments), **dwCount** doit contenir deux éléments, un pour chaque paire de dates.</span><span class="sxs-lookup"><span data-stu-id="e0dde-151">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="e0dde-152">Dans certains cas, les utilisateurs ont peut-être émis plus d’une licence pour un fichier.</span><span class="sxs-lookup"><span data-stu-id="e0dde-152">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="e0dde-153">Par exemple, ils peuvent avoir acquis une licence qui a autorisé cinq lectures jusqu’à la fin du mois et acquis ultérieurement une deuxième licence pour des droits illimités.</span><span class="sxs-lookup"><span data-stu-id="e0dde-153">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="e0dde-154">Dans ce cas, l’indicateur de \_ données de l' \_ État de licence DRM \_ \_ est défini dans **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) et le composant DRM utilise un algorithme pour déterminer l’ensemble de droits le plus probable qui ont été appliqués.</span><span class="sxs-lookup"><span data-stu-id="e0dde-154">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="e0dde-155">Lorsqu’une licence expire, le composant DRM examine les licences restantes, et ainsi de suite jusqu’à ce que toutes les licences aient expiré.</span><span class="sxs-lookup"><span data-stu-id="e0dde-155">When one license expires, the DRM component will examine the remaining license(s), and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0dde-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0dde-156">Requirements</span></span>



| <span data-ttu-id="e0dde-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0dde-157">Requirement</span></span> | <span data-ttu-id="e0dde-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0dde-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0dde-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0dde-159">Minimum supported client</span></span><br/> | <span data-ttu-id="e0dde-160">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0dde-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e0dde-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0dde-161">Minimum supported server</span></span><br/> | <span data-ttu-id="e0dde-162">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0dde-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e0dde-163">Version</span><span class="sxs-lookup"><span data-stu-id="e0dde-163">Version</span></span><br/>                  | <span data-ttu-id="e0dde-164">SDK Windows Media Format 7 ou versions ultérieures du kit de développement logiciel (SDK)</span><span class="sxs-lookup"><span data-stu-id="e0dde-164">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="e0dde-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0dde-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0dde-166"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0dde-166"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0dde-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0dde-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0dde-168">**Structures**</span><span class="sxs-lookup"><span data-stu-id="e0dde-168">**Structures**</span></span>](structures.md)
</dt> </dl>

 

