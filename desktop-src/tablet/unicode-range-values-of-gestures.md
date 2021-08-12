---
description: 'Lors de l’implémentation de votre propre module de reconnaissance de mouvement Microsoft, vous devez définir le nom et la valeur de plage Unicode pour tout mouvement que votre module de reconnaissance doit reconnaître. Si vous décidez d’implémenter les mouvements déjà pris en charge ou définis dans le cadre du module de reconnaissance de mouvement Microsoft, utilisez les noms définis et les valeurs de plage Unicode pour ces mouvements. L’intégralité de la collection de noms et de valeurs de plage Unicode pour les gestes implémentés et non implémentés dans le module de reconnaissance de mouvement Microsoft est fournie dans le fichier d’en-tête Recdefs. h (installé par défaut dans C : \\ Program Files \\ Microsoft Tablet PC Platform SDK \\ include). Les noms des mouvements et les valeurs de la plage Unicode sont également répertoriés dans les tableaux suivants. Notez que le geste de mouvement \_ null est utilisé pour indiquer qu’un module de reconnaissance ne reconnaît pas l’entrée comme un geste.'
ms.assetid: 931fc69a-1f7a-492c-8158-0691cd2fe57a
title: Valeurs de plage Unicode des mouvements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f96c1f59ea9e53d63999c01db73c45080f205bccf043e26463563b0f1f6af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449222"
---
# <a name="unicode-range-values-of-gestures"></a>Valeurs de plage Unicode des mouvements

Lors de l’implémentation de votre propre module de reconnaissance de mouvement Microsoft, vous devez définir le nom et la valeur de plage Unicode pour tout mouvement que votre module de reconnaissance doit reconnaître.

Si vous décidez d’implémenter les mouvements déjà pris en charge ou définis dans le cadre du module de reconnaissance de mouvement Microsoft, utilisez les noms définis et les valeurs de plage Unicode pour ces mouvements. L’intégralité de la collection de noms et de valeurs de plage Unicode pour les gestes implémentés et non implémentés dans le module de reconnaissance de mouvement Microsoft est fournie dans le fichier d’en-tête Recdefs. h (installé par défaut dans C : \\ Program Files \\ Microsoft Tablet PC Platform SDK \\ include). Les noms des mouvements et les valeurs de la plage Unicode sont également répertoriés dans les tableaux suivants.

> [!Note]  
> Le geste de mouvement \_ null est utilisé pour indiquer qu’un module de reconnaissance ne reconnaît pas l’entrée comme un geste.

 

## <a name="implemented-gestures"></a>Mouvements implémentés



| Nom du geste                          | Valeur de plage Unicode |
|---------------------------------------|---------------------|
| GESTE \_ null<br/>              | 0xF000<br/>   |
| MOUVEMENT \_ SCRATCHOUT<br/>        | 0xf001<br/>   |
| TRIANGLE de mouvement \_<br/>          | 0xf002<br/>   |
| carré de geste \_<br/>            | 0xf003<br/>   |
| étoile de mouvement \_<br/>              | 0xf004<br/>   |
| vérification du geste \_<br/>             | 0xf005<br/>   |
| MOUVEMENT \_ fioriture<br/>          | 0xf010<br/>   |
| MOUVEMENT \_ double \_ fioriture<br/>  | 0xf011<br/>   |
| cercle de mouvement \_<br/>            | 0xf020<br/>   |
| \_double \_ cercle de mouvement<br/>    | 0xf021<br/>   |
| MOUVEMENT \_ demi-cercle \_ gauche<br/>  | 0xf028<br/>   |
| \_demi-cercle \_ droit<br/> | 0xf029<br/>   |
| \_Chevron \_ vers le haut<br/>       | 0xf030<br/>   |
| \_Chevron \_ vers le dessous<br/>     | 0xf031<br/>   |
| \_Chevron \_ gauche<br/>     | 0xf032<br/>   |
| \_Chevron \_ droit<br/>    | 0xf033<br/>   |
| flèche de mouvement \_ vers le \_ haut<br/>         | 0xf038<br/>   |
| \_flèche \_ vers le bas<br/>       | 0xf039<br/>   |
| flèche de mouvement \_ vers la \_ gauche<br/>       | 0xf03a<br/>   |
| flèche de mouvement \_ vers la \_ droite<br/>      | 0xf03b<br/>   |
| GESTE \_ vers le haut<br/>                | 0xf058<br/>   |
| GESTE \_ vers le dessous<br/>              | 0xf059<br/>   |
| GESTE vers la \_ gauche<br/>              | 0xf05a<br/>   |
| GESTE vers la \_ droite<br/>             | 0xf05b<br/>   |
| \_monter \_ le geste<br/>          | 0xf060<br/>   |
| GESTE \_ vers le \_ haut<br/>          | 0xf061<br/>   |
| MOUVEMENT vers la \_ gauche à \_ droite<br/>       | 0xf062<br/>   |
| GESTE à \_ droite à \_ gauche<br/>       | 0xf063<br/>   |
| MOUVEMENT \_ vers la gauche en haut \_ \_<br/>    | 0xf064<br/>   |
| GESTE en \_ haut à \_ droite \_<br/>   | 0xf065<br/>   |
| MOUVEMENT \_ vers la gauche vers le \_ gauche \_<br/>  | 0xf066<br/>   |
| GESTE \_ vers le long de la partie \_ droite \_<br/> | 0xf067<br/>   |
| GESTE \_ vers le haut à \_ gauche<br/>          | 0xf068<br/>   |
| GESTE \_ vers \_ le haut<br/>         | 0xf069<br/>   |
| GESTE \_ vers le \_ gauche<br/>        | 0xf06a<br/>   |
| GESTE \_ vers le \_ droite<br/>       | 0xf06b<br/>   |
| GESTE \_ \_ vers le haut<br/>          | 0xf06c<br/>   |
| GESTE \_ \_ vers le gauche<br/>        | 0xf06d<br/>   |
| GESTE \_ \_ vers le haut<br/>         | 0xf06e<br/>   |
| GESTE \_ vers le droite \_<br/>       | 0xf06f<br/>   |
| point d’exclamation de mouvement \_<br/>       | 0xf0a4<br/>   |
| robinet de geste \_<br/>               | 0xf0f0<br/>   |
| \_double- \_ clic de mouvement<br/>       | 0xf0f1<br/>   |



 

