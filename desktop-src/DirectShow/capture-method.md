---
description: La méthode de capture capture une image continue à partir de l’image vidéo lorsque l’objet MSWebDVD est en mode sans fenêtre.
ms.assetid: 704e64ef-3593-403c-8ecf-625fb4983882
title: Capture, méthode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db16bbc6ef50de303dbcdac66bd066861bb5811
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108595"
---
# <a name="capture-method"></a><span data-ttu-id="f5093-103">Capture, méthode</span><span class="sxs-lookup"><span data-stu-id="f5093-103">Capture Method</span></span>

> [!Note]  
> <span data-ttu-id="f5093-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f5093-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f5093-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f5093-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f5093-106">La `Capture` méthode capture une image continue à partir de l’image vidéo lorsque l’objet mswebdvd est en mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f5093-106">The `Capture` method captures a still image from the video frame when the MSWebDVD object is in windowless mode.</span></span>

``` syntax
MSWebDVD.Capture()
```

## <a name="remarks"></a><span data-ttu-id="f5093-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f5093-107">Remarks</span></span>

<span data-ttu-id="f5093-108">Cette méthode capture le frame actuel à partir de l’image DVD-Video et le colle dans une fenêtre à partir de laquelle l’utilisateur peut enregistrer ou modifier l’image.</span><span class="sxs-lookup"><span data-stu-id="f5093-108">This method captures the current frame from the DVD-Video image and pastes it into a window from which the user can save or edit the image.</span></span> <span data-ttu-id="f5093-109">L’objet MSWebDVD doit être en mode sans fenêtre pour que cette méthode aboutisse.</span><span class="sxs-lookup"><span data-stu-id="f5093-109">The MSWebDVD object must be in windowless mode for this method to succeed.</span></span>

 

 



