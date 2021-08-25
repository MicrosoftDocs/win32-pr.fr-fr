---
title: Conditions préalables pour le développement avec DirectX
description: lorsque vous commencez à développer une application Windows à l’aide de DirectX, gardez à l’esprit les conditions préalables de cette page. Cela comprend les technologies que vous devez connaître avant de vous plonger dans.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- Application DirectX, conditions préalables
- application DirectX, application Windows Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c575fc24da5632582e30b9786d8c800161e5ad1a1cfbc765aa5ec33db3f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950989"
---
# <a name="prerequisites-for-developing-with-directx"></a>Conditions préalables pour le développement avec DirectX

lorsque vous commencez à développer une application Windows à l’aide de DirectX, gardez à l’esprit les conditions préalables de cette page. Cela comprend les technologies que vous devez connaître avant de vous plonger dans.

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a>que dois-je savoir pour développer un jeu de Windows à l’aide de DirectX ?

avant de commencer à développer une application Windows Store à l’aide de DirectX, vous devez savoir comment programmer dans Windows avec C++. les applications Windows à l’aide de DirectX sont développées à un faible niveau de programmation, ce qui signifie que vous serez exposé à de nombreuses fonctionnalités du système d’exploitation. Il s’agit notamment de la gestion de la mémoire et des ressources, ainsi que de l’interface du périphérique graphique lui-même. Si vous débutez avec le développement d’applications de jeux ou graphiques, cette opération peut s’avérer difficile. Mais vous y trouverez également une récompense, car le développement de jeux à ce niveau crée des possibilités bien supérieures pour la conception et le développement d’applications graphiques et de jeux.

Vous devez également comprendre les principes fondamentaux de la programmation et des mathématiques graphiques 2D et 3D, car la plupart des API que vous utiliserez ont été développées avec ces principes à l’esprit. Il est plus facile de comprendre les paramètres et les résultats si vous êtes familiarisé avec les opérations qui en dépendent.

Au minimum, vous devez comprendre les éléments suivants :

-   Windows Programmation C/C++. Cela signifie que vous comprenez les pointeurs et les références, les événements et les rappels, et peut-être quelques bibliothèques communes comme ATL.
-   Programmation Win32. Vous comprenez comment les fenêtres sont créées et comment les événements d’interface utilisateur sont traités. Vous comprenez également un peu les API COM et Win32 essentielles.
-   Algébrique et trigonométrie linéaires. Bien que ce ne soit pas essentiel, vous aurez plus de temps si vous êtes familiarisé avec les concepts de ces deux disciplines mathématiques, car ils constituent la base d’une grande partie de la programmation de graphiques 3D.
-   La terminologie et les concepts graphiques de base, tels que les bitmaps, les textures, les vertex, les mailles et les fenêtres d’affichage.

## <a name="what-does-directx-provide-me"></a>Qu’est-ce que DirectX me permet ?

DirectX est l’ensemble principal d’api graphiques que vous allez utiliser pour développer des jeux Windows. Voici les catégories de fonctionnalités que vous devez connaître lorsque vous décidez du développement de votre jeu.



| Bibliothèque     | Description                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D    | Ensemble de bibliothèques puissantes, orientées performances et accélérées par le matériel pour le rendu de graphiques 3D.                                              |
| Direct2D    | Ensemble de bibliothèques de graphiques 2D pour l’image bitmap accélérée par le matériel et le dessin 2D vectoriel.                                                           |
| DirectXMath | Bibliothèque d’opérations mathématiques courantes et optimisées utilisées dans les graphiques 2D et 3D, comme les opérations de vecteur et de matrice.                                |
| DirectWrite | Bibliothèque d’API de rendu et de disposition de texte 2D. Il prend en charge l’accélération matérielle et la pixellisation des logiciels.                              |
| XAudio2     | une API audio multiplateforme de bas niveau pour Microsoft Windows qui fournit un traitement de signal et une base de mixage audio pour le développement de jeux. |
| XInput      | Bibliothèque qui prend en charge différents contrôles de jeu traditionnels, en mettant l’accent sur le modèle de contrôleur Xbox 360.                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a>de quels outils ai-je besoin pour développer un jeu Windows avec DirectX ?

Pour vous familiariser avec ce didacticiel, vous avez besoin des éléments suivants :

-   Windows 8.1 ou supérieur
-   Microsoft Visual Studio 2013 ou version ultérieure

 

 