## <a name="unimplemented-gestures"></a>Mouvements non implémentés



| Nom du geste                             | Valeur de plage Unicode |
|------------------------------------------|---------------------|
| infini de mouvement \_<br/>             | 0xf006<br/>   |
| Croix de mouvement \_<br/>                | 0xf007<br/>   |
| paragraphe de mouvement \_<br/>            | 0xf008<br/>   |
| SECTION de mouvement \_<br/>              | 0xf009<br/>   |
| \_puce geste<br/>               | 0xf00a<br/>   |
| Croix du geste \_ \_<br/>        | 0xf00b<br/>   |
| tilde de mouvement \_<br/>             | 0xf00c<br/>   |
| échange de mouvement \_<br/>                 | 0xf00d<br/>   |
| MOUVEMENT \_ OPENUP<br/>               | 0xf00e<br/>   |
| MOUVEMENT \_ gros plan<br/>              | 0xf00f<br/>   |
| Rectangle de mouvement \_<br/>            | 0xf012<br/>   |
| robinet de mouvement \_ circulaire \_<br/>          | 0xf022<br/>   |
| \_cercle du cercle de mouvement \_<br/>       | 0xf023<br/>   |
| \_Croix du cercle de mouvement \_<br/>        | 0xf025<br/>   |
| ligne de cercle de mouvement \_ \_ \_ vert<br/>   | 0xf026<br/>   |
| trait de cercle de mouvement \_ \_ \_ Horiz<br/>   | 0xf027<br/>   |
| \_double \_ flèche vers le \_ haut<br/>    | 0xf03c<br/>   |
| \_double \_ flèche \_ vers le bas du geste<br/>  | 0xf03d<br/>   |
| \_double flèche de mouvement \_ vers la \_ gauche<br/>  | 0xf03e<br/>   |
| \_double flèche de mouvement \_ vers la \_ droite<br/> | 0xf03f<br/>   |
| flèche vers le \_ haut à \_ \_ gauche<br/>      | 0xf040<br/>   |
| \_flèche vers \_ le haut à \_ droite<br/>     | 0xf041<br/>   |
| \_flèche bas de geste vers la \_ \_ gauche<br/>    | 0xf042<br/>   |
| \_flèche bas de geste vers la \_ \_ droite<br/>   | 0xf043<br/>   |
| flèche gauche du geste vers le \_ \_ \_ haut<br/>      | 0xf044<br/>   |
| \_flèche gauche du geste \_ \_ vers le bas<br/>    | 0xf045<br/>   |
| \_flèche droite \_ vers le \_ haut<br/>     | 0xf046<br/>   |
| \_flèche droite de mouvement \_ vers le \_ bas<br/>   | 0xf047<br/>   |
| \_LEFTUP Diagonal des mouvements \_<br/>     | 0xf05c<br/>   |
| \_RIGHTUP Diagonal des mouvements \_<br/>    | 0xf05d<br/>   |
| \_LEFTDOWN Diagonal des mouvements \_<br/>   | 0xf05e<br/>   |
| \_RIGHTDOWN Diagonal des mouvements \_<br/>  | 0xf05f<br/>   |
| \_lettre \_ de mouvement A<br/>            | 0xf080<br/>   |
| lettre de mouvement \_ \_ B<br/>            | 0xf081<br/>   |
| lettre de mouvement \_ \_ C<br/>            | 0xf082<br/>   |
| lettre de mouvement \_ \_ D<br/>            | 0xf083<br/>   |
| lettre de mouvement \_ \_ E<br/>            | 0xf084<br/>   |
| lettre de mouvement \_ \_ F<br/>            | 0xf085<br/>   |
| lettre de mouvement \_ \_ G<br/>            | 0xf086<br/>   |
| lettre de mouvement \_ \_ H<br/>            | 0xf087<br/>   |
| Lettre du geste \_ \_ I<br/>            | 0xf088<br/>   |
| lettre de mouvement \_ \_ J<br/>            | 0xf089<br/>   |
| lettre de mouvement \_ \_ K<br/>            | 0xf08a<br/>   |
| lettre de mouvement \_ \_ L<br/>            | 0xf08b<br/>   |
| lettre de mouvement \_ \_ M<br/>            | 0xf08c<br/>   |
| lettre de mouvement \_ \_ N<br/>            | 0xf08d<br/>   |
| Lettre du geste \_ \_ O<br/>            | 0xf08e<br/>   |
| lettre de mouvement \_ \_ P<br/>            | 0xf08f<br/>   |
| lettre de mouvement \_ \_ Q<br/>            | 0xf090<br/>   |
| lettre de mouvement \_ \_ R<br/>            | 0xf091<br/>   |
| lettre de mouvement \_ \_ S<br/>            | 0xf092<br/>   |
| lettre de mouvement \_ \_ T<br/>            | 0xf093<br/>   |
| lettre de mouvement \_ \_ U<br/>            | 0xf094<br/>   |
| lettre de mouvement \_ \_ V<br/>            | 0xf095<br/>   |
| lettre de mouvement \_ \_ W<br/>            | 0xf096<br/>   |
| lettre de mouvement \_ \_ X<br/>            | 0xf097<br/>   |
| lettre de mouvement \_ \_ Y<br/>            | 0xf098<br/>   |
| lettre de mouvement \_ \_ Z<br/>            | 0xf099<br/>   |
| Chiffre de mouvement \_ \_ 0<br/>             | 0xf09a<br/>   |
| Chiffre du geste \_ \_ 1<br/>             | 0xf09b<br/>   |
| Chiffre de mouvement \_ \_ 2<br/>             | 0xf09c<br/>   |
| Chiffre de mouvement \_ \_ 3<br/>             | 0xf09d<br/>   |
| Chiffre de mouvement \_ \_ 4<br/>             | 0xf09e<br/>   |
| Chiffre de mouvement \_ \_ 5<br/>             | 0xf09f<br/>   |
| Chiffre de mouvement \_ \_ 6<br/>             | 0xf0a0<br/>   |
| Chiffre de mouvement \_ \_ 7<br/>             | 0xf0a1<br/>   |
| Chiffre de mouvement \_ \_ 8<br/>             | 0xf0a2<br/>   |
| Chiffre de mouvement \_ \_ 9<br/>             | 0xf0a3<br/>   |
| QUESTION de mouvement \_<br/>             | 0xf0a5<br/>   |
| MOUVEMENT \_ dièse<br/>                | 0xf0a6<br/>   |
| MOUVEMENT en \_ dollars<br/>               | 0xf0a7<br/>   |
| \_astérisque geste<br/>             | 0xf0a8<br/>   |
| GESTE \_ plus<br/>                 | 0xf0a9<br/>   |
| \_double \_ vers le haut<br/>           | 0xf0b8<br/>   |
| \_double \_ vers le « geste »<br/>         | 0xf0b9<br/>   |
| GESTE \_ double \_ gauche<br/>         | 0xf0ba<br/>   |
| MOUVEMENT \_ double \_ droit<br/>        | 0xf0bb<br/>   |
| \_tripler le geste \_<br/>           | 0xf0bc<br/>   |
| \_tripler du geste \_<br/>         | 0xf0bd<br/>   |
| MOUVEMENT \_ triple \_ gauche<br/>         | 0xf0be<br/>   |
| \_triple \_ droit de mouvement<br/>        | 0xf0bf<br/>   |
| crochet de geste \_ \_ sur<br/>        | 0xf0e4<br/>   |
| crochet de geste \_ \_ sous<br/>       | 0xf0e5<br/>   |
| \_crochet \_ gauche<br/>        | 0xf0e6<br/>   |
| crochet de geste vers la \_ \_ droite<br/>       | 0xf0e7<br/>   |
| \_accolade de geste \_ sur<br/>          | 0xf0e8<br/>   |
| \_accolade de geste \_ sous<br/>         | 0xf0e9<br/>   |
| \_accolade \_ gauche<br/>          | 0xf0ea<br/>   |
| crochet de geste vers la \_ \_ droite<br/>         | 0xf0eb<br/>   |
| \_triple \_ Tap du geste<br/>          | 0xf0f2<br/>   |
| \_robinet à quadruple \_ pression<br/>            | 0xf0f3<br/>   |



 

 

 




