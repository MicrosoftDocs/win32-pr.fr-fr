---
title: Référencement d’apparences dans des URL
description: Référencement d’apparences dans des URL
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Apparences du lecteur Windows Media, références d’URL
- apparences, références d’URL
- Références d’URL dans les apparences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675565"
---
# <a name="referencing-skins-in-urls"></a><span data-ttu-id="730ab-106">Référencement d’apparences dans des URL</span><span class="sxs-lookup"><span data-stu-id="730ab-106">Referencing Skins in URLs</span></span>

<span data-ttu-id="730ab-107">Si vous utilisez une URL pour charger un fichier multimédia qui sera lu par le lecteur Windows Media, vous pouvez demander qu’une apparence particulière soit utilisée avec ce fichier.</span><span class="sxs-lookup"><span data-stu-id="730ab-107">If you use a URL to load a media file that will be played by Windows Media Player, you can request that a particular skin be used with that file.</span></span> <span data-ttu-id="730ab-108">Si l’apparence est déjà installée sur l’ordinateur de l’utilisateur, elle est utilisée ; dans le cas contraire, l’apparence précédente sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="730ab-108">If the skin is already installed on the user's machine, it will be used; otherwise the previous skin will be used.</span></span>

<span data-ttu-id="730ab-109">Pour demander une apparence, ajoutez le code suivant à la fin de l’URL :</span><span class="sxs-lookup"><span data-stu-id="730ab-109">To request a skin, add the following to the end of the URL:</span></span>


```C++
?WMPSkin=skinname
```



<span data-ttu-id="730ab-110">*skinname* est le nom de l’apparence que vous souhaitez demander.</span><span class="sxs-lookup"><span data-stu-id="730ab-110">*skinname* is the name of the skin you want to request.</span></span> <span data-ttu-id="730ab-111">N’utilisez pas de guillemets autour du nom de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="730ab-111">Do not use quotes around the name of the skin.</span></span>

<span data-ttu-id="730ab-112">Par exemple, pour demander l’utilisation de l’apparence de l’en-dessus, tapez l’URL http suivante :</span><span class="sxs-lookup"><span data-stu-id="730ab-112">For example, to request the headspace skin be used, type the following http URL:</span></span>


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a><span data-ttu-id="730ab-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="730ab-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="730ab-114">**À propos des apparences**</span><span class="sxs-lookup"><span data-stu-id="730ab-114">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




