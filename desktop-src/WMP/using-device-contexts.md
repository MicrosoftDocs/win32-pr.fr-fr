---
title: Utilisation des contextes de périphérique
description: Utilisation des contextes de périphérique
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- visualisations, contexte de périphérique
- visualisations personnalisées, contexte de périphérique
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- Fonction Render, contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310309"
---
# <a name="using-device-contexts"></a><span data-ttu-id="0b993-108">Utilisation des contextes de périphérique</span><span class="sxs-lookup"><span data-stu-id="0b993-108">Using Device Contexts</span></span>

<span data-ttu-id="0b993-109">Le contexte de périphérique est un handle standard d’un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0b993-109">The device context is a standard handle to a device context.</span></span> <span data-ttu-id="0b993-110">Vous en avez besoin pour de nombreuses fonctions de dessin afin que Microsoft Windows sache quelle fenêtre créer.</span><span class="sxs-lookup"><span data-stu-id="0b993-110">You need this for many drawing functions so that Microsoft Windows knows which window to draw in.</span></span> <span data-ttu-id="0b993-111">Par exemple, pour dessiner un rectangle, vous devez spécifier le contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0b993-111">For example, to draw a rectangle, you need to specify the device context.</span></span>


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



<span data-ttu-id="0b993-112">Le contexte de périphérique (Device Context) est spécifié par le lecteur Windows Media via la fonction de **rendu** .</span><span class="sxs-lookup"><span data-stu-id="0b993-112">The device context is specified by Windows Media Player through the **Render** function.</span></span> <span data-ttu-id="0b993-113">Si votre plug-in s’affiche à l’aide d’une fenêtre, vous devez utiliser le contexte de périphérique de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0b993-113">If your plug-in renders using a window, you'll need to use the device context of that window.</span></span> <span data-ttu-id="0b993-114">Utilisez ce contexte de périphérique pour tous les outils de dessin qui requièrent un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0b993-114">Use this device context for any drawing tool that requires a device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b993-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b993-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b993-116">**Implémentation du rendu**</span><span class="sxs-lookup"><span data-stu-id="0b993-116">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




