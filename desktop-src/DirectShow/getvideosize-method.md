---
description: La méthode GetVideoSize récupère les dimensions natives de la vidéo.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Méthode GetVideoSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106540797"
---
# <a name="getvideosize-method"></a><span data-ttu-id="89ec7-103">Méthode GetVideoSize</span><span class="sxs-lookup"><span data-stu-id="89ec7-103">GetVideoSize Method</span></span>

> [!Note]  
> <span data-ttu-id="89ec7-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="89ec7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="89ec7-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="89ec7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="89ec7-106">La `GetVideoSize` méthode récupère les dimensions natives de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="89ec7-106">The `GetVideoSize` method retrieves the native video dimensions.</span></span>

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a><span data-ttu-id="89ec7-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="89ec7-107">Return Value</span></span>

<span data-ttu-id="89ec7-108">Retourne un objet [DVDRect](dvdrect-object.md) contenant quatre propriétés en lecture/écriture : (en haut à gauche) x ; (en haut à gauche) y, largeur et hauteur.</span><span class="sxs-lookup"><span data-stu-id="89ec7-108">Returns a [DVDRect](dvdrect-object.md) object containing four read/write properties: (top left) x; (top left) y, Width, and Height.</span></span> <span data-ttu-id="89ec7-109">Les propriétés **x** et **y** sont définies sur zéro et les deux autres propriétés reflètent la largeur et la hauteur du rectangle vidéo tel qu’il a été créé sur le disque.</span><span class="sxs-lookup"><span data-stu-id="89ec7-109">The **x** and **y** properties are set to zero and the other two properties reflect the width and height of the video rectangle as authored on the disc.</span></span>

 

 



