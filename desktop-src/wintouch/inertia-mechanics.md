---
title: Mécanismes d’inertie
description: Mécanismes d’inertie
ms.assetid: 188b6936-b36e-4e57-9118-8b61ed134c17
keywords:
- Windows Toucher, inertie
- Windows Tactile, animation lisse
- Windows Toucher, marge élastique
- inertie, mécanique
- inertie, principes de base du calcul
- inertie, présentation physique
- inertie, animation lisse
- inertie, marge élastique
- animation lisse
- marge élastique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79b27900c6921c972710e7e922ab42b834afc1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404213"
---
# <a name="inertia-mechanics"></a>Mécanismes d’inertie

l’inertie est utilisée pour effectuer des calculs pour animer le mouvement des objets et pour activer la prise en charge de la convivialité générique dans les applications qui incorporent Windows Touch. Cette section illustre les fonctionnalités suivantes qui sont activées par inertie.

-   Brève vue d’ensemble de la physique d’inertie.
-   Animation lisse des objets à l’aide des propriétés de vélocité et de décélération.
-   Animation lisse des objets à l’aide d’une propriété de déplacement.
-   Rebond à partir des bords de l’écran à l’aide de limites élastiques.

## <a name="inertia-physics-overview"></a>Vue d’ensemble physique de l’inertie

Le processeur d’inertie utilise un modèle physique simple qui incorpore une position, une valeur de décélération et une rapidité initiale. L’heure est utilisée comme entrée dynamique dans le modèle pour déterminer la position actuelle d’un objet en cours de déplacement. Le graphique et la formule suivants décrivent le modèle physique utilisé pour calculer les positions des objets.

![illustration illustrant le graphique et la formule utilisés pour calculer les positions des objets](images/velocity.png)

Dans la formule utilisée pour calculer la position actuelle (x), la vélocité initiale (v) est multipliée par le temps écoulé (t) et est réduite par le facteur de décélération (d) multiplié par le temps. Cela entraîne une décélération lisse des objets. Dans l’illustration précédente de la partie initiale (la plus à gauche) de la courbe, l’objet se déplace rapidement, car sa vélocité actuelle est la vélocité initiale. À la dernière partie (la plus à droite) de la courbe, l’objet a été complètement arrêté, car sa vélocité est 0. Les calculs de vélocité d’objet pour la vélocité x, la vélocité y et la vélocité de rotation utilisent tous cette formule pour les calculs.

Toute distance utilisée pour le processeur d’inertie est relative. Si vous souhaitez utiliser des coordonnées d’écran, vous transmettez des coordonnées d’écran au processeur de manipulation (ou d’inertie); Si vous souhaitez utiliser des coordonnées absolues, vous devez les transmettre au processeur que vous utilisez. Quelles que soient les valeurs que vous utilisez, le processeur de manipulation utilise des battements d’horloge en millisecondes pour traiter le temps. Ces valeurs peuvent être passées directement au processeur d’inertie à l’aide de la méthode [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) ou en utilisant l’horodatage par défaut via les appels au [**processus**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process).

## <a name="smooth-object-animation-using-the-velocity-and-deceleration-properties"></a>Animation lisse des objets à l’aide des propriétés de vélocité et de décélération

Vous pouvez activer l’animation lisse en interagissant directement avec le modèle physique en définissant les valeurs de vélocité et de décélération dans l’interface du processeur d’inertie, puis en appelant le [**processus**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process). Le **processus** appelant déclenche des manipulations d’objets qui, à leur tour, doivent provoquer des mises à jour de l’interface utilisateur. Les valeurs de vélocité d’objet passées au processeur d’inertie sont généralement récupérées à partir du processeur de manipulation une fois l’opération terminée. Votre valeur de décélération dépend de la durée pendant laquelle vous souhaitez que votre objet soit animé et des unités que vous utilisez pour vos calculs. Étant donné que les valeurs sont dépendantes, vous devez parfois mettre à l’échelle la vitesse d’entrée à partir du processeur maniplation et utiliser des valeurs arbitraires pour la décélération. Les valeurs suivantes sont typiques pour les différents scénarios dans lesquels vous passez des valeurs centipixel à partir des propriétés x et y de la structure [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) au processeur de manipulation.



