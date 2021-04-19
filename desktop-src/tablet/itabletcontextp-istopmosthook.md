---
description: Indique si le contexte de tablette se trouve dans le hook le plus élevé.
ms.assetid: b4aaee47-3d77-49cd-9600-f41764b9fb85
title: 'ITabletContextP :: IsTopMostHook, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.IsTopMostHook
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: f62de678085bda723bb13a721d75c349d395787a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530230"
---
# <a name="itabletcontextpistopmosthook-method"></a><span data-ttu-id="f4a98-103">ITabletContextP :: IsTopMostHook, méthode</span><span class="sxs-lookup"><span data-stu-id="f4a98-103">ITabletContextP::IsTopMostHook method</span></span>

<span data-ttu-id="f4a98-104">Indique si le contexte de tablette se trouve dans le hook le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="f4a98-104">Indicates if the tablet context is in the top most hook.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4a98-105">Syntax</span></span>


```C++
HRESULT IsTopMostHook();
```



## <a name="parameters"></a><span data-ttu-id="f4a98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4a98-106">Parameters</span></span>

<span data-ttu-id="f4a98-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f4a98-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4a98-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4a98-108">Return value</span></span>

<span data-ttu-id="f4a98-109">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f4a98-109">This method can return one of these values.</span></span>



| <span data-ttu-id="f4a98-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f4a98-110">Return code</span></span>                                                                            | <span data-ttu-id="f4a98-111">Description</span><span class="sxs-lookup"><span data-stu-id="f4a98-111">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="f4a98-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f4a98-112"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="f4a98-113">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="f4a98-113">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="f4a98-114"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="f4a98-114"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="f4a98-115">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="f4a98-115">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f4a98-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4a98-116">Requirements</span></span>



| <span data-ttu-id="f4a98-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4a98-117">Requirement</span></span> | <span data-ttu-id="f4a98-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4a98-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a98-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4a98-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f4a98-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4a98-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f4a98-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4a98-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f4a98-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4a98-122">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f4a98-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f4a98-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4a98-124"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f4a98-124"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4a98-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4a98-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a98-126">**Interface ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="f4a98-126">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




