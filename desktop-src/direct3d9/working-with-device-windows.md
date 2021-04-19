---
description: Cette section répertorie un problème que vous pouvez rencontrer lors de l’utilisation de fenêtres d’appareil dans des applications Direct3D.
ms.assetid: 7cfd2ad6-fb85-4303-9fa4-6fe7d16d9951
title: Utilisation des fenêtres d’appareils (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56352ef0ec66def620a0ae0995d92d8b421722e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519179"
---
# <a name="working-with-device-windows-direct3d-9"></a><span data-ttu-id="33f17-103">Utilisation des fenêtres d’appareils (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="33f17-103">Working with Device Windows (Direct3D 9)</span></span>

<span data-ttu-id="33f17-104">Cette section répertorie un problème que vous pouvez rencontrer lors de l’utilisation de fenêtres d’appareil dans des applications Direct3D.</span><span class="sxs-lookup"><span data-stu-id="33f17-104">This section lists an issue that you might encounter when working with device windows in Direct3D applications.</span></span>

-   <span data-ttu-id="33f17-105">Direct3D bloque uniquement les fenêtres de focus au lieu de la fenêtre du périphérique avec la fonction de traitement des messages Direct3D et traite uniquement les messages de la fenêtre de focus.</span><span class="sxs-lookup"><span data-stu-id="33f17-105">Direct3D only hooks up the focus windows instead of the device window with the Direct3D message processing function, and only processes the focus window messages.</span></span> <span data-ttu-id="33f17-106">Par conséquent, la fenêtre de focus doit être le parent d’une fenêtre d’appareil.</span><span class="sxs-lookup"><span data-stu-id="33f17-106">So, the focus window should be the parent of any device window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33f17-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33f17-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33f17-108">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="33f17-108">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



