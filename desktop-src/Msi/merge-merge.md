---
description: La méthode Merge de l’objet Merge exécute une fusion de la base de données active et du module actuel.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Merge. Merge, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525619"
---
# <a name="mergemerge-method"></a><span data-ttu-id="205f8-103">Merge. Merge, méthode</span><span class="sxs-lookup"><span data-stu-id="205f8-103">Merge.Merge method</span></span>

<span data-ttu-id="205f8-104">La méthode **Merge** de l’objet [**Merge**](merge-object.md) exécute une fusion de la base de données active et du module actuel.</span><span class="sxs-lookup"><span data-stu-id="205f8-104">The **Merge** method of the [**Merge**](merge-object.md) object executes a merge of the current database and current module.</span></span> <span data-ttu-id="205f8-105">La fusion attache les composants du module à la fonctionnalité identifiée par la *fonctionnalité*.</span><span class="sxs-lookup"><span data-stu-id="205f8-105">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="205f8-106">La racine de l’arborescence de répertoires du module est redirigée vers l’emplacement donné par *RedirectDir*.</span><span class="sxs-lookup"><span data-stu-id="205f8-106">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

<span data-ttu-id="205f8-107">La méthode **Merge** ne peut être appelée qu’une seule fois pour fusionner une combinaison particulière de fichiers. msi et. msm.</span><span class="sxs-lookup"><span data-stu-id="205f8-107">The **Merge** method can only be called once to merge a particular combination of .msi and .msm files.</span></span>

## <a name="syntax"></a><span data-ttu-id="205f8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="205f8-108">Syntax</span></span>


```JScript
Merge.Merge(
  Feature,
  RedirectDir
)
```



## <a name="parameters"></a><span data-ttu-id="205f8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="205f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="205f8-110">*Fonctionnalité*</span><span class="sxs-lookup"><span data-stu-id="205f8-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="205f8-111">Nom d’une fonctionnalité dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="205f8-111">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="205f8-112">*RedirectDir*</span><span class="sxs-lookup"><span data-stu-id="205f8-112">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="205f8-113">Clé d’une entrée dans la [table des répertoires](directory-table.md) de la base de données.</span><span class="sxs-lookup"><span data-stu-id="205f8-113">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="205f8-114">Ce paramètre peut avoir la valeur null ou être une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="205f8-114">This parameter may be null or an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="205f8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="205f8-115">Return value</span></span>

<span data-ttu-id="205f8-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="205f8-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="205f8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="205f8-117">Remarks</span></span>

<span data-ttu-id="205f8-118">Une fois la fusion terminée, les composants du module sont attachés à la fonctionnalité identifiée par la *fonctionnalité*.</span><span class="sxs-lookup"><span data-stu-id="205f8-118">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="205f8-119">Cette fonctionnalité n’est pas créée et doit être une fonctionnalité existante.</span><span class="sxs-lookup"><span data-stu-id="205f8-119">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="205f8-120">Notez que la méthode **Merge** obtient toutes les références de fonctionnalités dans le module et remplace la référence de fonctionnalité pour toutes les occurrences du GUID null dans la base de données du module.</span><span class="sxs-lookup"><span data-stu-id="205f8-120">Note that the **Merge** method gets all the feature references in the module and substitutes the feature reference for all occurrences of the null GUID in the module database.</span></span> <span data-ttu-id="205f8-121">Pour plus d’informations, consultez [référencement des fonctionnalités dans les modules de fusion](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="205f8-121">For more information, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>

<span data-ttu-id="205f8-122">Le module peut être attaché à des fonctionnalités supplémentaires à l’aide de la méthode [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="205f8-122">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span> <span data-ttu-id="205f8-123">Notez que l’appel de la méthode **Connect** crée uniquement des associations composant-composant.</span><span class="sxs-lookup"><span data-stu-id="205f8-123">Note that calling the **Connect** method only creates feature-component associations.</span></span> <span data-ttu-id="205f8-124">Elle ne modifie pas les lignes qui ont déjà été fusionnées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="205f8-124">It does not modify the rows that have already been merged in to the database.</span></span>

<span data-ttu-id="205f8-125">Les modifications apportées à la base de données sont enregistrées si et seulement si la méthode [**FermerBase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) est appelée avec *BCommit* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="205f8-125">Changes made to the database are saved if and only if the [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="205f8-126">Si des conflits de fusion se produisent, y compris des exclusions, ils sont placés dans l’énumérateur d’erreurs pour une récupération ultérieure, mais n’entraînent pas l’échec de la fusion.</span><span class="sxs-lookup"><span data-stu-id="205f8-126">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="205f8-127">Les erreurs peuvent être récupérées par le biais de la propriété [**Errors**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="205f8-127">Errors may be retrieved through the [**Errors**](error-object.md) property.</span></span> <span data-ttu-id="205f8-128">Les erreurs et les messages d’information sont publiés dans le fichier journal actuel.</span><span class="sxs-lookup"><span data-stu-id="205f8-128">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="205f8-129">C++</span><span class="sxs-lookup"><span data-stu-id="205f8-129">C++</span></span>

<span data-ttu-id="205f8-130">Consultez [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , fonction.</span><span class="sxs-lookup"><span data-stu-id="205f8-130">See [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="205f8-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="205f8-131">Requirements</span></span>



| <span data-ttu-id="205f8-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="205f8-132">Requirement</span></span> | <span data-ttu-id="205f8-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="205f8-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="205f8-134">Version</span><span class="sxs-lookup"><span data-stu-id="205f8-134">Version</span></span><br/> | <span data-ttu-id="205f8-135">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="205f8-135">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="205f8-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="205f8-136">Header</span></span><br/>  | <dl> <span data-ttu-id="205f8-137"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="205f8-137"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="205f8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="205f8-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="205f8-139"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="205f8-139"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
