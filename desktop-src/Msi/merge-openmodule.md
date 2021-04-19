---
description: La méthode OpenModule de l’objet Merge ouvre un module de fusion Windows Installer en mode lecture seule. Vous devez ouvrir un module avant de pouvoir le fusionner avec une base de données d’installation.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Merge. OpenModule, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534934"
---
# <a name="mergeopenmodule-method"></a><span data-ttu-id="5f2c4-104">Merge. OpenModule, méthode</span><span class="sxs-lookup"><span data-stu-id="5f2c4-104">Merge.OpenModule method</span></span>

<span data-ttu-id="5f2c4-105">La méthode **OpenModule** de l’objet [**Merge**](merge-object.md) ouvre un module de fusion Windows Installer en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-105">The **OpenModule** method of the [**Merge**](merge-object.md) object opens a Windows Installer merge module in read-only mode.</span></span> <span data-ttu-id="5f2c4-106">Vous devez ouvrir un module avant de pouvoir le fusionner avec une base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-106">A module must be opened before it can be merged with an installation database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f2c4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f2c4-107">Syntax</span></span>


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="5f2c4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f2c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f2c4-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="5f2c4-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="5f2c4-110">Nom de fichier complet pointant vers un module de fusion.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-110">Fully qualified file name pointing to a merge module.</span></span>

</dd> <dt>

<span data-ttu-id="5f2c4-111">*Langage*</span><span class="sxs-lookup"><span data-stu-id="5f2c4-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="5f2c4-112">Identificateur de langue valide (LANGID).</span><span class="sxs-lookup"><span data-stu-id="5f2c4-112">A valid language identifier (LANGID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f2c4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f2c4-113">Return value</span></span>

<span data-ttu-id="5f2c4-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f2c4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5f2c4-115">Remarks</span></span>

<span data-ttu-id="5f2c4-116">Cette fonction ouvre le module de fusion en mode lecture seule et exclut l’écriture d’autres programmes dans le module de fusion jusqu’à ce que la méthode [**CloseModule**](merge-closemodule.md) soit appelée.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-116">This function opens the merge module in read-only mode and excludes other programs from writing to the merge module until the [**CloseModule**](merge-closemodule.md) method is called.</span></span>

<span data-ttu-id="5f2c4-117">Le programme d’installation tente d’ouvrir le module dans la langue spécifiée par la *langue*, ou dans une langue plus générale.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-117">The installer attempts to open the module in the language specified by *Language*, or a more general language.</span></span> <span data-ttu-id="5f2c4-118">Par exemple, si la *langue* est spécifiée comme 1033, un module avec une langue par défaut de 1033, 9 ou 0 peut être ouvert dans sa langue par défaut.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-118">For example, if *Language* is specified as 1033, a module with a default language of 1033, 9, or 0 can be opened in its default language.</span></span> <span data-ttu-id="5f2c4-119">La valeur de *langue* 9 ouvre les modules dont la langue par défaut est 9 ou 0.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-119">A *Language* value of 9 opens modules with a default language of 9 or 0.</span></span> <span data-ttu-id="5f2c4-120">Si la langue par défaut du module ne répond pas aux exigences spécifiées, une tentative est faite pour transformer le module en la langue demandée.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-120">If the default language of the module does not meet the specified requirements, an attempt is made to transform the module to the requested language.</span></span> <span data-ttu-id="5f2c4-121">En cas d’échec, le module est transformé en langages de plus en plus généraux, tout comme le langage neutre.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-121">If that fails, the module is transformed to increasingly general languages, all the way to language neutral.</span></span> <span data-ttu-id="5f2c4-122">Si aucune des transformations ne réussit, le module ne parvient pas à s’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-122">If none of the transforms succeed, the module fails to open.</span></span> <span data-ttu-id="5f2c4-123">Dans ce cas, une erreur est ajoutée à la liste d’erreurs de type msmErrorLanguageUnsupported.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-123">In this case, an error is added to the error list of type msmErrorLanguageUnsupported.</span></span> <span data-ttu-id="5f2c4-124">En cas d’erreur lors de la transformation du module en langue souhaitée, une erreur est ajoutée à la liste d’erreurs de type msmErrorLanguageFailed.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-124">If there is an error transforming the module to the desired language, an error is added to the error list of type msmErrorLanguageFailed.</span></span> <span data-ttu-id="5f2c4-125">Pour plus d’informations, consultez la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5f2c4-125">For details, see the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span> <span data-ttu-id="5f2c4-126">L’ouverture d’un module de fusion efface toutes les erreurs qui n’ont pas encore été récupérées.</span><span class="sxs-lookup"><span data-stu-id="5f2c4-126">Opening a merge module clears any errors that have not already been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="5f2c4-127">C++</span><span class="sxs-lookup"><span data-stu-id="5f2c4-127">C++</span></span>

<span data-ttu-id="5f2c4-128">Consultez fonction [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) .</span><span class="sxs-lookup"><span data-stu-id="5f2c4-128">See [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f2c4-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f2c4-129">Requirements</span></span>



| <span data-ttu-id="5f2c4-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f2c4-130">Requirement</span></span> | <span data-ttu-id="5f2c4-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f2c4-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2c4-132">Version</span><span class="sxs-lookup"><span data-stu-id="5f2c4-132">Version</span></span><br/> | <span data-ttu-id="5f2c4-133">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5f2c4-133">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5f2c4-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f2c4-134">Header</span></span><br/>  | <dl> <span data-ttu-id="5f2c4-135"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f2c4-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f2c4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5f2c4-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="5f2c4-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f2c4-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
