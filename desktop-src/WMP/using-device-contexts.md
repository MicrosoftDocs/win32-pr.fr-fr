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
# <a name="using-device-contexts"></a>Utilisation des contextes de périphérique

Le contexte de périphérique est un handle standard d’un contexte de périphérique. Vous en avez besoin pour de nombreuses fonctions de dessin afin que Microsoft Windows sache quelle fenêtre créer. Par exemple, pour dessiner un rectangle, vous devez spécifier le contexte de périphérique.


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



Le contexte de périphérique (Device Context) est spécifié par le lecteur Windows Media via la fonction de **rendu** . Si votre plug-in s’affiche à l’aide d’une fenêtre, vous devez utiliser le contexte de périphérique de cette fenêtre. Utilisez ce contexte de périphérique pour tous les outils de dessin qui requièrent un contexte de périphérique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation du rendu**](implementing-render.md)
</dt> </dl>

 

 




