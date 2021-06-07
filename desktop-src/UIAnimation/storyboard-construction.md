---
title: Vue d’ensemble du storyboard
description: Cette présentation se concentre sur la façon dont les transitions et les storyboards sont utilisés dans les animations Windows.
ms.assetid: d37718ac-0256-4a24-a26c-d29173593be0
keywords:
- Animation Windows Animation Windows, vue d’ensemble du storyboard
- Animation des storyboards Windows, Description
- transitions Windows animation, Description
- transitions Windows animation, personnalisé
- interpolateurs Windows animation, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58210ae98f6d3a96c554276466ad72b3364d72a1
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524283"
---
# <a name="storyboard-overview"></a>Vue d’ensemble du storyboard

Cette présentation se concentre sur la façon dont les transitions et les storyboards sont utilisés dans les animations Windows. Pour obtenir une vue d’ensemble des composants de Windows animation, consultez [vue d’ensemble des animations Windows](scenic-animation-api-overview.md).

Cette rubrique contient les sections suivantes :

-   [Transitions](#custom-transitions)
    -   [Bibliothèque de transitions](#transition-library)
    -   [Transitions personnalisées](#custom-transitions)
-   [Storyboards](#storyboards)
    -   [Création d’un Storyboard simple](#building-a-simple-storyboard)
    -   [Utilisation d’une durée de Context-Sensitive](#using-a-context-sensitive-duration)
    -   [Création d’un Storyboard plus complexe](#building-a-more-complex-storyboard)
    -   [Utilisation d’images clés](#using-keyframes)
    -   [Conserver les variables](#holding-variables)
    -   [Planification d’une table de montage séquentiel](#scheduling-a-storyboard)
-   [Rubriques connexes](#related-topics)

## <a name="transitions"></a>Transitions

Une transition définit la manière dont une variable d’animation unique change sur un intervalle de temps particulier. Windows animation comprend une bibliothèque de transitions courantes que les développeurs peuvent appliquer à une ou plusieurs variables d’animation. Différents genres de transitions ont des jeux de paramètres différents, qui peuvent inclure la valeur de la variable lorsque la transition se termine, la durée de la transition ou des quantités uniques à la fonction mathématique sous-jacente, telles que l’accélération ou la plage d’oscillation.

Toutes les transitions partagent deux paramètres implicites : la valeur initiale et la vélocité initiale (pente) de la fonction mathématique. Elles peuvent être spécifiées explicitement par l’application, mais elles sont généralement définies par le gestionnaire d’animations sur la valeur et la rapidité de la variable d’animation au début de la transition.

-   [Bibliothèque de transitions](#transition-library)
-   [Transitions personnalisées](#custom-transitions)

### <a name="transition-library"></a>Bibliothèque de transitions

Les transitions suivantes sont actuellement fournies par la bibliothèque de transition. Si une application requiert un effet qui ne peut pas être spécifié à l’aide de la bibliothèque de transition, les développeurs peuvent créer d’autres genres de transitions en implémentant un interpolateur personnalisé pour l’application, ou en utilisant une bibliothèque de transition d’un tiers.



| Nom de la transition                        | Description                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| accélérer la décélération<br/>       | La variable d’animation accélère, puis ralentit sur une durée donnée.<br/>                                                                                                               |
| constant<br/>                    | La variable d’animation reste à sa valeur initiale tout au long de la transition.<br/>                                                                                                            |
| cubiques<br/>                       | La variable d’animation passe de sa valeur initiale à une valeur finale spécifiée, avec une vélocité finale spécifiée, sur une durée donnée.<br/>                                                 |
| discrètes<br/>                    | La variable d’animation reste à sa valeur initiale pour un délai spécifié, puis passe instantanément à une valeur finale spécifiée et reste à cette valeur pour une durée de conservation donnée.<br/> |
| quasi<br/>               | La variable d’animation change instantanément de sa valeur actuelle en une valeur finale spécifiée.<br/>                                                                                               |
| linear<br/>                      | La variable d’animation passe de façon linéaire de sa valeur initiale à une valeur finale spécifiée sur une durée donnée.<br/>                                                                      |
| linéaire à partir de la vitesse<br/>           | La variable d’animation passe de façon linéaire de sa valeur initiale à une valeur finale spécifiée avec une vitesse spécifiée.<br/>                                                                     |
| parabolique de l’accélération<br/> | La variable d’animation passe de sa valeur initiale à une valeur finale spécifiée, avec une vélocité finale spécifiée, en modifiant sa vélocité avec une accélération spécifiée.<br/>               |
| inversion<br/>                    | La variable change de direction sur une durée donnée. La valeur finale sera la même que la valeur initiale et la vélocité finale sera la valeur négative de la rapidité initiale.<br/>          |
| sinusoïdal de la plage<br/>       | La variable oscille dans une plage de valeurs donnée, avec une période spécifiée d’oscillation, pour une durée donnée.<br/>                                                                     |
| sinusoïde à partir de la vélocité<br/>    | La variable oscille avec une période spécifiée d’oscillation, pour une durée donnée. L’amplitude de l’oscillation est déterminée par la rapidité initiale de la variable.<br/>                      |
| arrêt en douceur<br/>                 | La variable d’animation arrive à un arrêt sans heurts à une valeur finale spécifiée, dans une durée maximale.<br/>                                                                              |



 

Le tableau suivant contient des illustrations pour chacune de ces transitions.



|    Illustrations                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![illustration d’une transition instantanée](images/instantaneoustransition.png)  ![illustration d’une transition constante](images/constanttransition.png)  ![illustration d’une transition linéaire](images/lineartransition.png)  ![illustration d’une transition lineat à partir d’une vitesse](images/lineartransitionfromspeed.png)  ![illustration d’une transition discrète](images/discretetransition.png) |
| ![illustration d’une transition parabolique de l’accélération](images/parabolictransitionfromacceleration.png)  ![illustration d’une transition cubique](images/cubictransition.png)  ![illustration d’une transition d’arrêt lisse](images/smoothstoptransition.png)                                                                                                                                       |
| ![illustration d’une transition de contrepassation](images/reversaltransition.png)  ![illustration d’une transition sinusoïdale de la vélocité](images/sinusolidaltransitionfromvelocity.png)  ![illustration d’une transition sinusoïdale à partir d’une plage](images/sinusolidaltransitionfromrange.png)                                                                                                                  |
| ![illustration des transitions de accellerate et de décélération](images/acceleratedeceleratetransition.png)                                                                                                                                                                                                                                                                                               |



 

### <a name="custom-transitions"></a>Transitions personnalisées

Un *interpolateur* définit la fonction mathématique qui détermine la manière dont une variable d’animation change au fil du temps, au fur et à mesure qu’elle progresse de sa valeur initiale à une valeur finale. Chaque transition dans la bibliothèque de transition a un objet d’interpolation associé qui est fourni par le système et implémente la fonction d’interpolation. Si une application requiert un effet qui ne peut pas être spécifié à l’aide de la bibliothèque de transition, elle peut implémenter une ou plusieurs transitions personnalisées en implémentant un objet d’interpolation pour chaque nouvelle transition. Les objets de l’interpolateur ne peuvent pas être utilisés directement par les applications et doivent être encapsulés dans une transition associée. Une *fabrique de transition* est utilisée pour générer des transitions à partir d’un objet d’interpolation. Pour plus d’informations, consultez [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) et [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory) .

Notez que la plupart des applications auront toutes les transitions dont elles ont besoin à l’aide de la bibliothèque de transition et, par conséquent, n’auront pas besoin d’implémenter un interpolateur.

## <a name="storyboards"></a>Storyboards

Une table de montage séquentiel est une collection de transitions appliquées à une ou plusieurs variables d’animation dans le temps. Les transitions dans une table de montage séquentiel sont garanties pour rester synchronisées les unes par rapport aux autres, et la table de montage séquentiel est planifiée ou annulée en tant qu’unité. Après avoir créé les transitions souhaitées, une application crée une table de montage séquentiel à l’aide du gestionnaire d’animations, ajoute les transitions à la table de montage séquentiel, configure le Storyboard de manière appropriée et planifie son exécution le plus rapidement possible. Le gestionnaire d’animations détermine l’heure de début réelle de la table de montage séquentiel, car il peut y avoir des conflits avec d’autres storyboards qui animent actuellement les mêmes variables.

La durée globale d’une table de montage séquentiel dépend des durées des transitions au sein de la table de montage séquentiel. La durée d’une transition n’a pas besoin d’être fixe ; Il peut être déterminé par la valeur et la vélocité des variables animées au début de la transition. Ainsi, la durée d’une table de montage séquentiel peut également dépendre de l’état des variables qu’elle anime.

Les exemples suivants supposent qu’un gestionnaire d’animations, une bibliothèque de transition et un minuteur ont été créés. Pour plus d’informations, consultez [créer les objets d’animation principaux](adding-animation-to-an-application.md). Les exemples supposent également que l’application a créé trois variables d’animation (X, Y et Z) à l’aide de la méthode [**IUIAnimationManager :: CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) et cinq transitions (T1, T2, T3, T4 et T5) à l’aide de l’une des méthodes de l’interface [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary) .

-   [Création d’un Storyboard simple](#building-a-simple-storyboard)
-   [Utilisation d’une durée de Context-Sensitive](#using-a-context-sensitive-duration)
-   [Création d’un Storyboard plus complexe](#building-a-more-complex-storyboard)
-   [Utilisation d’images clés](#using-keyframes)
-   [Conserver les variables](#holding-variables)
-   [Planification d’une table de montage séquentiel](#scheduling-a-storyboard)

### <a name="building-a-simple-storyboard"></a>Création d’un Storyboard simple

Pour générer une table de montage séquentiel simple, utilisez la méthode [**IUIAnimationManager :: CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) pour créer un nouvel Storyboard, la méthode [**IUIAnimationTransitionLibrary :: CreateLinearTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) pour créer une transition linéaire, T1 et la méthode [**IUIAnimationStoryboard :: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) pour appliquer la transition T1 à la variable X et ajouter la transition résultante à la table de montage séquentiel.

Ce processus génère une table de montage séquentiel simple, comme illustré dans la figure suivante. La table de montage séquentiel contient une transition, T1, de telle sorte que la valeur de la variable X change de façon linéaire sur une durée fixe.

![Illustration montrant un Storyboard simple avec une durée fixe](images/simplestoryboardfixedduration.png)

Notez que pour un scénario de ce type simple, une autre option consiste à utiliser la méthode [**IUIAnimationManager :: ScheduleTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition) .

### <a name="using-a-context-sensitive-duration"></a>Utilisation d’une durée de Context-Sensitive

Tandis que certaines transitions ont une durée fixe, la durée des autres dépend de la valeur initiale ou de la rapidité de la variable animée au début de la transition. Par exemple, la méthode [**IUIAnimationTransitionLibrary :: CreateLinearTransitionFromSpeed**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) crée une transition avec une durée proportionnelle à la différence entre la valeur initiale de la variable d’animation et la valeur finale spécifiée. Dans cette illustration, et les autres illustrations, ces transitions avec des durées arbitraires s’affichent avec un point d’interrogation ( ?) et leurs durées réelles sont déterminées lors de la lecture de la table de montage séquentiel.

![Illustration montrant un Storyboard simple avec une durée inconnue](images/simplestoryboardunknownduration.png)

### <a name="building-a-more-complex-storyboard"></a>Création d’un Storyboard plus complexe

Après avoir créé une table de montage séquentiel et ajouté une transition unique, T1, vous pouvez ajouter une deuxième transition pour la variable X en appelant la méthode [**IUIAnimationStoryboard :: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) , mais avec T2 au lieu de T1.

En supposant que la transition T2 ait une durée contextuel, la table de montage séquentiel contient désormais deux transitions d’arrière en arrière de durée arbitraire affectant la variable X.

![Illustration montrant une table de montage séquentiel contenant deux transitions sur la même variable](images/appendingwithaddtransition.png)

L’appel de [**AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) à nouveau avec la variable Y et la transition T3 ajoute une troisième transition au début de la table de montage séquentiel. Selon les valeurs de X et Y lors de la lecture de la table de montage séquentiel, T3 peut se terminer après T1 ou même après T2.

![Illustration montrant une table de montage séquentiel contenant des transitions sur plusieurs variables](images/multivariablestoryboard.png)

### <a name="using-keyframes"></a>Utilisation d’images clés

Pour ajouter une transition à un offset à partir du début de la table de montage séquentiel, vous devez d’abord ajouter une image clé. Les images clés représentent des instantanés dans le temps et n’ont pas d’effet sur le comportement de la table de montage séquentiel. Chaque Storyboard a une image clé implicite qui représente le début de la table de montage séquentiel, la table de montage de l' [**\_ \_ image clé \_ \_**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))de l’animation de l’interface utilisateur. vous pouvez ajouter de nouvelles images clés aux décalages à partir du début en appelant la méthode [**IUIAnimationStoryboard :: AddKeyframeAtOffset**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) avec l' **interface utilisateur de la table de \_ \_ \_ montage séquentiel \_ d’animation**.

Le décalage auquel vous ajoutez une image clé est toujours relatif à une autre image clé. Le diagramme suivant montre le résultat de l’ajout de keyframe1 et de la transition T4, qui est appliqué à la variable Z, alignée avec keyframe1, et créée avec une durée fixe. Bien sûr, étant donné que les durées des autres transitions ne sont pas encore connues, T4 peut ne pas être la dernière transition à se terminer.

![illustration illustrant l’ajout d’une transition alignée sur une image clé](images/addtransitionatkeyframe.png)

Les images clés peuvent également être placées aux extrémités des transitions, à l’aide de la méthode [**IUIAnimationStoryboard :: AddKeyframeAfterTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) . Le diagramme suivant montre le résultat de l’ajout de keyframe2 après T1 et keyframe3 après T2.

![illustration illustrant l’ajout d’images clés après différentes transitions](images/addkeyframeaftertransition.png)

Étant donné que les durées de T1 et T2 ne sont pas connues jusqu’à la lecture de la table de montage séquentiel, les décalages de keyframe2 et keyframe3 ne sont pas non plus déterminés. Par conséquent, keyframe2 et même keyframe3 peuvent se produire avant keyframe1.

Le début et la fin d’une transition peuvent être alignés avec les images clés à l’aide de la méthode [**IUIAnimationStoryboard :: AddTransitionBetweenKeyframes**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) . Le diagramme suivant montre le résultat de l’ajout d’une cinquième transition, T5, sur la variable Y, entre keyframe2 et keyframe3. Cela modifie la durée T5, ce qui la rend plus longue ou plus rapide en fonction des décalages relatifs de keyframe2 et keyframe3.

![Illustration montrant additon d’une transition entre les images clés](images/addtransitionbetweenkeyframes.png)

### <a name="holding-variables"></a>Conserver les variables

Si T4 se termine après T2 et T5, la table de montage séquentiel arrête d’animer les variables X et Y, ce qui les rend disponibles pour les autres storyboards. Toutefois, l’application peut appeler la méthode [**IUIAnimationStoryboard :: HoldVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) pour demander que la table de montage séquentiel contienne une partie ou la totalité des variables qu’elle anime aux valeurs finales jusqu’à ce que la table de montage séquentiel soit terminée. Le diagramme suivant montre le résultat de la conservation de X et de Z lorsque T4 termine la dernière. Notez que la table de montage séquentiel contient X à sa valeur finale jusqu’à ce que la table de montage séquentiel soit terminée. La suspension n’a aucun effet sur Z car le Storyboard se termine lorsque T4 est terminé.

![Illustration montrant la détention de variables aux valeurs finales jusqu’à la fin de la table de montage séquentiel](images/holdvariable.png)

Même si Y n’est pas détenu par ce Storyboard, sa valeur n’est pas modifiée après T5, sauf si une autre table de montage séquentiel l’anime. Étant donné que Y n’est pas détenu, toute autre table de montage séquentiel, quelle que soit la priorité, peut animer Y après la fin de T5. En revanche, étant donné que X est conservé, un Storyboard de priorité inférieure ne peut pas animer X tant que cette table de montage séquentiel n’est pas terminée.

Toutes ces illustrations ont supposé un ensemble arbitraire de valeurs actuelles pour les variables au démarrage de la création de la table de montage séquentiel. Si d’autres valeurs sont rencontrées, les durées des transitions contextuelles sont susceptibles d’être différentes, comme indiqué dans l’illustration suivante.

![Illustration montrant le résultat de la modification des conditions initiales utilisées pour l’illustration précédente](images/holdvariablez.png)

Dans ce scénario, T5 commence avant la fin de T3 et T3 est donc tronqué. Comme T4 termine les versions antérieures à T2 et T5, la valeur de Z est maintenue jusqu’à la fin de la table de montage séquentiel. En général, les valeurs et les rapidités des variables lors du démarrage d’une table de montage séquentiel peuvent affecter le classement des images clés et la longueur et la forme globales de la table de montage séquentiel.

### <a name="scheduling-a-storyboard"></a>Planification d’une table de montage séquentiel

Lors de la planification d’un Storyboard, son heure de début est déterminée par son plan et les contours des storyboards qui sont actuellement dans la planification. Plus précisément, le premier et le dernier moments où le Storyboard anime chaque variable individuelle déterminent si et quand deux storyboards sont en conflit, mais les détails internes des transitions dans ne sont pas importants.

L’illustration suivante montre le plan d’une table de montage séquentiel avec cinq transitions animant trois variables.

![Illustration montrant une table de montage séquentiel avec cinq transitions animant trois variables](images/storyboardwithoutline.png)

L’une des pierres angulaires de la plateforme d’animation Windows est sa prise en charge pour permettre à une animation de se terminer avant qu’une autre ne commence, le cas échéant. Bien que cela élimine de nombreux problèmes logiques, elle introduit également une latence arbitraire dans l’interface utilisateur. Pour résoudre ce cas, les applications peuvent spécifier le délai le plus *long acceptable* pour le démarrage d’une table de montage séquentiel, à l’aide de la méthode [**IUIAnimationStoryboard :: SetLongestAcceptableDelay**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay) , et le gestionnaire d’animations utilise ces informations pour planifier le Storyboard avant l’expiration de la période de latence spécifiée. Lorsqu’une table de montage séquentiel est planifiée, le gestionnaire d’animations détermine si d’autres storyboards doivent d’abord être annulés, supprimés, conclus et/ou compressés.

Une application peut inscrire un gestionnaire qui sera appelé quand l’état d’une table de montage séquentiel change. Cela permet à l’application de répondre lorsque la création de la table de montage séquentiel démarre, s’exécute jusqu’à son achèvement, est entièrement supprimée de la planification ou ne peut pas se terminer en raison d’une interruption par un Storyboard de priorité plus élevée. Pour identifier les storyboards passés aux gestionnaires d’événements de Storyboard (ou comparaisons de priorité), une application peut utiliser la méthode [**IUIAnimationStoryboard :: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) pour appliquer des balises aux storyboards, similaires à celles qui peuvent être utilisées pour identifier des variables. Comme pour la réutilisation des storyboards, les développeurs doivent faire preuve de prudence lors de l’utilisation de balises pour identifier les storyboards, et vous assurer que les ambiguïtés ne se produisent pas lorsque des actions de l’utilisateur entraînent la mise en file d’attente de plusieurs storyboards.

Les exemples suivants illustrent deux variantes d’une tentative de planification de la table de montage séquentiel générée dans les sections précédentes de cette rubrique.

Dans ce scénario, six storyboards, A à F, ont déjà été planifiés pour animer les variables W, X, Y et Z, mais seuls A et B commencent à être joués. Le nouveau Storyboard, étiqueté G, a son délai le plus long acceptable défini sur la durée indiquée dans l’illustration suivante.

![illustration illustrant l’ajout d’un nouveau Storyboard à la planification existante](images/existingschedule1withlines.png)

L’application a enregistré des comparaisons de priorité qui incluent la logique suivante :

-   G peut annuler uniquement C et E, et uniquement pour empêcher l’échec.
-   G peut uniquement supprimer A, C, E et F et uniquement pour empêcher l’échec.
-   Tout Storyboard peut compresser n’importe quel autre Storyboard (la compression est toujours effectuée uniquement pour éviter les défaillances).

> [!Note]  
> Le qualificateur « uniquement pour empêcher une défaillance » signifie que les comparaisons de priorité inscrites retournent la \_ valeur S OK uniquement lorsque le paramètre *priorityEffect* est l’effet de priorité d’animation de l' **interface utilisateur \_ \_ \_ \_**. Pour plus d’informations, consultez la méthode [**IUIAnimationPriorityComparison :: HasPriority**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority) .

 

Pour démarrer G avant l’expiration du délai le plus long, le gestionnaire d’animations doit effectuer les opérations suivantes :

-   Trim F
-   Annuler E

Quand E est annulé, D et F sont découverts et reprennent leurs contours originaux :

![Illustration montrant des contours originaux](images/existingschedule1bwithlines.png)

Le gestionnaire d’animations n’a pas besoin d’annuler ou de découper C à planifier avant que son délai acceptable le plus long ne s’est écoulé, de sorte que la réunion de C et G détermine le moment où G démarre.

![Illustration montrant que f est tronqué pour permettre à c et à g de répondre](images/schedule1withgwithlines.png)

Une fois la planification de G terminée, les durées de ses transitions peuvent être déterminées et le reste de son contour est donc connu. Toutefois, le plan peut changer si une autre table de montage séquentiel est ensuite supprimée de la planification.

En guise de deuxième exemple, considérez un scénario comme celui ci-dessus, mais avec un délai plus long acceptable spécifié pour G.

![Illustration montrant le scénario précédent, mais avec un délai plus long acceptable pour g](images/existingschedule2withlines.png)

Dans ce cas, les actions suivantes sont effectuées :

-   Trim F
-   Annuler E
-   Annuler C

En outre, le gestionnaire d’animations doit compresser D par la quantité indiquée pour permettre à G de démarrer après son délai le plus long et non plus tard.

![Illustration montrant où d doit être compressé pour permettre à g de démarrer à son délai acceptable le plus long](images/trimmedandcancelledwithlines.png)

Pour conserver leur minutage relatif, A, B et F sont également compressés.

![Illustration montrant a, b, d et f compressés](images/schedule2withgwithlines.png)

Toutefois, les storyboards sur des variables non liées (non affichées) ne sont pas compressés.

Là encore, la structure de G est maintenant connue et est différente du résultat dans le premier scénario, car les variables ont des valeurs différentes lorsque G commence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationPriorityComparison**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)
</dt> <dt>

[**IUIAnimationStoryboard**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> </dl>

 

