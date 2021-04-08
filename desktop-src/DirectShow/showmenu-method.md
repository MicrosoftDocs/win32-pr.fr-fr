---
description: La méthode ShowMenu affiche le menu spécifié à l’écran.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Méthode ShowMenu
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746788"
---
# <a name="showmenu-method"></a><span data-ttu-id="c17c5-103">Méthode ShowMenu</span><span class="sxs-lookup"><span data-stu-id="c17c5-103">ShowMenu Method</span></span>

> [!Note]  
> <span data-ttu-id="c17c5-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c17c5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c17c5-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c17c5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c17c5-106">La `ShowMenu` méthode affiche le menu spécifié à l’écran.</span><span class="sxs-lookup"><span data-stu-id="c17c5-106">The `ShowMenu` method displays the specified menu on the screen.</span></span>

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a><span data-ttu-id="c17c5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c17c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c17c5-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span><span class="sxs-lookup"><span data-stu-id="c17c5-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span></span>
</dt> <dd>

<span data-ttu-id="c17c5-109">Spécifie l’ID de menu en tant qu’entier.</span><span class="sxs-lookup"><span data-stu-id="c17c5-109">Specifies the menu ID as an Integer.</span></span>



| <span data-ttu-id="c17c5-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="c17c5-110">Value</span></span> | <span data-ttu-id="c17c5-111">Description</span><span class="sxs-lookup"><span data-stu-id="c17c5-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="c17c5-112">2</span><span class="sxs-lookup"><span data-stu-id="c17c5-112">2</span></span>     | <span data-ttu-id="c17c5-113">Titre (haut)</span><span class="sxs-lookup"><span data-stu-id="c17c5-113">Title (Top)</span></span> |
| <span data-ttu-id="c17c5-114">3</span><span class="sxs-lookup"><span data-stu-id="c17c5-114">3</span></span>     | <span data-ttu-id="c17c5-115">Root</span><span class="sxs-lookup"><span data-stu-id="c17c5-115">Root</span></span>        |
| <span data-ttu-id="c17c5-116">4</span><span class="sxs-lookup"><span data-stu-id="c17c5-116">4</span></span>     | <span data-ttu-id="c17c5-117">Sous-titres</span><span class="sxs-lookup"><span data-stu-id="c17c5-117">Subpicture</span></span>  |
| <span data-ttu-id="c17c5-118">5</span><span class="sxs-lookup"><span data-stu-id="c17c5-118">5</span></span>     | <span data-ttu-id="c17c5-119">Audio</span><span class="sxs-lookup"><span data-stu-id="c17c5-119">Audio</span></span>       |
| <span data-ttu-id="c17c5-120">6</span><span class="sxs-lookup"><span data-stu-id="c17c5-120">6</span></span>     | <span data-ttu-id="c17c5-121">Angle</span><span class="sxs-lookup"><span data-stu-id="c17c5-121">Angle</span></span>       |
| <span data-ttu-id="c17c5-122">7</span><span class="sxs-lookup"><span data-stu-id="c17c5-122">7</span></span>     | <span data-ttu-id="c17c5-123">Chapitre</span><span class="sxs-lookup"><span data-stu-id="c17c5-123">Chapter</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c17c5-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c17c5-124">Return Value</span></span>

<span data-ttu-id="c17c5-125">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c17c5-125">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c17c5-126">Notes</span><span class="sxs-lookup"><span data-stu-id="c17c5-126">Remarks</span></span>

<span data-ttu-id="c17c5-127">Les noms de menu DVD peuvent être un peu confus.</span><span class="sxs-lookup"><span data-stu-id="c17c5-127">DVD menu names can be somewhat confusing.</span></span> <span data-ttu-id="c17c5-128">Le menu du titre est un autre nom pour le menu Gestionnaire vidéo, le menu principal de l’ensemble du disque. Elle répertorie généralement tous les jeux de titres vidéo disponibles sur le disque. Le menu racine est le menu d’un jeu de titres vidéo, qui peut contenir un titre ou un groupe de titres.</span><span class="sxs-lookup"><span data-stu-id="c17c5-128">The title menu is another name for the Video Manager Menu, the main menu for the entire disc; it generally lists all the video title sets available on the disc. The root menu is the menu for one video title set, which can contain one title or a group of titles.</span></span> <span data-ttu-id="c17c5-129">Tous les titres d’un jeu de titres partagent les mêmes menus de sous-image, audio et d’angle.</span><span class="sxs-lookup"><span data-stu-id="c17c5-129">All the titles in a title set share the same Subpicture, Audio, and Angle menus.</span></span>

 

 



