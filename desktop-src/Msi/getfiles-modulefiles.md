---
description: La propriété ModuleFiles de l’objet GetFiles retourne toutes les clés primaires de la table de fichiers pour le module actuellement ouvert.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: GetFiles. ModuleFiles, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543935"
---
# <a name="getfilesmodulefiles-property"></a><span data-ttu-id="c690d-103">GetFiles. ModuleFiles, propriété</span><span class="sxs-lookup"><span data-stu-id="c690d-103">GetFiles.ModuleFiles property</span></span>

<span data-ttu-id="c690d-104">La propriété **ModuleFiles** de l’objet [**GetFiles**](getfiles-object.md) retourne toutes les clés primaires de la [table de fichiers](file-table.md) pour le module actuellement ouvert.</span><span class="sxs-lookup"><span data-stu-id="c690d-104">**ModuleFiles** property of the [**GetFiles**](getfiles-object.md) object returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span> <span data-ttu-id="c690d-105">Les clés primaires sont retournées sous la forme d’une collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="c690d-105">The primary keys are returned as a collection of strings.</span></span> <span data-ttu-id="c690d-106">Le module doit être ouvert par un appel à la méthode [**OpenModule**](merge-openmodule.md) de l' [objet Merge](merge-object.md) avant d’appeler **ModuleFiles**.</span><span class="sxs-lookup"><span data-stu-id="c690d-106">The module must be opened by a call to the [**OpenModule**](merge-openmodule.md) method of the [Merge object](merge-object.md) before calling **ModuleFiles**.</span></span>

<span data-ttu-id="c690d-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c690d-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c690d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c690d-108">Syntax</span></span>


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a><span data-ttu-id="c690d-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c690d-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c690d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c690d-110">Remarks</span></span>

<span data-ttu-id="c690d-111">Notez que l’ordre des fichiers figurant dans la collection ne peut pas être dans le même ordre que celui indiqué dans la table file.</span><span class="sxs-lookup"><span data-stu-id="c690d-111">Note that order of the files listed in the collection may not be in the same sequence as listed in the File table.</span></span>

<span data-ttu-id="c690d-112">Si le module n’a pas de table de fichiers ou ne contient pas de fichiers dans la langue particulière, ModuleFiles retourne une collection de chaînes vide.</span><span class="sxs-lookup"><span data-stu-id="c690d-112">If the module has no File table, or contains no files in the particular language, ModuleFiles returns an empty collection of strings.</span></span>

### <a name="c"></a><span data-ttu-id="c690d-113">C++</span><span class="sxs-lookup"><span data-stu-id="c690d-113">C++</span></span>

<span data-ttu-id="c690d-114">Consultez la fonction [**obtenir \_ ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) .</span><span class="sxs-lookup"><span data-stu-id="c690d-114">See [**get\_ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c690d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c690d-115">Requirements</span></span>



| <span data-ttu-id="c690d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c690d-116">Requirement</span></span> | <span data-ttu-id="c690d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c690d-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c690d-118">Version</span><span class="sxs-lookup"><span data-stu-id="c690d-118">Version</span></span><br/> | <span data-ttu-id="c690d-119">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c690d-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="c690d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c690d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c690d-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="c690d-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="c690d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c690d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="c690d-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c690d-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
