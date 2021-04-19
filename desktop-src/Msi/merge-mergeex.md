---
description: La méthode MergeEx de l’objet Merge équivaut à la fonction Merge, à ceci près qu’elle accepte un argument supplémentaire.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Merge. MergeEx, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535922"
---
# <a name="mergemergeex-method"></a><span data-ttu-id="14ee6-103">Merge. MergeEx, méthode</span><span class="sxs-lookup"><span data-stu-id="14ee6-103">Merge.MergeEx method</span></span>

<span data-ttu-id="14ee6-104">La méthode **MergeEx** de l’objet [**Merge**](merge-object.md) équivaut à la fonction [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , à ceci près qu’elle accepte un argument supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="14ee6-104">The **MergeEx** method of the [**Merge**](merge-object.md) object is equivalent to the [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function, except that it takes an extra argument.</span></span> <span data-ttu-id="14ee6-105">L’argument *pConfiguration* est une interface implémentée par le client.</span><span class="sxs-lookup"><span data-stu-id="14ee6-105">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="14ee6-106">L’argument peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="14ee6-106">The argument may be null.</span></span> <span data-ttu-id="14ee6-107">La présence de cet argument indique que le client peut prendre en charge la fonctionnalité de configuration, mais n’impose pas au client de fournir des données de configuration pour un élément configurable spécifique.</span><span class="sxs-lookup"><span data-stu-id="14ee6-107">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

<span data-ttu-id="14ee6-108">La méthode [**Merge**](merge-merge.md) exécute une fusion de la base de données active et du module actuel.</span><span class="sxs-lookup"><span data-stu-id="14ee6-108">The [**Merge**](merge-merge.md) method executes a merge of the current database and current module.</span></span> <span data-ttu-id="14ee6-109">La fusion attache les composants du module à la fonctionnalité identifiée par la *fonctionnalité*.</span><span class="sxs-lookup"><span data-stu-id="14ee6-109">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="14ee6-110">La racine de l’arborescence de répertoires du module est redirigée vers l’emplacement donné par *RedirectDir*.</span><span class="sxs-lookup"><span data-stu-id="14ee6-110">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ee6-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14ee6-111">Syntax</span></span>


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
)
```



## <a name="parameters"></a><span data-ttu-id="14ee6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14ee6-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14ee6-113">*Fonctionnalité*</span><span class="sxs-lookup"><span data-stu-id="14ee6-113">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="14ee6-114">Nom d’une fonctionnalité dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="14ee6-114">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="14ee6-115">*RedirectDir*</span><span class="sxs-lookup"><span data-stu-id="14ee6-115">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="14ee6-116">Clé d’une entrée dans la [table des répertoires](directory-table.md) de la base de données.</span><span class="sxs-lookup"><span data-stu-id="14ee6-116">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="14ee6-117">Ce paramètre peut avoir la valeur null ou être une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="14ee6-117">This parameter may be null or an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="14ee6-118">*pConfiguration*</span><span class="sxs-lookup"><span data-stu-id="14ee6-118">*pConfiguration*</span></span> 
</dt> <dd>

<span data-ttu-id="14ee6-119">L’argument *pConfiguration* est une interface implémentée par le client.</span><span class="sxs-lookup"><span data-stu-id="14ee6-119">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="14ee6-120">L’argument peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="14ee6-120">The argument may be null.</span></span> <span data-ttu-id="14ee6-121">La présence de cet argument indique que le client peut prendre en charge la fonctionnalité de configuration, mais n’impose pas au client de fournir des données de configuration pour un élément configurable spécifique.</span><span class="sxs-lookup"><span data-stu-id="14ee6-121">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14ee6-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14ee6-122">Return value</span></span>

<span data-ttu-id="14ee6-123">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="14ee6-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14ee6-124">Notes</span><span class="sxs-lookup"><span data-stu-id="14ee6-124">Remarks</span></span>

<span data-ttu-id="14ee6-125">Une fois la fusion terminée, les composants du module sont attachés à la fonctionnalité identifiée par la *fonctionnalité*.</span><span class="sxs-lookup"><span data-stu-id="14ee6-125">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="14ee6-126">Cette fonctionnalité n’est pas créée et doit être une fonctionnalité existante.</span><span class="sxs-lookup"><span data-stu-id="14ee6-126">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="14ee6-127">Le module peut être attaché à des fonctionnalités supplémentaires à l’aide de la méthode [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="14ee6-127">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span>

<span data-ttu-id="14ee6-128">Les modifications apportées à la base de données sont enregistrées si et seulement si la méthode [**FermerBase**](merge-closedatabase.md) est appelée avec *BCommit* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="14ee6-128">Changes made to the database are saved if and only if the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="14ee6-129">Si des conflits de fusion se produisent, y compris des exclusions, ils sont placés dans l’énumérateur d’erreurs pour une récupération ultérieure, mais n’entraînent pas l’échec de la fusion.</span><span class="sxs-lookup"><span data-stu-id="14ee6-129">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="14ee6-130">Les erreurs peuvent être récupérées par le biais de la propriété [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="14ee6-130">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="14ee6-131">Les erreurs et les messages d’information sont publiés dans le fichier journal actuel.</span><span class="sxs-lookup"><span data-stu-id="14ee6-131">Errors and informational messages are posted to the current log file.</span></span>

<span data-ttu-id="14ee6-132">Lorsque la fusion échoue en raison d’une configuration de module incorrecte, la fonction [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) retourne E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="14ee6-132">When the merge fails because of an incorrect module configuration the [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function returns E\_FAIL.</span></span> <span data-ttu-id="14ee6-133">Cela comprend les erreurs msmErrorType suivantes : **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem** et **msmErrorDataRequestFailed**.</span><span class="sxs-lookup"><span data-stu-id="14ee6-133">This includes these msmErrorType errors: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem**, and **msmErrorDataRequestFailed**.</span></span> <span data-ttu-id="14ee6-134">Ces erreurs provoquent l’arrêt immédiat de la fusion lorsque l’erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="14ee6-134">These errors cause the merge to stop immediately when the error is encountered.</span></span> <span data-ttu-id="14ee6-135">L’objet d’erreur est toujours ajouté à l’énumérateur lorsque **MergeEx** retourne E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="14ee6-135">The error object is still added to the enumerator when **MergeEx** returns E\_FAIL.</span></span> <span data-ttu-id="14ee6-136">Pour plus d’informations sur les erreurs msmErrorType, consultez [**obtenir le \_ type, fonction (objet d’erreur)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span><span class="sxs-lookup"><span data-stu-id="14ee6-136">For more information about msmErrorType errors, see [**get\_Type Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span></span> <span data-ttu-id="14ee6-137">Toutes les autres erreurs  provoquent le renvoi de S \_ false par MergeEx et la poursuite de la fusion.</span><span class="sxs-lookup"><span data-stu-id="14ee6-137">All other errors cause **MergeEx** to return S\_FALSE and cause the merge to continue.</span></span>

### <a name="c"></a><span data-ttu-id="14ee6-138">C++</span><span class="sxs-lookup"><span data-stu-id="14ee6-138">C++</span></span>

<span data-ttu-id="14ee6-139">Consultez fonction [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) .</span><span class="sxs-lookup"><span data-stu-id="14ee6-139">See [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="14ee6-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14ee6-140">Requirements</span></span>



| <span data-ttu-id="14ee6-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14ee6-141">Requirement</span></span> | <span data-ttu-id="14ee6-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="14ee6-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14ee6-143">Version</span><span class="sxs-lookup"><span data-stu-id="14ee6-143">Version</span></span><br/> | <span data-ttu-id="14ee6-144">Mergemod.dll 2,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="14ee6-144">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="14ee6-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="14ee6-145">Header</span></span><br/>  | <dl> <span data-ttu-id="14ee6-146"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="14ee6-146"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="14ee6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="14ee6-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="14ee6-148"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14ee6-148"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
