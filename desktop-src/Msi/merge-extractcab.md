---
description: La méthode ExtractCAB de l’objet Merge extrait le fichier. cab incorporé d’un module et l’enregistre dans le fichier spécifié. Le programme d’installation crée ce fichier s’il n’existe pas déjà et est remplacé s’il existe.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Merge. ExtractCAB, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539559"
---
# <a name="mergeextractcab-method"></a><span data-ttu-id="c55b3-104">Merge. ExtractCAB, méthode</span><span class="sxs-lookup"><span data-stu-id="c55b3-104">Merge.ExtractCAB method</span></span>

<span data-ttu-id="c55b3-105">La méthode **ExtractCAB** de l’objet [**Merge**](merge-object.md) extrait le fichier. cab incorporé d’un module et l’enregistre dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c55b3-105">The **ExtractCAB** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and saves it as the specified file.</span></span> <span data-ttu-id="c55b3-106">Le programme d’installation crée ce fichier s’il n’existe pas déjà et est remplacé s’il existe.</span><span class="sxs-lookup"><span data-stu-id="c55b3-106">The installer creates this file if it does not already exist and overwritten if it does exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55b3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c55b3-107">Syntax</span></span>


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a><span data-ttu-id="c55b3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c55b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c55b3-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="c55b3-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="c55b3-110">Fichier de destination complet.</span><span class="sxs-lookup"><span data-stu-id="c55b3-110">The fully qualified destination file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c55b3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c55b3-111">Return value</span></span>

<span data-ttu-id="c55b3-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c55b3-112">This method does not return a value.</span></span>

## <a name="c"></a><span data-ttu-id="c55b3-113">C++</span><span class="sxs-lookup"><span data-stu-id="c55b3-113">C++</span></span>

<span data-ttu-id="c55b3-114">Consultez fonction [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) .</span><span class="sxs-lookup"><span data-stu-id="c55b3-114">See [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55b3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c55b3-115">Requirements</span></span>



| <span data-ttu-id="c55b3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c55b3-116">Requirement</span></span> | <span data-ttu-id="c55b3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c55b3-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c55b3-118">Version</span><span class="sxs-lookup"><span data-stu-id="c55b3-118">Version</span></span><br/> | <span data-ttu-id="c55b3-119">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c55b3-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="c55b3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c55b3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c55b3-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="c55b3-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="c55b3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c55b3-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="c55b3-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c55b3-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
