---
title: Implémentation du rendu
description: Implémentation du rendu
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- visualisations, événements chronométrés
- visualisations personnalisées, événements chronométrés
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- visualisations, fonction RenderWindow
- visualisations personnalisées, fonction RenderWindow
- Fonction Render, paramètres
- RenderWindow fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217065"
---
# <a name="implementing-render"></a>Implémentation du rendu

La façon la plus simple de considérer la programmation de la visualisation est que vous créez un gestionnaire pour un événement chronométré. à des intervalles spécifiques, Lecteur Windows Media prend un instantané des données audio qu’il lit et fournit les données d’instantané à la visualisation actuellement chargée. Cela est similaire à la programmation pilotée par les événements et fait partie du modèle de programmation de Microsoft Windows. Vous écrivez du code et attendez qu’il soit appelé par un événement particulier.

Si votre code est une implémentation de la fonction [IWMPEffects :: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) pour le rendu en mode sans fenêtre, il reçoit les paramètres suivants :

*TimedLevel*

Il s’agit d’une structure qui définit les données audio que votre code analysera. La structure est composée de deux tableaux. Le premier tableau est basé sur les informations de fréquence et contient un instantané du spectre audio divisé en portions de 1024. Chaque cellule du tableau contient une valeur comprise entre 0 et 255. La première cellule commence à 20 Hz et la dernière à 22050 Hz. Le tableau est en deux dimensions pour représenter l’audio stéréo. Le deuxième tableau est basé sur les informations de forme d’onde et correspond à la puissance audio, où le plus fort de l’onde est, plus la valeur est grande. Le tableau de forme d’onde est un instantané granulaire des 1024 dernières tranches de puissance audio prises à des intervalles de temps très petits. Ce tableau est également à deux dimensions pour représenter l’audio stéréo.

*HDC*

il s’agit d’un handle de Windows Microsoft vers un contexte de périphérique. Cela donne un moyen d’identifier la surface de dessin à Windows. Vous n’avez pas besoin de la créer, il vous suffit de l’utiliser pour des appels de fonction de dessin spécifiques.

*RECTANGULAIRE*

il s’agit d’un rectangle de Windows Microsoft qui définit la taille d’une surface de dessin. Il s’agit d’un rectangle simple avec quatre propriétés : **gauche**, **droite**, **haut** et **bas**. les valeurs réelles sont fournies par Lecteur Windows Media afin que vous puissiez déterminer la manière dont le développeur de l’utilisateur ou de la peau a dimensionné la fenêtre sur laquelle vous allez dessiner. Elle détermine également la position sur le HDC sur laquelle l’effet est supposé être rendu.

Si votre code est une implémentation de la fonction **IWMPEffects2 :: RenderWindowed** pour le rendu dans une fenêtre, il reçoit les paramètres suivants :

*TimedLevel*

Il s’agit des mêmes informations que celles reçues par la fonction **Render** .

*fRequiredRender*

Le paramètre *fRequiredRender* vous informe que votre visualisation doit se redessiner, par exemple, lorsqu’une autre fenêtre est glissée au-dessus. Lorsque cette valeur est false, vous pouvez ignorer en toute sécurité le code de rendu si l’élément multimédia actuel est arrêté ou suspendu. Cela vous permet d’éviter de consommer inutilement des cycles d’UC.

L’exemple de plug-in généré par l’Assistant de plug-in ne fournit pas d’implémentation personnalisée pour **RenderWindowed**. au lieu de cela, l’exemple de code de plug-in récupère le contexte de périphérique à partir de la fenêtre parente fournie par Lecteur Windows Media dans [IWMPEffects2 :: create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), puis récupère les dimensions de la fenêtre parente comme une structure RECT, puis appelle pour effectuer le **rendu** à l’aide du contexte de périphérique, du RECT et du pointeur de niveau chronométré à partir de **RenderWindowed**.

Les sections suivantes fournissent plus d’informations sur l’implémentation du **rendu**:

-   [Utilisation de niveaux chronométrés](using-timed-levels.md)
-   [Utilisation des contextes de périphérique](using-device-contexts.md)
-   [Utilisation de rectangles](using-rectangles.md)
-   [Exemple de code de rendu](sample-render-code.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de votre code**](implementing-your-code.md)
</dt> </dl>

 

 