| Scénario    | Jeu de propriétés                                                                       | Valeur de décélération | Mise à l’échelle d’entrée de vélocité classique                                  | Notes                                                                                 |
|-------------|------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| Traduction | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,003 f             | Aucun.                                                           | L’utilisation de cette valeur entraîne des animations à distance plus longues lors de l’utilisation de l’entrée tactile.    |
| Traduction | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,001 f             | Vitesse initiale de 1/20 pour les entrées tactiles, aucune pour les entrées de souris | L’utilisation de cette valeur est animée pour environ une deuxième entrée de vélocité standard donnée.      |
| Traduction | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,5 f               | None                                                            | l’utilisation de cette valeur donne un sentiment naturel à l’animation sur les écrans grand Windows Touch.   |
| Rotation    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000015 f          | Radians convertis en degrés.                                   | L’utilisation de cette valeur entraîne des animations de rotation plus longues lors de l’utilisation de l’entrée tactile.      |
| Rotation    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0,00001 f           | Delta de rotation 1/40th pour les entrées tactiles, aucune pour les entrées de souris   | Cette valeur est exprimée en radians. vous devez donc utiliser de très petites valeurs de décélération et de vélocité. |
| Rotation    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000005 f          | None                                                            | cette valeur a un aspect naturel sur les écrans tactiles de grande Windows.                        |



 

## <a name="smooth-object-animation-using-the-desired-displacement-property"></a>Animation lisse des objets à l’aide de la propriété de déplacement souhaitée

Dans certains cas, vous ne souhaitez pas utiliser l’entrée de l’utilisateur pour le déplacement de l’objet, mais vous souhaitez tout de même qu’un objet s’anime en douceur sur l’écran. Dans ce cas, vous pouvez utiliser les propriétés de déplacement dans le processeur d’inertie pour que le processeur calcule la rapidité initiale pour déplacer un objet sur l’écran.

## <a name="controlling-object-position-using-elastic-bounds"></a>Contrôle de la position d’un objet à l’aide de limites élastiques

Une fois que vous avez un objet qui se déplace à travers l’écran, vous souhaiterez généralement qu’il s’arrête avant de sortir du point de vue de l’utilisateur. Le processeur d’inertie active cette fonctionnalité via les propriétés des marges et des marges élastiques. L’illustration suivante montre les différentes propriétés de limite et de marge dans une application classique.

![capture d’écran montrant les propriétés des marges et des marges élastiques](images/elastic-illustrated.png)

Vous définissez les limites gauche, supérieure, droite et inférieure et les marges élastiques pour votre application, et le processeur d’inertie gère les éléments d’interface utilisateur dans les limites. Quand un objet atteint une marge élastique, il ralentit jusqu’à ce qu’il atteigne la limite. Elle ne retournera jamais cette marge pendant l’inertie, mais continuera à se déplacer jusqu’à ce que le composant d’inertie perpendiculaire de l’objet décélère à 0. Dans l’illustration, un cercle est placé vers la limite élastique gauche. La flèche pleine indique la direction de la manipulation ; le cercle plein est la position initiale de l’objet. la flèche pleine est constituée des modifications apportées avant que le cercle atteigne la marge élastique ; la flèche pointillée indique où le processeur d’inertie manipule le cercle après avoir atteint la marge ; et les cercles en pointillés indiquent où l’objet s’arrête.

> [!Note]  
> La définition des propriétés de marge déplace les limites vers l’extérieur. Par exemple, si la limite supérieure est définie sur 50 et que vous définissez ensuite la marge élastique supérieure sur 10, votre limite supérieure devient alors de 40.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de l’inertie dans du code non managé](handling-inertia-in-unmanaged-code.md)
</dt> <dt>

[Inertie](getting-started-with-inertia.md)
</dt> <dt>

[Manipulations](getting-started-with-manipulations.md)
</dt> </dl>

 

 




