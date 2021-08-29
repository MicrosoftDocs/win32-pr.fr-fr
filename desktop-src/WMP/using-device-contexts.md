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
ms.openlocfilehash: 35e07247de9496cd0221b6031e65c0f68def0bade8ce1c814c5096daff486098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507149"
---
# <a name="using-device-contexts"></a>Utilisation des contextes de périphérique

Le contexte de périphérique est un handle standard d’un contexte de périphérique. vous en avez besoin pour de nombreuses fonctions de dessin afin que Microsoft Windows sache à quelle fenêtre dessiner. Par exemple, pour dessiner un rectangle, vous devez spécifier le contexte de périphérique.


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



le contexte de périphérique (device context) est spécifié par Lecteur Windows Media via la fonction **Render** . Si votre plug-in s’affiche à l’aide d’une fenêtre, vous devez utiliser le contexte de périphérique de cette fenêtre. Utilisez ce contexte de périphérique pour tous les outils de dessin qui requièrent un contexte de périphérique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation du rendu**](implementing-render.md)
</dt> </dl>

 

 




