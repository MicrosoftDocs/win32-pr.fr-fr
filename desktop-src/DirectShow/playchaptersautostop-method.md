---
description: La méthode PlayChaptersAutoStop démarre la lecture au chapitre spécifié dans le titre spécifié et pour le nombre de chapitres spécifié.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Méthode PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200724"
---
# <a name="playchaptersautostop-method"></a><span data-ttu-id="5bb02-103">Méthode PlayChaptersAutoStop</span><span class="sxs-lookup"><span data-stu-id="5bb02-103">PlayChaptersAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="5bb02-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5bb02-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5bb02-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5bb02-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5bb02-106">La `PlayChaptersAutoStop` méthode démarre la lecture au chapitre spécifié dans le titre spécifié et pour le nombre de chapitres spécifié.</span><span class="sxs-lookup"><span data-stu-id="5bb02-106">The `PlayChaptersAutoStop` method starts playback at the specified chapter in the specified title and for the number of chapters specified.</span></span>

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a><span data-ttu-id="5bb02-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bb02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bb02-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="5bb02-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="5bb02-109">Spécifie le titre sous la forme d’une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="5bb02-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="5bb02-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="5bb02-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="5bb02-111">Spécifie le chapitre de démarrage sous la forme d’une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="5bb02-111">Specifies the start chapter as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="5bb02-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span><span class="sxs-lookup"><span data-stu-id="5bb02-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span></span>
</dt> <dd>

<span data-ttu-id="5bb02-113">Spécifie le nombre de chapitres à lire sous la forme d’une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="5bb02-113">Specifies the number of chapters to play as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bb02-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5bb02-114">Return Value</span></span>

<span data-ttu-id="5bb02-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5bb02-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bb02-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5bb02-116">Remarks</span></span>

<span data-ttu-id="5bb02-117">Lorsque le dernier chapitre a joué, cette méthode entraîne l’envoi à l’application d’une notification d’événement [**\_ \_ \_ autostop du chapitre de DVD ce**](ec-dvd-chapter-autostop.md) .</span><span class="sxs-lookup"><span data-stu-id="5bb02-117">When the last chapter has played, this method causes an [**EC\_DVD\_CHAPTER\_AUTOSTOP**](ec-dvd-chapter-autostop.md) event notification to be sent to the application.</span></span>

 

 



