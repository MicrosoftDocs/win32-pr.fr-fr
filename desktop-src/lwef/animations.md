---
title: Animations
description: Animations
ms.assetid: 8bd9ac94-3f86-4168-bf33-7a2c8d11907d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf1b9f5e8daa320390f5c19c3c4c27cb8195a8fe
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104562024"
---
# <a name="animations"></a>Animations

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Les animations d’un caractère reflètent son sexe, son âge, son personnalité et son comportement. Le nombre et les types d’animations que vous créez pour un caractère dépendent de ce que fait votre caractère et de la façon dont il répond à différentes situations.

Comme les animations traditionnelles, les animations numériques impliquent la création d’une série d’images légèrement différentes qui, lorsqu’elles sont affichées de façon séquentielle, fournissent l’illusion de l’action. La création d’images d’animation de haute qualité peut nécessiter un animateur expérimenté, mais le style et la présentation du caractère que vous créez affectent également la qualité. Les caractères à deux dimensions avec des formes et des caractéristiques simples peuvent parfois être aussi efficaces que les caractères très rendus (ou plus efficaces que). Il n’est pas nécessaire de créer une image réaliste pour présenter un caractère effectif. De nombreux caractères animés populaires ne sont pas réalistes dans leur présentation, mais ils sont efficaces, car l’animateur comprend comment transmettre des actions et des émotions. L’annexe fournit des informations générales sur les principes fondamentaux de conception d’animations.

### <a name="frames"></a>Frame

Chaque animation que vous créez pour un caractère Microsoft Agent est composée d’une séquence temporelle de frames. Chaque image de l’animation est composée d’une ou de plusieurs images bitmap. Les images peuvent être aussi petites que vous en avez besoin ou aussi volumineuses que le frame lui-même.

Les détails de l’animation, tels que le clignotement oculaire ou le mouvement du doigt, peuvent être inclus en tant qu’images supplémentaires pour le cadre. Vous pouvez superposer plusieurs images pour créer un composite et faire varier sa position dans les couches. Cette technique vous permet de réutiliser des images dans plusieurs frames et de faire varier les détails qui changent. Par exemple, si vous souhaitez avoir une vague de caractères, pour chaque image, vous pouvez utiliser une image de base avec tout sauf la main et superposer l’image de base avec une autre image. De même, si vous souhaitez faire clignoter le caractère, vous pouvez superposer un autre jeu d’yeux sur une image de base pour chaque image. Les images peuvent également être décalées à partir de l’image de base. Toutefois, seule la partie de l’image qui existe dans la taille du cadre sera affichée.

Vous pouvez avoir autant de frames que vous le souhaitez dans une animation. Toutefois, une animation classique a une moyenne de 14 frames afin qu’elle ne soit pas plus de six secondes. Cette durée modeste garantit que votre caractère semble réactif à l’entrée utilisateur. En outre, plus le nombre de frames est élevé, plus votre fichier d’animation est grand. Pour les caractères Web téléchargés, conservez la taille de votre fichier d’animation le plus petit possible tout en fournissant un jeu de frames de taille raisonnable, afin que l’animation du caractère n’apparaisse pas saccadée.

### <a name="image-design"></a>Conception d’image

