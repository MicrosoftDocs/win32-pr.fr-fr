---
description: L’événement UpdateOverlay est envoyé lorsque la surface de recouvrement a été déplacée ou redimensionnée ou que sa clé de couleur a changé.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (Ddraw. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533243"
---
# <a name="updateoverlay"></a><span data-ttu-id="46046-103">UpdateOverlay</span><span class="sxs-lookup"><span data-stu-id="46046-103">UpdateOverlay</span></span>

> [!Note]  
> <span data-ttu-id="46046-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="46046-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="46046-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="46046-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="46046-106">L’événement **UpdateOverlay** est envoyé lorsque la surface de recouvrement a été déplacée ou redimensionnée ou que sa clé de couleur a changé.</span><span class="sxs-lookup"><span data-stu-id="46046-106">The **UpdateOverlay** event is sent when the overlay surface has been moved or resized or its color key has changed.</span></span>

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a><span data-ttu-id="46046-107">Notes</span><span class="sxs-lookup"><span data-stu-id="46046-107">Remarks</span></span>

<span data-ttu-id="46046-108">Les applications ne doivent jamais se préoccuper de la surface de superposition redimensionnée ou déplacée.</span><span class="sxs-lookup"><span data-stu-id="46046-108">Applications should never be concerned about the overlay surface being resized or moved.</span></span> <span data-ttu-id="46046-109">Tout est géré en interne.</span><span class="sxs-lookup"><span data-stu-id="46046-109">This is all handled internally.</span></span> <span data-ttu-id="46046-110">Toutefois, cet événement est également envoyé lorsque la clé de couleur change.</span><span class="sxs-lookup"><span data-stu-id="46046-110">But this event is also sent when the color key changes.</span></span> <span data-ttu-id="46046-111">Cela signifie que si une application héberge MSWebDVD comme un contrôle sans fenêtre et affiche des boutons flottants en plus de la surface vidéo en mode plein écran, elle doit répondre à cet événement en obtenant la nouvelle valeur de la propriété **ColorKey** afin de pouvoir dessiner correctement les boutons.</span><span class="sxs-lookup"><span data-stu-id="46046-111">That means that if an application is hosting MSWebDVD as a windowless control and displaying floating buttons on top of the video surface in full-screen mode, it should respond to this event by getting the new value of the **ColorKey** property so that it can draw the buttons properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="46046-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46046-112">Requirements</span></span>



| <span data-ttu-id="46046-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46046-113">Requirement</span></span> | <span data-ttu-id="46046-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="46046-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46046-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="46046-115">Header</span></span><br/> | <dl> <span data-ttu-id="46046-116"><dt>Ddraw. h</dt></span><span class="sxs-lookup"><span data-stu-id="46046-116"><dt>Ddraw.h</dt></span></span> </dl> |



 

 




