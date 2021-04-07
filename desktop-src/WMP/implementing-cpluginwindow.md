---
title: Implémentation de CPluginWindow
description: Implémentation de CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Plug-ins du lecteur Windows Media, classe CPluginWindow
- plug-ins, classe CPluginWindow
- plug-ins d’interface utilisateur, classe CPluginWindow
- Plug-ins d’interface utilisateur, classe CPluginWindow
- CPluginWindow, classe
- Guide de programmation, plug-ins d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672249"
---
# <a name="implementing-cpluginwindow"></a>Implémentation de CPluginWindow

La classe CPluginWindow fournit l’interface utilisateur du plug-in. Dans le cas du plug-in de l’interface utilisateur de recherche, cette classe contient le code pour le bouton **Rechercher** et le code qui lance la page de recherche lorsque l’utilisateur clique sur le bouton.

L’Assistant fournit une implémentation de base de CPluginWindow dans le fichier d’en-tête CPluginWindow. h. Pour simplifier les choses, le plug-in de l’interface utilisateur de recherche modifie ce fichier directement, bien que les ajouts approfondis soient normalement placés dans un fichier CPluginWindow. cpp distinct.

Les sections suivantes décrivent ce que vous devez faire pour implémenter CPluginWindow :

-   [La table des messages](the-message-map.md)
-   [Le constructeur](the-constructor.md)
-   [Méthode OnPaint](the-onpaint-method.md)
-   [La méthode OnCreate](the-oncreate-method.md)
-   [Méthode OnSearch](the-onsearch-method.md)
-   [Méthode LaunchPage](the-launchpage-method.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation de plug-ins d’interface utilisateur**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