Vous pouvez utiliser n’importe quel outil graphique ou d’animation pour créer des images pour les images d’animation, à condition que vous stockiez les images finales dans le bitmap Windows (. BMP). Une fois les images créées, utilisez l’éditeur de caractères Microsoft Agent (disponible dans le [téléchargeable](https://www.microsoft.com/download/en/details.aspx?id=14765)) pour assembler, séquencer et créer des images, fournir d’autres informations sur les caractères et compiler toutes les informations dans un fichier de caractères final.

Les images de caractères doivent être conçues pour une palette de couleurs de 256, ce qui permet de conserver les 20 couleurs système Windows standard dans leur position standard dans la palette (les 10 premières et les 10 dernières positions). Cela signifie que la palette de couleurs de votre caractère peut utiliser les couleurs système standard et jusqu’à 236 autres couleurs. Lorsque vous définissez votre palette, incluez toutes les propriétés utilisées par votre caractère dans l’animation. Si la palette de votre caractère place des couleurs dans les positions de couleur système, ces couleurs de caractères seront remplacées par les couleurs système lorsque Microsoft Agent créera la palette.

Plus le nombre de couleurs que vous utilisez dans la palette de couleurs d’un caractère est élevé, plus il est possible qu’une partie des couleurs de votre caractère soit remappée pour les systèmes configurés sur un paramètre de couleur 8 bits (256). Tenez également compte de l’utilisation de la palette de l’application dans laquelle le caractère sera utilisé. Il est préférable d’éviter que les caractères remappent les couleurs de l’application hôte et vice-versa. De même, si vous envisagez de prendre en charge plusieurs caractères affichés en même temps, vous souhaiterez probablement conserver une palette cohérente pour ces caractères. Vous pouvez envisager d’utiliser uniquement les couleurs système standard dans votre caractère si vous ciblez les utilisateurs avec une configuration de couleur de 8 bits. Toutefois, cela peut toujours empêcher le remappage de la couleur de votre caractère si une autre application redéfinit largement la palette de couleurs. Sur les systèmes dotés de résolutions de couleurs supérieures, le remappage de palette de couleurs ne doit pas être un problème, car le système gère automatiquement les palettes de couleurs.

L’utilisation d’un plus grand nombre de couleurs dans une image peut également augmenter la taille globale de votre fichier d’animation. Le nombre de couleurs et la fréquence de variation peuvent déterminer le degré de compression de vos fichiers de caractères. Par exemple, un caractère à deux dimensions qui utilise uniquement quelques couleurs sera mieux compressé qu’un caractère à trois dimensions, ombré.

Vous devez utiliser la même palette de couleurs pour l’ensemble de votre fichier de caractères. Vous ne pouvez pas modifier la palette pour différentes animations. Si vous tentez de prendre en charge des configurations de couleur de 8 bits, envisagez d’utiliser la même palette pour votre application et les autres caractères que vous envisagez de prendre en charge.

La 11<sup>ième</sup> position dans la palette est définie par défaut comme couleur de transparence (ou alpha), même si vous pouvez également définir la couleur à l’aide de l’éditeur de caractères Microsoft Agent. Les services d’animation Microsoft Agent s’affichent en toute transparence sur tous les pixels de cette couleur. par conséquent, utilisez la couleur de vos images uniquement lorsque vous souhaitez la transparence.

Examinez attentivement la forme de votre caractère, car cela peut affecter les performances de l’animation. Pour afficher le caractère, les services d’animation créent une fenêtre de région basée sur l’image globale. Les petites zones irrégulières nécessitent souvent davantage de données de région et peuvent réduire les performances de votre caractère d’animation. Par conséquent, dans la mesure du possible, évitez les espaces, les éléments et les détails d’un seul pixel.

Évitez l’anticrénelage du bord extérieur de votre caractère. Bien que l’anticrénelage soit une bonne technique pour réduire les bords dentelés, il est basé sur des couleurs adjacentes. Étant donné que votre caractère peut apparaître au-dessus d’une variété de couleurs, l’anticrénelage du bord extérieur peut faire apparaître un caractère médiocre sur les autres arrière-plans. Toutefois, vous pouvez utiliser l’anticrénelage des détails internes de votre caractère sans rencontrer ce problème.

### <a name="frame-size"></a>Taille de trame

La taille de l’image ne doit généralement pas dépasser 128 x 128 pixels. Bien que les caractères puissent être plus grands ou plus petits dans les deux dimensions, l’éditeur de caractères Microsoft Agent l’utilise comme taille d’affichage et met à l’échelle les images de caractères si vous définissez une taille de frame supérieure. La taille de la trame 128 x 128 permet d’effectuer des compromis raisonnables avec l’espace occupé par le caractère sur l’écran. Votre application peut mettre à l’échelle un caractère au moment de l’exécution.

### <a name="frame-duration"></a>Durée de la trame

Vous pouvez utiliser l’éditeur de caractères Microsoft Agent pour définir la durée d’affichage de chaque image de l’animation avant de passer au frame suivant. Définir la durée de chaque cadre sur au moins 10 centièmes de seconde (10 images par seconde)--tout ce qui est moins peut ne pas être perceptible sur certains systèmes. Vous pouvez également définir une durée plus longue, mais évitez les pauses non naturelles dans l’action.

L’éditeur de caractères Microsoft agent prend également en charge la branchement d’une image d’une animation vers une autre, en fonction des pourcentages de probabilité que vous fournissez. Pour tout Frame donné, vous pouvez définir jusqu’à trois branches différentes. La création de branche vous permet de créer des animations qui varient quand elles sont lues et les animations qui bouclent. Toutefois, soyez prudent lors de l’utilisation de la création de branche, car cela peut créer des problèmes quand vous tentez de lire une animation après une autre. Par exemple, si vous jouez une animation de boucle ou de création de branche, elle peut continuer indéfiniment, sauf si vous utilisez une méthode [**Stop**](stop-method.md) . Si vous n’êtes pas certain, évitez de créer des branchements.

Les frames qui n’ont pas d’images et qui sont définis sur une durée de zéro n’apparaissent pas lorsqu’ils sont inclus dans une animation. Vous pouvez utiliser cette fonctionnalité pour créer des frames qui prennent en charge la création de branche sans être visibles. Toutefois, un frame qui n’a pas encore d’images a une durée supérieure à zéro s’affiche. Par conséquent, évitez d’inclure des frames vides dans votre animation, car l’utilisateur peut ne pas être en mesure de distinguer un frame vide de lorsque le caractère est masqué.

### <a name="frame-transition"></a>Transition de frame

Lors de la conception d’une animation, réfléchissez à la façon de passer en douceur de et vers l’animation. Par exemple, si vous créez une animation dans laquelle les gestes de caractère se trouvent à droite, et une autre dans laquelle les mouvements de caractères restants, vous souhaitez que le caractère s’anime facilement d’une position à l’autre. Bien que vous puissiez la créer dans l’une ou l’autre des animations, une meilleure solution consiste à définir une position neutre ou transitoire à partir de laquelle le caractère démarre et retourne. L’animation vers la position neutre peut être incorporée dans le cadre de chaque animation ou sous la forme d’une animation distincte. Dans l’éditeur de caractères Microsoft Agent, vous pouvez spécifier une animation de **retour** complémentaire pour chaque animation pour votre caractère. L’animation de **retour** ne doit généralement pas dépasser 2-4 frames, de sorte que le caractère peut passer rapidement à la position neutre.

Par exemple, à l’aide du scénario « gesturing Right, gesturing Left », vous pouvez créer une animation **GestureRight** , en commençant par un frame où le caractère apparaît dans une position neutre et ajouter des frames avec des images qui étendent la main du caractère vers la droite. Ensuite, créez son animation de **retour** : une animation complémentaire avec des images qui retournent le caractère à sa position neutre. Vous pouvez l’assigner comme animation de retour pour l’animation **GestureRight** . Ensuite, créez l’animation **GestureLeft** qui démarre à partir de la position neutre et étend le bras du caractère vers la gauche. Enfin, créez également une animation de **retour** complémentaire pour cette animation. Une animation de **retour** commence généralement par une image qui suit la dernière image de l’animation précédente.

Le démarrage et le retour à la même position neutre, que ce soit dans une animation ou à l’aide d’une animation de retour, vous permet de lire n’importe quelle animation dans n’importe quel ordre. Les services d’animation Microsoft Agent lisent automatiquement votre animation de retour désignée dans de nombreux cas. Par exemple, les services jouent l’animation de **retour** indiquée avant de lire les animations d’État ralenti de votre caractère. Il est judicieux de définir et d’assigner des animations de **retour** si vos animations ne se terminent pas encore à la position neutre.

Si vous souhaitez fournir vos propres transitions entre des animations spécifiques ; par exemple, étant donné que vous les lisez toujours dans un ordre bien défini, vous pouvez éviter de définir des animations de **retour** . Toutefois, il est toujours judicieux de commencer et de terminer la séquence d’animations à partir de la position neutre.

### <a name="speaking-animation"></a>Animation orale

Fournissez des images de bouche pour chaque animation pendant laquelle vous souhaitez que le caractère soit en mesure de parler, sauf si la conception de votre caractère n’a pas de bouche animée ou d’indication de sortie parlée. En général, le mouvement bouche est très important. Un personnage peut apparaître moins intelligent, Likable ou honnête si le mouvement de la bouche n’est pas raisonnablement synchronisé avec sa parole. Les images de bouche permettent de synchroniser votre caractère avec une sortie parlée. Vous définissez des images de bouche séparément et en tant que fichiers bitmap Windows. Ils doivent correspondre à la même palette de couleurs que les autres images de votre animation.

Les services d’animation de l’agent Microsoft affichent des images d’animation de la bouche en haut de la dernière image d’une animation, également appelée *cadre de parole* de l’animation. Par exemple, lorsque le caractère parle de l’animation **GestureRight** , les services d’animation chevauchent les images de l’animation bouche sur la dernière image de **GestureRight**. Un caractère ne peut pas parler lors de l’animation. vous ne devez donc fournir des images de bouche que pour la dernière image d’une animation. En outre, le cadre de conversation doit être le cadre de fin d’une animation, de sorte qu’un caractère ne peut pas parler dans une animation de bouclage.

En général, vous fournissez les images de la bouche dans la même taille que le cadre (et l’image de base), mais incluez uniquement la zone qui s’anime dans le mouvement de la bouche, puis affichez le reste de l’image dans la couleur transparente. Concevez l’image de façon à ce qu’elle corresponde à l’image dans le cadre de discours lorsqu’elle est superposée. Pour qu’il corresponde correctement, il est probable que vous deviez créer un ensemble distinct d’images de bouche pour chaque animation dans laquelle le personnage parle.

Une image bouche peut inclure plus que la bouche elle-même, telle que l’menton ou d’autres parties du corps du caractère pendant qu’elle parle. Toutefois, si vous déplacez une main ou une jambe, Notez qu’elle peut sembler se déplacer de façon aléatoire, car la façade bouche affichée sera basée sur le phonème actuel d’une expression parlée. En outre, le serveur découpe l’image bouche sur le contour de l’image de l’image de parole. Concevez votre image de recouvrement de l’embouchure pour rester dans le contour de son image de l’image de base, car le serveur utilise l’image de base pour créer la limite de la fenêtre pour le caractère.

L’éditeur de caractères Microsoft agent vous permet de définir sept positions de base qui correspondent à des formes de bouche courantes, présentées dans le tableau suivant :

**Images d’animation bouche**



| Position de la bouche | Exemple d’image                       | Représentation                                                                                                                     |
|----------------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Fermés         | :::image type="icon" source="images/g07ci01.gif":::<br/> | Forme bouche fermée normale. Également utilisé pour les phonèmes tels que « m » comme dans « MOM », « b » comme dans « Bob », « f », comme dans « Fife ».<br/>           |
| Open-élargi 1    | :::image type="icon" source="images/g07ci02.gif":::<br/> | La bouche est légèrement ouverte, à pleine chasse. Utilisé pour les phonèmes, tels que « g », comme dans « gag », « l » comme dans « accalmie », « Ear » comme dans « entendre ».<br/> |
| Open-élargi 2    | :::image type="icon" source="images/g07ci03.gif":::<br/> | La bouche est partiellement ouverte, à pleine chasse. Utilisé pour les phonèmes, tels que « n », comme dans « Noun », « d » comme dans « Dad », « t » comme dans « total ».<br/>    |
| Open-élargi 3    | :::image type="icon" source="images/g07ci04.gif":::<br/> | La bouche est ouverte, à pleine chasse. Utilisé pour les phonèmes, tels que « u », comme dans « arrêter », « EA » comme dans « Head », « Your » comme dans « blessés ».<br/>          |
| Open-élargi 4    | :::image type="icon" source="images/g07ci05.gif":::<br/> | La bouche est entièrement ouverte, à pleine chasse. Utilisé pour les phonèmes, tels que « a », comme dans « chapeau », comme dans « Comment ».<br/>                   |
| Ouvert-moyen    | :::image type="icon" source="images/g07ci06.gif":::<br/> | La bouche est ouverte à demi-chasse. Utilisé pour les phonèmes, tels que « Oy », comme dans « Ahoy », « o » comme dans « Hot ».<br/>                              |
| Ouvert-étroit    | :::image type="icon" source="images/g07ci07.gif":::<br/> | La bouche est ouverte à une largeur étroite. Utilisé pour les phonèmes, tels que « o », comme dans « cerceau », « o » comme dans « espoir », « w » comme dans « mouillé ».<br/>           |



 

 

 





