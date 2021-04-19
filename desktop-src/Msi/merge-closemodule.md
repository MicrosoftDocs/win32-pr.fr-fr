---
description: La méthode CloseModule de l’objet Merge (fusion) ferme le module de fusion Windows Installer actuellement ouvert.
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: Merge. CloseModule, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseModule
- IMsmMerge.CloseModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8688ae06cedca1e3b75290f7831f7d3539e3ec21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544414"
---
# <a name="mergeclosemodule-method"></a><span data-ttu-id="31bc7-103">Merge. CloseModule, méthode</span><span class="sxs-lookup"><span data-stu-id="31bc7-103">Merge.CloseModule method</span></span>

<span data-ttu-id="31bc7-104">La méthode **CloseModule** de l’objet [**Merge (fusion**](merge-object.md) ) ferme le module de fusion Windows Installer actuellement ouvert.</span><span class="sxs-lookup"><span data-stu-id="31bc7-104">The **CloseModule** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer merge module.</span></span>

## <a name="syntax"></a><span data-ttu-id="31bc7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31bc7-105">Syntax</span></span>


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a><span data-ttu-id="31bc7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31bc7-106">Parameters</span></span>

<span data-ttu-id="31bc7-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="31bc7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31bc7-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31bc7-108">Return value</span></span>

<span data-ttu-id="31bc7-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="31bc7-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31bc7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="31bc7-110">Remarks</span></span>

<span data-ttu-id="31bc7-111">La fermeture d’un module de fusion n’affecte pas les erreurs qui n’ont pas été récupérées.</span><span class="sxs-lookup"><span data-stu-id="31bc7-111">Closing a merge module will not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="31bc7-112">C++</span><span class="sxs-lookup"><span data-stu-id="31bc7-112">C++</span></span>

<span data-ttu-id="31bc7-113">Consultez fonction [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) .</span><span class="sxs-lookup"><span data-stu-id="31bc7-113">See [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="31bc7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31bc7-114">Requirements</span></span>



| <span data-ttu-id="31bc7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31bc7-115">Requirement</span></span> | <span data-ttu-id="31bc7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="31bc7-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31bc7-117">Version</span><span class="sxs-lookup"><span data-stu-id="31bc7-117">Version</span></span><br/> | <span data-ttu-id="31bc7-118">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="31bc7-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="31bc7-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="31bc7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="31bc7-120"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="31bc7-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="31bc7-121">DLL</span><span class="sxs-lookup"><span data-stu-id="31bc7-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="31bc7-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31bc7-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
