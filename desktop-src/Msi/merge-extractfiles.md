---
description: La méthode ExtractFiles de l’objet Merge extrait le fichier. cab incorporé d’un module, puis écrit ces fichiers dans le répertoire de destination.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Merge. ExtractFiles, méthode (Advpub. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540269"
---
# <a name="mergeextractfiles-method"></a><span data-ttu-id="78af6-103">Merge. ExtractFiles, méthode</span><span class="sxs-lookup"><span data-stu-id="78af6-103">Merge.ExtractFiles method</span></span>

<span data-ttu-id="78af6-104">La méthode **ExtractFiles** de l’objet [**Merge**](merge-object.md) extrait le fichier. cab incorporé d’un module, puis écrit ces fichiers dans le répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="78af6-104">The **ExtractFiles** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="78af6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78af6-105">Syntax</span></span>


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="78af6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78af6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78af6-107">*Chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="78af6-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="78af6-108">Le répertoire de destination complet.</span><span class="sxs-lookup"><span data-stu-id="78af6-108">The fully qualified destination directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78af6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78af6-109">Return value</span></span>

<span data-ttu-id="78af6-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="78af6-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78af6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="78af6-111">Remarks</span></span>

<span data-ttu-id="78af6-112">Tous les fichiers du répertoire de destination portant le même nom sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="78af6-112">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="78af6-113">Le chemin d’accès est créé s’il n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="78af6-113">The path is created if it does not already exist.</span></span>

<span data-ttu-id="78af6-114">**ExtractFiles** extrait toujours les fichiers en utilisant des noms de fichiers courts pour le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="78af6-114">**ExtractFiles** always extracts files using short file names for the path.</span></span> <span data-ttu-id="78af6-115">Pour utiliser des noms de fichiers longs pour le chemin d’accès, utilisez la [**méthode ExtractFilesEx**](merge-extractfilesex.md).</span><span class="sxs-lookup"><span data-stu-id="78af6-115">To use long file names for the path, use the [**ExtractFilesEx method**](merge-extractfilesex.md).</span></span>

### <a name="c"></a><span data-ttu-id="78af6-116">C++</span><span class="sxs-lookup"><span data-stu-id="78af6-116">C++</span></span>

<span data-ttu-id="78af6-117">Consultez fonction [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) .</span><span class="sxs-lookup"><span data-stu-id="78af6-117">See [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="78af6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78af6-118">Requirements</span></span>



| <span data-ttu-id="78af6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78af6-119">Requirement</span></span> | <span data-ttu-id="78af6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="78af6-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78af6-121">Version</span><span class="sxs-lookup"><span data-stu-id="78af6-121">Version</span></span><br/> | <span data-ttu-id="78af6-122">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="78af6-122">Mergemod.dll 1.0 or later</span></span><br/>                                                                     |
| <span data-ttu-id="78af6-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="78af6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="78af6-124"><dt>Advpub. h (inclure Mergemod. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78af6-124"><dt>Advpub.h (include Mergemod.h)</dt></span></span> </dl> |
| <span data-ttu-id="78af6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="78af6-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="78af6-126"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78af6-126"><dt>Mergemod.dll</dt></span></span> </dl>                  |



 

 
