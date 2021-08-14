---
title: Implémentation de CPluginWindow
description: Implémentation de CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- plug-ins Lecteur Windows Media, classe CPluginWindow
- plug-ins, classe CPluginWindow
- plug-ins d’interface utilisateur, classe CPluginWindow
- Plug-ins d’interface utilisateur, classe CPluginWindow
- CPluginWindow, classe
- Guide de programmation, plug-ins d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6364d991fb219678d4f64b09ae4cd3df2526e77797093dcfff3a8dbce7f36101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748134"
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

 

 




