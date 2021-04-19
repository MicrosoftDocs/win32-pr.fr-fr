---
title: Structure DRM_LICENSE_STATE_DATA (wmdrmsdk. h)
description: La \_ \_ \_ structure des données d’état de licence DRM contient des informations sur les restrictions de licence pour un droit DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- Structure DRM_LICENSE_STATE_DATA format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545577"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a><span data-ttu-id="aa216-105">Structure DRM_LICENSE_STATE_DATA (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="aa216-105">DRM_LICENSE_STATE_DATA structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="aa216-106">La structure des **\_ données d' \_ état \_ de licence DRM** contient des informations sur les restrictions de licence pour un droit DRM.</span><span class="sxs-lookup"><span data-stu-id="aa216-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains information about the license restrictions for a DRM right.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa216-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa216-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="aa216-108">Membres</span><span class="sxs-lookup"><span data-stu-id="aa216-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa216-109">**dwStreamId**</span><span class="sxs-lookup"><span data-stu-id="aa216-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="aa216-110">Numéro de flux auquel la licence s’applique.</span><span class="sxs-lookup"><span data-stu-id="aa216-110">Stream number to which the license applies.</span></span> <span data-ttu-id="aa216-111">Doit avoir la valeur 0, ce qui indique que la licence s’applique à tous les flux du fichier.</span><span class="sxs-lookup"><span data-stu-id="aa216-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="aa216-112">**dwCategory**</span><span class="sxs-lookup"><span data-stu-id="aa216-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="aa216-113">Catégorie de chaîne à afficher.</span><span class="sxs-lookup"><span data-stu-id="aa216-113">Category of string to be displayed.</span></span> <span data-ttu-id="aa216-114">Consultez [**\_ catégorie d' \_ état \_ de licence DRM**](drmdrm-license-state-category.md) pour connaître les valeurs possibles et leur signification.</span><span class="sxs-lookup"><span data-stu-id="aa216-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drmdrm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="aa216-115">**dwNumCounts**</span><span class="sxs-lookup"><span data-stu-id="aa216-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="aa216-116">Nombre d’éléments fournis dans **dwCount**.</span><span class="sxs-lookup"><span data-stu-id="aa216-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="aa216-117">Cette valeur est généralement 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="aa216-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="aa216-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="aa216-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="aa216-119">Tableau de 0 ou de 1 ou plusieurs valeurs **DWORD** qui représentent le nombre de fois que l’action spécifiée dans **dwCategory** peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="aa216-119">An array of 0 or 1 or more **DWORD** values that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="aa216-120">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="aa216-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="aa216-121">**dwNumDates**</span><span class="sxs-lookup"><span data-stu-id="aa216-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="aa216-122">Nombre d’éléments fournis dans **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="aa216-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="aa216-123">En règle générale, il n’est pas possible d’utiliser plus de deux dates, par exemple avec une licence valide à partir d’une date jusqu’à une autre date.</span><span class="sxs-lookup"><span data-stu-id="aa216-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="aa216-124">**DATEHEURE \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="aa216-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="aa216-125">Tableau d’une ou de plusieurs structures **fileTime** représentant une ou plusieurs dates dans la licence.</span><span class="sxs-lookup"><span data-stu-id="aa216-125">An array of one or more **FILETIME** structures representing one or more dates in the license.</span></span> <span data-ttu-id="aa216-126">La signification d’une date particulière dépend de la valeur de **dwCategory**.</span><span class="sxs-lookup"><span data-stu-id="aa216-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="aa216-127">**dwVague**</span><span class="sxs-lookup"><span data-stu-id="aa216-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="aa216-128">Zéro, un ou plusieurs des indicateurs suivants combinés avec une **opération or** au niveau du bit :</span><span class="sxs-lookup"><span data-stu-id="aa216-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="aa216-129">Indicateur</span><span class="sxs-lookup"><span data-stu-id="aa216-129">Flag</span></span>                                    | <span data-ttu-id="aa216-130">Description</span><span class="sxs-lookup"><span data-stu-id="aa216-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa216-131">données d’état de la \_ licence DRM \_ \_ \_ vague</span><span class="sxs-lookup"><span data-stu-id="aa216-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="aa216-132">Si cette valeur est définie, il peut y avoir plus de licences qui s’appliquent au contenu.</span><span class="sxs-lookup"><span data-stu-id="aa216-132">If set, there may be more licenses that apply to the content.</span></span> <span data-ttu-id="aa216-133">La seule façon d’être certain des licences individuelles qui s’appliquent à un ID de clé donné consiste à énumérer les licences.</span><span class="sxs-lookup"><span data-stu-id="aa216-133">The only way to be certain about the individual licenses that apply to a given key ID is to enumerate the licenses.</span></span> <span data-ttu-id="aa216-134">Pour ce faire, appelez [**IWMDRMLicenseManagement :: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), en passant l’ID de clé comme paramètre bstrKID.</span><span class="sxs-lookup"><span data-stu-id="aa216-134">To do this, call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing the key ID as the bstrKID parameter.</span></span> <span data-ttu-id="aa216-135">Utilisez ensuite l’interface IWMDRMLicense extraite pour examiner les licences.</span><span class="sxs-lookup"><span data-stu-id="aa216-135">Then use the retrieved IWMDRMLicense interface to examine the licenses.</span></span> |
| <span data-ttu-id="aa216-136">\_OPL de données d’état de licence DRM \_ \_ \_ \_ présent</span><span class="sxs-lookup"><span data-stu-id="aa216-136">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="aa216-137">Si cette option est définie, la licence comprend des niveaux de protection de sortie (OPLs) qui doivent être récupérés et vérifiés par rapport à la destination de la sortie de votre application.</span><span class="sxs-lookup"><span data-stu-id="aa216-137">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="aa216-138">données d’état de la \_ licence DRM \_ \_ \_ \_ présentes</span><span class="sxs-lookup"><span data-stu-id="aa216-138">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="aa216-139">S’il est défini, le contenu doit être remis à l’aide d’un chemin d’accès audio sécurisé (SAP).</span><span class="sxs-lookup"><span data-stu-id="aa216-139">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa216-140">Notes</span><span class="sxs-lookup"><span data-stu-id="aa216-140">Remarks</span></span>

