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
# <a name="referencing-skins-in-urls"></a>Référencement d’apparences dans des URL

Si vous utilisez une URL pour charger un fichier multimédia qui sera lu par le lecteur Windows Media, vous pouvez demander qu’une apparence particulière soit utilisée avec ce fichier. Si l’apparence est déjà installée sur l’ordinateur de l’utilisateur, elle est utilisée ; dans le cas contraire, l’apparence précédente sera utilisée.

Pour demander une apparence, ajoutez le code suivant à la fin de l’URL :


```C++
?WMPSkin=skinname
```



*skinname* est le nom de l’apparence que vous souhaitez demander. N’utilisez pas de guillemets autour du nom de l’apparence.

Par exemple, pour demander l’utilisation de l’apparence de l’en-dessus, tapez l’URL http suivante :


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des apparences**](about-skins.md)
</dt> </dl>

 

 




