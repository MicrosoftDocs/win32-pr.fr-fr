---
title: Utilisation de rectangles (Windows Media Player SDK)
description: Utilisation de rectangles
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- visualisations, rectangles
- visualisations personnalisées, rectangles
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- Render, fonction, rectangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106510512"
---
# <a name="using-rectangles-windows-media-player-sdk"></a>Utilisation de rectangles (Windows Media Player SDK)

Les rectangles sont utilisés pour spécifier des zones rectangulaires dans Microsoft Windows. Vous pouvez créer de nombreux rectangles dans votre fenêtre, mais le lecteur Windows Media fournit les valeurs d’un rectangle via la fonction [IWMPEffects :: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) . Si votre plug-in est restitué à l’aide d’une fenêtre, le rectangle est la zone cliente de la fenêtre. C’est ce que l’on appelle le rectangle PRC et définit le rectangle par lequel le lecteur Windows Media affiche votre visualisation. Utilisez cette fréquence pour être certain de ne pas dessiner au-delà des étendues du rectangle fourni par le lecteur Windows Media.

Un rectangle a quatre valeurs qui le définissent. Ils sont gauche, haut, droit et bas. L’angle supérieur gauche du rectangle est défini par des gauches et des haut, et le coin inférieur droit du rectangle est défini par le bas et la droite.

Utilisez le code suivant pour récupérer les étendues de votre rectangle de dessin. Vous devez effectuer cette opération, car l’utilisateur peut redimensionner la fenêtre et vous voulez être sûr que vous dessinez toujours dans une zone que l’utilisateur peut voir.


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



Par exemple, pour dessiner de gauche à droite, en haut de la fenêtre, utilisez un code similaire à celui-ci :


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation du rendu**](implementing-render.md)
</dt> </dl>

 

 




