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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412213"
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

 

 




