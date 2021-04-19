---
description: La méthode ExtractFilesEx de l’objet Merge extrait le fichier. cab incorporé d’un module, puis écrit ces fichiers dans le répertoire de destination.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Merge. ExtractFilesEx, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528834"
---
# <a name="mergeextractfilesex-method"></a><span data-ttu-id="5d728-103">Merge. ExtractFilesEx, méthode</span><span class="sxs-lookup"><span data-stu-id="5d728-103">Merge.ExtractFilesEx method</span></span>

<span data-ttu-id="5d728-104">La méthode **ExtractFilesEx** de l’objet [**Merge**](merge-object.md) extrait le fichier. cab incorporé d’un module, puis écrit ces fichiers dans le répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="5d728-104">The **ExtractFilesEx** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d728-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d728-105">Syntax</span></span>


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="5d728-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d728-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d728-107">*Chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="5d728-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="5d728-108">Le répertoire de destination complet.</span><span class="sxs-lookup"><span data-stu-id="5d728-108">The fully qualified destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="5d728-109">*fLongFileNames*</span><span class="sxs-lookup"><span data-stu-id="5d728-109">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="5d728-110">Défini pour spécifier à l’aide de noms de fichiers longs pour les segments de chemin d’accès et les noms de fichiers finaux.</span><span class="sxs-lookup"><span data-stu-id="5d728-110">Set to specify using long file names for path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="5d728-111">*pFilePaths*</span><span class="sxs-lookup"><span data-stu-id="5d728-111">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="5d728-112">Il s’agit d’une liste de chemins d’accès complets pour les fichiers qui ont été extraits avec succès.</span><span class="sxs-lookup"><span data-stu-id="5d728-112">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d728-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d728-113">Return value</span></span>

<span data-ttu-id="5d728-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5d728-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d728-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5d728-115">Remarks</span></span>

<span data-ttu-id="5d728-116">Tous les fichiers du répertoire de destination portant le même nom sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="5d728-116">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="5d728-117">Le chemin d’accès est créé s’il n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="5d728-117">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="5d728-118">C++</span><span class="sxs-lookup"><span data-stu-id="5d728-118">C++</span></span>

<span data-ttu-id="5d728-119">Consultez fonction [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) .</span><span class="sxs-lookup"><span data-stu-id="5d728-119">See [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d728-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d728-120">Requirements</span></span>



| <span data-ttu-id="5d728-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d728-121">Requirement</span></span> | <span data-ttu-id="5d728-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d728-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d728-123">Version</span><span class="sxs-lookup"><span data-stu-id="5d728-123">Version</span></span><br/> | <span data-ttu-id="5d728-124">Mergemod.dll 2,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5d728-124">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5d728-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d728-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5d728-126"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d728-126"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d728-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5d728-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d728-128"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d728-128"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




