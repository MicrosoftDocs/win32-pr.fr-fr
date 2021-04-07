---
title: La table des messages
description: La table des messages
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Plug-ins du lecteur Windows Media, table des messages
- plug-ins, table des messages
- plug-ins d’interface utilisateur, table des messages
- Plug-ins d’interface utilisateur, table des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029320"
---
# <a name="the-message-map"></a><span data-ttu-id="b0628-107">La table des messages</span><span class="sxs-lookup"><span data-stu-id="b0628-107">The Message Map</span></span>

<span data-ttu-id="b0628-108">La fenêtre du plug-in répond à différents événements en appelant des méthodes qui sont mappées aux messages d’événements correspondants.</span><span class="sxs-lookup"><span data-stu-id="b0628-108">The plug-in window responds to various events by calling methods that are mapped to corresponding event messages.</span></span> <span data-ttu-id="b0628-109">L’Assistant fournit un mappage afin que OnPaint et OnEraseBackground soient appelés aux moments appropriés.</span><span class="sxs-lookup"><span data-stu-id="b0628-109">The wizard provides a mapping so that OnPaint and OnEraseBackground will be called at the appropriate times.</span></span> <span data-ttu-id="b0628-110">Pour créer le bouton de **recherche** et répondre aux clics, la section de la table des messages est modifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="b0628-110">To create the **Search** button and to respond to clicks from it, the message map section is modified as follows:</span></span>


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a><span data-ttu-id="b0628-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0628-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0628-112">**Implémentation de CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="b0628-112">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




