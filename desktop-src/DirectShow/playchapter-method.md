---
description: La méthode PlayChapter démarre la lecture à partir du chapitre spécifié dans le titre actuel.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Méthode PlayChapter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514300"
---
# <a name="playchapter-method"></a><span data-ttu-id="979d1-103">Méthode PlayChapter</span><span class="sxs-lookup"><span data-stu-id="979d1-103">PlayChapter Method</span></span>

> [!Note]  
> <span data-ttu-id="979d1-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="979d1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="979d1-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="979d1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="979d1-106">La `PlayChapter` méthode démarre la lecture à partir du chapitre spécifié dans le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="979d1-106">The `PlayChapter` method starts playback from the specified chapter within the current title.</span></span>

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a><span data-ttu-id="979d1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="979d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="979d1-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="979d1-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="979d1-109">Spécifie l’index de chapitre dans le titre actuel sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="979d1-109">Specifies the chapter index in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="979d1-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="979d1-110">Return Value</span></span>

<span data-ttu-id="979d1-111">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="979d1-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="979d1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="979d1-112">Remarks</span></span>

<span data-ttu-id="979d1-113">Quand la fin du chapitre spécifié est atteinte, cette méthode continue de visionner les chapitres suivants, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="979d1-113">When the end of the specified chapter is reached, this method continues playing subsequent chapters, if any exist.</span></span> <span data-ttu-id="979d1-114">Si vous souhaitez lire uniquement un chapitre spécifié, utilisez [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="979d1-114">If you want to play only a specified chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="979d1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="979d1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="979d1-116">**PlayChapterInTitle**</span><span class="sxs-lookup"><span data-stu-id="979d1-116">**PlayChapterInTitle**</span></span>](playchapterintitle-method.md)
</dt> </dl>

 

 



