---
title: Fonctions de format de pixel
description: Les fonctions Windows suivantes gèrent les formats de pixel.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Fonctions WGL, format de pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840769"
---
# <a name="pixel-format-functions"></a><span data-ttu-id="bf480-104">Fonctions de format de pixel</span><span class="sxs-lookup"><span data-stu-id="bf480-104">Pixel Format Functions</span></span>

<span data-ttu-id="bf480-105">Les fonctions Windows suivantes gèrent les formats de pixel.</span><span class="sxs-lookup"><span data-stu-id="bf480-105">The following Windows functions manage pixel formats.</span></span>



| <span data-ttu-id="bf480-106">Fonction Windows</span><span class="sxs-lookup"><span data-stu-id="bf480-106">Windows Function</span></span>                                               | <span data-ttu-id="bf480-107">Description</span><span class="sxs-lookup"><span data-stu-id="bf480-107">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf480-108">**ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="bf480-108">**ChoosePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | <span data-ttu-id="bf480-109">Obtient le format de pixel du contexte de périphérique qui correspond le plus à un format de pixel spécifié.</span><span class="sxs-lookup"><span data-stu-id="bf480-109">Obtains the device context's pixel format that is the closest match to a specified pixel format.</span></span>                                                                      |
| [<span data-ttu-id="bf480-110">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="bf480-110">**SetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | <span data-ttu-id="bf480-111">Définit le format de pixel actuel d’un contexte de périphérique au format de pixel spécifié par un index de format de pixel.</span><span class="sxs-lookup"><span data-stu-id="bf480-111">Sets a device context's current pixel format to the pixel format specified by a pixel format index.</span></span>                                                                   |
| [<span data-ttu-id="bf480-112">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="bf480-112">**GetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | <span data-ttu-id="bf480-113">Obtient l’index de format de pixel du format de pixel actuel d’un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="bf480-113">Obtains the pixel format index of a device context's current pixel format.</span></span>                                                                                            |
| [<span data-ttu-id="bf480-114">**DescribePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="bf480-114">**DescribePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | <span data-ttu-id="bf480-115">Étant donné un contexte de périphérique et un index de format de pixel, remplit une structure de données [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) avec les propriétés du format de pixel.</span><span class="sxs-lookup"><span data-stu-id="bf480-115">Given a device context and a pixel format index, fills in a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure with the pixel format's properties.</span></span> |
| [<span data-ttu-id="bf480-116">**GetEnhMetaFilePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="bf480-116">**GetEnhMetaFilePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | <span data-ttu-id="bf480-117">Récupère les informations de format de pixel pour un métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="bf480-117">Retrieves pixel format information for an enhanced metafile.</span></span>                                                                                                          |



 

<span data-ttu-id="bf480-118">La fonction [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) retourne un index de format de pixel de base 1 qui identifie la meilleure correspondance à partir des formats de pixel pris en charge du contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="bf480-118">The [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function returns a one-based pixel format index that identifies the best match from the device context's supported pixel formats.</span></span>

<span data-ttu-id="bf480-119">La fonction [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifie le format souhaité à l’aide d’un index de format de pixel de base 1.</span><span class="sxs-lookup"><span data-stu-id="bf480-119">The [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) function identifies the desired format using a one-based pixel format index.</span></span> <span data-ttu-id="bf480-120">En général, vous appelez **ChoosePixelFormat** pour rechercher un format de pixel le mieux adapté, puis vous appelez **SetPixelFormat** avec le résultat de **ChoosePixelFormat**.</span><span class="sxs-lookup"><span data-stu-id="bf480-120">Typically, you call **ChoosePixelFormat** to find a best-match pixel format, and then call **SetPixelFormat** with the result of **ChoosePixelFormat**.</span></span>

<span data-ttu-id="bf480-121">Si vous appelez **SetPixelFormat** pour un contexte de périphérique qui référence une fenêtre, **SetPixelFormat** modifie également le format de pixel de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bf480-121">If you call **SetPixelFormat** for a device context that references a window, **SetPixelFormat** also changes the pixel format of the window.</span></span> <span data-ttu-id="bf480-122">La définition du format de pixel d’une fenêtre plusieurs fois peut entraîner des complications significatives pour le gestionnaire de fenêtres et pour les applications multithread, ce qui n’est donc pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="bf480-122">Setting the pixel format of a window more than once can lead to significant complications for the Window Manager and for multithread applications, so it is not allowed.</span></span> <span data-ttu-id="bf480-123">Vous ne pouvez définir le format de pixel d’une fenêtre qu’une seule fois ; Après cela, le format de pixel de la fenêtre ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="bf480-123">You can set the pixel format of a window only one time; after that, the window's pixel format cannot be changed.</span></span>

<span data-ttu-id="bf480-124">La fonction [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) retourne un index de format de pixel de base un.</span><span class="sxs-lookup"><span data-stu-id="bf480-124">The [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) function returns a one-based pixel format index.</span></span>

<span data-ttu-id="bf480-125">La fonction [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) prend les valeurs suivantes comme paramètres :</span><span class="sxs-lookup"><span data-stu-id="bf480-125">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function takes the following as parameters:</span></span>

-   <span data-ttu-id="bf480-126">Handle vers un contexte de périphérique (Device Context)</span><span class="sxs-lookup"><span data-stu-id="bf480-126">A handle to a device context</span></span>
-   <span data-ttu-id="bf480-127">Un index de format de pixel</span><span class="sxs-lookup"><span data-stu-id="bf480-127">A pixel format index</span></span>
-   <span data-ttu-id="bf480-128">Pointeur vers une structure de données [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)</span><span class="sxs-lookup"><span data-stu-id="bf480-128">A pointer to a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure</span></span>

<span data-ttu-id="bf480-129">La fonction [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) retourne avec les membres de **PIXELFORMATDESCRIPTOR** définis de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="bf480-129">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function returns with the members of **PIXELFORMATDESCRIPTOR** appropriately set.</span></span>

<span data-ttu-id="bf480-130">La fonction **GetEnhMetaFilePixelFormat** retourne la taille du format de pixel d’un métafichier et récupère les informations de format de pixel du métafichier.</span><span class="sxs-lookup"><span data-stu-id="bf480-130">The **GetEnhMetaFilePixelFormat** function returns the size of a metafile's pixel format and retrieves the pixel format information of the metafile.</span></span>

 

 




