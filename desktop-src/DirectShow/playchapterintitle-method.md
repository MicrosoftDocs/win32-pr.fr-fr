---
description: La méthode PlayChapterInTitle lit le chapitre spécifié dans le titre spécifié.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Méthode PlayChapterInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845677"
---
# <a name="playchapterintitle-method"></a><span data-ttu-id="14a50-103">Méthode PlayChapterInTitle</span><span class="sxs-lookup"><span data-stu-id="14a50-103">PlayChapterInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="14a50-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="14a50-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="14a50-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="14a50-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="14a50-106">La `PlayChapterInTitle` méthode lit le chapitre spécifié dans le titre spécifié.</span><span class="sxs-lookup"><span data-stu-id="14a50-106">The `PlayChapterInTitle` method plays the specified chapter in the specified title.</span></span>

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a><span data-ttu-id="14a50-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14a50-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14a50-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="14a50-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="14a50-109">Spécifie le titre sous la forme d’une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="14a50-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="14a50-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="14a50-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="14a50-111">Spécifie le chapitre sous la forme d’une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="14a50-111">Specifies the chapter as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14a50-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="14a50-112">Return Value</span></span>

<span data-ttu-id="14a50-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="14a50-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14a50-114">Notes</span><span class="sxs-lookup"><span data-stu-id="14a50-114">Remarks</span></span>

<span data-ttu-id="14a50-115">Cette méthode démarre la lecture au chapitre spécifié, puis continue la lecture indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="14a50-115">This method starts playback at the specified chapter and then continues playing indefinitely.</span></span> <span data-ttu-id="14a50-116">Si vous souhaitez lire uniquement un chapitre particulier, utilisez [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="14a50-116">If you want to play only a particular chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

 

 