<span data-ttu-id="aa216-141">Cette structure est récupérée en appelant **IWMDRMLicenseQuery :: QueryLicenseState**.</span><span class="sxs-lookup"><span data-stu-id="aa216-141">This structure is retrieved by calling **IWMDRMLicenseQuery::QueryLicenseState**.</span></span>

<span data-ttu-id="aa216-142">Si **dwCategory** est **le \_ \_ \_ nombre d’États de licence WM DRM \_ \_ de \_ jusqu'** à, le tableau **DateTime** contient généralement deux dates : une date « de » et une date « jusqu’au ».</span><span class="sxs-lookup"><span data-stu-id="aa216-142">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**, then the **datetime** array will typically contain two dates: a "from" date and an "until" date.</span></span> <span data-ttu-id="aa216-143">Il est également possible de spécifier deux paires de dates pour créer des licences plus complexes.</span><span class="sxs-lookup"><span data-stu-id="aa216-143">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="aa216-144">Les éléments du tableau **dwCount** correspondent aux dates ou aux plages de dates spécifiées dans le tableau **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="aa216-144">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="aa216-145">Si **dwCategory** est **le \_ \_ \_ nombre d’États de licence WM DRM \_ \_ de \_ until et que** **DateTime** contient une paire de dates, **dwCount** contient un élément.</span><span class="sxs-lookup"><span data-stu-id="aa216-145">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="aa216-146">Si **DateTime** contient deux paires de dates (quatre éléments), **dwCount** doit contenir deux éléments, un pour chaque paire de dates.</span><span class="sxs-lookup"><span data-stu-id="aa216-146">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="aa216-147">Dans certains cas, les utilisateurs ont peut-être émis plus d’une licence pour un fichier.</span><span class="sxs-lookup"><span data-stu-id="aa216-147">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="aa216-148">Par exemple, ils peuvent avoir acquis une licence qui a autorisé cinq lectures jusqu’à la fin du mois et acquis ultérieurement une deuxième licence pour des droits illimités.</span><span class="sxs-lookup"><span data-stu-id="aa216-148">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="aa216-149">Dans ce cas, l’indicateur de \_ données de l' \_ État de licence DRM \_ \_ est défini dans **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) et le composant DRM utilise un algorithme pour déterminer l’ensemble de droits le plus probable qui ont été appliqués.</span><span class="sxs-lookup"><span data-stu-id="aa216-149">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="aa216-150">Lorsqu’une licence expire, le composant DRM examine les licences restantes, et ainsi de suite jusqu’à ce que toutes les licences aient expiré.</span><span class="sxs-lookup"><span data-stu-id="aa216-150">When one license expires, the DRM component will examine the remaining licenses, and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa216-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa216-151">Requirements</span></span>



| <span data-ttu-id="aa216-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa216-152">Requirement</span></span> | <span data-ttu-id="aa216-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa216-153">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa216-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa216-154">Header</span></span><br/> | <dl> <span data-ttu-id="aa216-155"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa216-155"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa216-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa216-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa216-157">**Structures**</span><span class="sxs-lookup"><span data-stu-id="aa216-157">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





