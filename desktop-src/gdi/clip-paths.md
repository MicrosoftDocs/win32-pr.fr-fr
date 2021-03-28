---
description: Comme pour une zone de découpage, un tracé de clip est un autre objet graphique qu’une application peut sélectionner dans un contexte de périphérique.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Tracés de clip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972758"
---
# <a name="clip-paths"></a><span data-ttu-id="0938b-103">Tracés de clip</span><span class="sxs-lookup"><span data-stu-id="0938b-103">Clip Paths</span></span>

<span data-ttu-id="0938b-104">Comme pour une zone de découpage, un tracé de clip est un autre objet graphique qu’une application peut sélectionner dans un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0938b-104">Like a clipping region, a clip path is another graphics object that an application can select into a device context.</span></span> <span data-ttu-id="0938b-105">Contrairement à une zone de découpage, un tracé de clip est toujours créé par une application et il est utilisé pour le découpage vers une ou plusieurs formes irrégulières.</span><span class="sxs-lookup"><span data-stu-id="0938b-105">Unlike a clipping region, a clip path is always created by an application and it is used for clipping to one or more irregular shapes.</span></span> <span data-ttu-id="0938b-106">Par exemple, une application peut utiliser les lignes et les courbes qui forment les contours de caractères dans une chaîne de texte pour définir un tracé de clip.</span><span class="sxs-lookup"><span data-stu-id="0938b-106">For example, an application can use the lines and curves that form the outlines of characters in a string of text to define a clip path.</span></span>

<span data-ttu-id="0938b-107">Pour créer un tracé de clip, il est tout d’abord nécessaire de créer un chemin d’accès qui décrit la forme irrégulière requise.</span><span class="sxs-lookup"><span data-stu-id="0938b-107">To create a clip path, it's first necessary to create a path that describes the required irregular shape.</span></span> <span data-ttu-id="0938b-108">Les chemins d’accès sont créés en appelant les fonctions de dessin GDI (Graphics Device Interface) appropriées après l’appel de la fonction [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) et avant l’appel de la fonction [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) .</span><span class="sxs-lookup"><span data-stu-id="0938b-108">Paths are created by calling the appropriate graphics device interface (GDI) drawing functions after calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function and before calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="0938b-109">Cette collection de fonctions est appelée un crochet de tracé.</span><span class="sxs-lookup"><span data-stu-id="0938b-109">This collection of functions is called a path bracket.</span></span> <span data-ttu-id="0938b-110">Pour plus d’informations sur les chemins d’accès et les crochets, consultez [chemins](paths.md)d’accès.</span><span class="sxs-lookup"><span data-stu-id="0938b-110">For more information about paths and path brackets, see [Paths](paths.md).</span></span>

<span data-ttu-id="0938b-111">Une fois le chemin d’accès créé, il peut être converti en chemin d’accès de clip en appelant la fonction [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) , en identifiant un contexte de périphérique et en spécifiant un mode d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="0938b-111">After the path is created, it can be converted to a clip path by calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function, identifying a device context, and specifying a usage mode.</span></span> <span data-ttu-id="0938b-112">Le mode d’utilisation détermine la façon dont le système combine le nouveau chemin d’accès au clip avec la région de découpage d’origine du contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0938b-112">The usage mode determines how the system combines the new clip path with the device context's original clipping region.</span></span> <span data-ttu-id="0938b-113">Le tableau suivant décrit les modes d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="0938b-113">The following table describes the usage modes.</span></span>



| <span data-ttu-id="0938b-114">Mode</span><span class="sxs-lookup"><span data-stu-id="0938b-114">Mode</span></span>      | <span data-ttu-id="0938b-115">Description</span><span class="sxs-lookup"><span data-stu-id="0938b-115">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0938b-116">RGN \_ et</span><span class="sxs-lookup"><span data-stu-id="0938b-116">RGN\_AND</span></span>  | <span data-ttu-id="0938b-117">Le chemin d’accès au clip comprend l’intersection (zones qui se chevauchent) de la zone de découpage du contexte de périphérique et du chemin d’accès actuel.</span><span class="sxs-lookup"><span data-stu-id="0938b-117">The clip path includes the intersection (overlapping areas) of the device context's clipping region and the current path.</span></span>    |
| <span data-ttu-id="0938b-118">\_copie RGN</span><span class="sxs-lookup"><span data-stu-id="0938b-118">RGN\_COPY</span></span> | <span data-ttu-id="0938b-119">Le chemin d’accès au clip est le chemin d’accès actuel.</span><span class="sxs-lookup"><span data-stu-id="0938b-119">The clip path is the current path.</span></span>                                                                                           |
| <span data-ttu-id="0938b-120">\_diff RGN</span><span class="sxs-lookup"><span data-stu-id="0938b-120">RGN\_DIFF</span></span> | <span data-ttu-id="0938b-121">Le chemin d’accès au clip comprend la région de découpage du contexte de périphérique et les parties d’intersection du chemin d’accès actuel sont exclues.</span><span class="sxs-lookup"><span data-stu-id="0938b-121">The clip path includes the device context's clipping region with any intersecting parts of the current path excluded.</span></span>        |
| <span data-ttu-id="0938b-122">RGN \_ ou</span><span class="sxs-lookup"><span data-stu-id="0938b-122">RGN\_OR</span></span>   | <span data-ttu-id="0938b-123">Le chemin d’accès au clip comprend l’Union (zones combinées) de la zone de découpage du contexte de périphérique et le chemin d’accès actuel.</span><span class="sxs-lookup"><span data-stu-id="0938b-123">The clip path includes the union (combined areas) of the device context's clipping region and the current path.</span></span>              |
| <span data-ttu-id="0938b-124">RGN \_ Xor</span><span class="sxs-lookup"><span data-stu-id="0938b-124">RGN\_XOR</span></span>  | <span data-ttu-id="0938b-125">Le chemin d’accès au clip inclut l’Union entre la zone de découpage du contexte de périphérique et le chemin d’accès actuel, mais exclut l’intersection.</span><span class="sxs-lookup"><span data-stu-id="0938b-125">The clip path includes the union of the device context's clipping region and the current path but excludes the intersection.</span></span> |



 

 

 



