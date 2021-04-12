---
title: Comparaison de l’accélération matérielle de Direct2D et GDI
description: Direct2D et GDI sont des API de rendu 2D en mode immédiat et offrent tous les deux un certain niveau d’accélération matérielle.
ms.assetid: 0028a0c3-445d-46b7-b55b-46dff3bce9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f05dce8719f4d07d3160c65b88570391c3eb736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315258"
---
# <a name="comparing-direct2d-and-gdi-hardware-acceleration"></a>Comparaison de l’accélération matérielle de Direct2D et GDI

[Direct2D](./direct2d-portal.md) et [GDI](/windows/desktop/gdi/windows-gdi) sont des API de rendu 2D en mode immédiat et offrent tous les deux un certain niveau d’accélération matérielle. Cette rubrique explore les différences entre Direct2D et GDI, y compris les différences passées et actuelles dans les fonctionnalités d’accélération matérielle des deux API.

Cette rubrique contient les éléments suivants :

-   [Différences entre Direct2D et GDI](#differences-between-direct2d-and-gdi)
-   [Accélération matérielle GDI et Direct2D](#gdi-and-direct2d-hardware-acceleration)
    -   [Complexité croissante et taille des pilotes d’affichage](#increasing-complexity-and-size-of-display-drivers)
    -   [Difficulté de la synchronisation des espaces d’adressage de la session et du noyau global](#difficulty-in-synchronizing-session-and-global-kernel-address-spaces)
    -   [Gestion de fenêtres composites](#composited-window-management)
-   [Rendu GDI dans Windows 7](#gdi-rendering-in-windows-7)
-   [Différences entre l’accélération Direct2D et GDI dans Windows 7](#contrasting-direct2d-and-gdi-acceleration-in-windows-7)
    -   [Emplacement des ressources](#location-of-resources)
    -   [Méthode de rendu](#rendering-method)
    -   [Extensibilité](#scalability)
    -   [Lieu](#location-of-resources)
    -   [Disponibilité de l’accélération matérielle](#availability-of-hardware-acceleration)
    -   [Modèle de présentation](#presentation-model)
-   [Conclusion](#conclusion)

## <a name="differences-between-direct2d-and-gdi"></a>Différences entre Direct2D et GDI

[GDI](/windows/desktop/gdi/windows-gdi) effectue le rendu des géométries opaques, telles que les polygones, les ellipses et les lignes. Il restitue le texte avec alias et ClearType, et il peut prendre en charge la fusion de transparence par le biais de l’API AlphaBlend. Toutefois, sa gestion de la transparence est incohérente et la plupart des API GDI ignorent simplement le canal alpha. Peu d’API GDI garantissent ce que le canal alpha contiendra après une opération. Plus important encore, le rendu de GDI n’est pas facilement mappé aux opérations 3D et un GPU moderne est rendu le plus efficacement possible sur la partie 3D de son moteur de rendu. Par exemple, les lignes avec alias de [Direct2D](./direct2d-portal.md)sont conçues pour être implémentées simplement comme deux triangles restitués sur le GPU, tandis que GDI utilise l’algorithme de dessin de lignes de Bresenham.

[Direct2D](./direct2d-portal.md) rend les primitives opaque, transparente, avec alias et avec anticrénelage. Les interfaces utilisateur modernes utilisent souvent la transparence et l’animation. Direct2D facilite la création d’une interface utilisateur moderne, car il offre des garanties strictes quant à la façon dont il accepte et restitue le contenu transparent, et toutes ses primitives sont rendues à l’aide de l’accélération matérielle. Direct2D n’est pas un sur-ensemble pur de [GDI](/windows/desktop/gdi/windows-gdi): les primitives qui auraient été déraisonnablement lentes lorsqu’elles étaient implémentées sur un GPU ne sont pas présentes dans Direct2D. Comme Direct2D est construit avec cette mise en évidence sur l’accélération 3D, il est également facile à utiliser avec Direct3D.

Depuis Windows NT 4, [GDI](/windows/desktop/gdi/windows-gdi) s’exécute en mode noyau. L’application appelle GDI, qui appelle ensuite son équivalent en mode noyau qui transmet les primitives à son propre modèle de pilote. Ce pilote envoie ensuite les résultats au pilote d’affichage global en mode noyau.

À compter de Windows 2000, [GDI](/windows/desktop/gdi/windows-gdi) et les pilotes GDI s’exécutent dans un espace indépendant dans le noyau appelé « espace de session ». Un espace d’adressage de session est créé pour chaque session de connexion, et chaque instance de GDI s’exécute indépendamment dans cet espace d’adressage en mode noyau distinct. Toutefois, Direct2D s’exécute en mode utilisateur et passe les commandes de dessin via le pilote Direct3D en mode utilisateur au pilote en mode noyau.

![Figure 1-Direct2D comparé à GDI](images/direct2d-vs-gdi1.png)

## <a name="gdi-and-direct2d-hardware-acceleration"></a>Accélération matérielle GDI et Direct2D

La différence la plus importante entre l’accélération matérielle [Direct2D](./direct2d-portal.md) et [GDI](/windows/desktop/gdi/windows-gdi) est la technologie sous-jacente qui les pilote. Direct2D est superposé sur les principaux Direct3D et GDI possède son propre modèle de pilote, l’interface DDI (Device Driver Interface) GDI, qui correspond aux primitives GDI. Le modèle de pilote Direct3D correspond à ce que le matériel de rendu 3D dans un GPU restitue. Lorsque l’interface DDI GDI a été définie pour la première fois, la plupart du matériel d’accélération de l’affichage ciblait les primitives GDI. Au fil du temps, une plus grande importance a été placée sur l’accélération des jeux en 3D et moins sur l’accélération des applications. Par conséquent, l’API BitBlt était l’accélération matérielle et la plupart des autres opérations GDI n’étaient pas effectuées.

Cela permet de définir la phase d’une séquence de modifications du rendu de [GDI](/windows/desktop/gdi/windows-gdi) à l’affichage. L’illustration suivante montre comment le rendu de l’affichage GDI est passé de Windows XP à Windows 7.

![Figure 2 : évolution du rendu de l’affichage GDI](images/direct2d-vs-gdi2.png)

Il y avait également un certain nombre de facteurs supplémentaires qui ont entraîné des modifications du modèle de pilote [GDI](/windows/desktop/gdi/windows-gdi) , comme expliqué ci-dessous.

### <a name="increasing-complexity-and-size-of-display-drivers"></a>Complexité croissante et taille des pilotes d’affichage

les pilotes 3D sont devenus plus complexes au fil du temps. Un code plus complexe a tendance à avoir plus de défauts, ce qui permet au pilote d’exister en mode utilisateur, où un bogue de pilote ne peut pas provoquer un redémarrage du système. Comme vous pouvez le voir dans la figure ci-dessus, le pilote d’affichage est divisé en un composant en mode utilisateur complexe et un composant plus simple en mode noyau.

### <a name="difficulty-in-synchronizing-session-and-global-kernel-address-spaces"></a>Difficulté de la synchronisation des espaces d’adressage de la session et du noyau global

Dans Windows XP, un pilote d’affichage existe dans deux espaces d’adressage différents : l’espace de session et l’espace du noyau. Certaines parties du pilote doivent répondre à des événements tels que les événements de gestion de l’alimentation. Cela doit être synchronisé avec l’état du pilote dans l’espace d’adressage de la session. Il s’agit d’une tâche difficile qui peut entraîner des défauts lorsque les pilotes d’affichage essaient de traiter ces espaces d’adressage distincts.

### <a name="composited-window-management"></a>Gestion de fenêtres composites

Le Gestionnaire de fenêtrage (DWM), le gestionnaire de fenêtres de composition introduit dans Windows 7, restitue toutes les fenêtres à des surfaces hors écran, puis les compose pour les afficher à l’écran. Cela nécessite que [GDI](/windows/desktop/gdi/windows-gdi) puisse être rendu sur une surface qui sera ensuite rendue par Direct3D à afficher. Cela posait un problème dans le modèle de pilote XP, car GDI et Direct3D étaient des piles de pilotes parallèles.

Par conséquent, dans Windows Vista, le pilote d’affichage DDI [GDI](/windows/desktop/gdi/windows-gdi) a été implémenté en tant que pilote d’affichage canonique fourni par Microsoft (CDD) qui affichait le contenu GDI dans une image bitmap de mémoire système pour qu’il soit composé à l’écran.

## <a name="gdi-rendering-in-windows-7"></a>Rendu GDI dans Windows 7

Le modèle de pilote utilisé dans Windows Vista exigeait que chaque fenêtre [GDI](/windows/desktop/gdi/windows-gdi) soit sauvegardée à la fois par une surface de mémoire vidéo et une surface de mémoire système. Cela a entraîné l’utilisation de la mémoire système pour chaque fenêtre GDI.

Pour cette raison, [GDI](/windows/desktop/gdi/windows-gdi) a été de nouveau modifié dans Windows 7. . Au lieu d’effectuer un rendu sur une surface de mémoire système, GDI a été modifié pour être rendu sur un segment de mémoire d’ouverture. La mémoire d’ouverture peut être mise à jour à partir de l’aire mémoire vidéo contenant le contenu de la fenêtre. GDI peut retourner à la mémoire d’ouverture et le résultat peut ensuite être renvoyé à la surface de la fenêtre. Étant donné que le segment de mémoire d’ouverture est adressable par le GPU, le GPU peut accélérer ces mises à jour de la surface de la mémoire vidéo. Par exemple, le rendu de texte, BitBlts, AlphaBlend, TransparentBlt et StretchBlt sont accélérés dans ces cas.

## <a name="contrasting-direct2d-and-gdi-acceleration-in-windows-7"></a>Différences entre l’accélération Direct2D et GDI dans Windows 7

[Direct2D](./direct2d-portal.md) et [GDI](/windows/desktop/gdi/windows-gdi) sont des API de rendu en mode immédiat 2D et sont accélérées par le matériel. Toutefois, il existe un certain nombre de différences qui restent dans les deux API.

### <a name="location-of-resources"></a>Emplacement des ressources

[GDI](/windows/desktop/gdi/windows-gdi) conserve ses ressources, notamment les bitmaps, dans la mémoire système par défaut. [Direct2D](./direct2d-portal.md) conserve ses ressources dans la mémoire vidéo sur la carte graphique. Lorsque GDI doit mettre à jour la mémoire vidéo, cette opération doit être effectuée sur le bus, sauf si la ressource figure déjà dans le segment de mémoire à l’ouverture ou si l’opération peut être exprimée directement. En revanche, Direct2D peut simplement traduire ses primitives en primitives Direct3D, car les ressources se trouvent déjà dans la mémoire vidéo.

### <a name="rendering-method"></a>Méthode de rendu

Pour assurer la compatibilité, [GDI](/windows/desktop/gdi/windows-gdi) effectue une grande partie de son rendu à la mémoire d’ouverture à l’aide de l’UC. En revanche, [Direct2D](./direct2d-portal.md) traduit ses appels d’API en opérations de dessin et primitives Direct3D. Le résultat est ensuite rendu sur le GPU. Une partie du rendu GDI ? s est effectuée sur le GPU lorsque la mémoire d’ouverture est copiée sur la surface de mémoire vidéo représentant la fenêtre GDI.

### <a name="scalability"></a>Extensibilité

Les appels de rendu de [Direct2D](./direct2d-portal.md)sont tous des flux de commandes indépendants vers le GPU. Chaque fabrique Direct2D représente un appareil Direct3D différent. [GDI](/windows/desktop/gdi/windows-gdi) utilise un flux de commande pour toutes les applications sur le système. La méthode GDI peut entraîner une accumulation de la surcharge du contexte de rendu du GPU et de l’UC.

### <a name="location"></a>Emplacement

[Direct2D](./direct2d-portal.md) fonctionne entièrement en mode utilisateur, y compris le runtime Direct3D et le pilote Direct3D en mode utilisateur. Cela permet d’éviter les pannes système causées par des erreurs de code dans le noyau. [GDI](/windows/desktop/gdi/windows-gdi), toutefois, possède la plupart de ses fonctionnalités dans l’espace de session en mode noyau, avec sa surface d’API en mode utilisateur.

### <a name="availability-of-hardware-acceleration"></a>Disponibilité de l’accélération matérielle

[GDI](/windows/desktop/gdi/windows-gdi) est l’accélération matérielle sur Windows XP et est accéléré sur Windows 7 lorsque le gestionnaire de fenêtrage est en cours d’exécution et qu’un pilote WDDM 1,1 est en cours d’utilisation. [Direct2D](./direct2d-portal.md) est l’accélération matérielle sur la quasi-totalité des pilotes WDDM et indique si DWM est en cours d’utilisation. Sur Vista, GDI est toujours rendu sur le processeur.

### <a name="presentation-model"></a>Modèle de présentation

Lorsque Windows était conçu pour la première fois, la mémoire était insuffisante pour permettre le stockage de chaque fenêtre dans sa propre bitmap. Par conséquent, [GDI](/windows/desktop/gdi/windows-gdi) est toujours rendu logiquement à l’écran, avec plusieurs régions de découpage appliquées pour s’assurer qu’une application n’a pas été rendue en dehors de sa fenêtre. Dans le modèle [Direct2D](./direct2d-portal.md) , une application est rendue en mémoire tampon d’arrière-plan, et le résultat s’affiche lorsque l’application effectue un dessin. Cela permet à Direct2D de gérer des scénarios d’animation bien plus fluides que GDI.

## <a name="conclusion"></a>Conclusion

Le code [GDI](/windows/desktop/gdi/windows-gdi) existant continuera à fonctionner correctement sous Windows 7. Toutefois, lors de l’écriture d’un nouveau code de rendu graphique, [Direct2D](./direct2d-portal.md) doit être pris en compte, car il tire le meilleur parti des GPU modernes.

 

 