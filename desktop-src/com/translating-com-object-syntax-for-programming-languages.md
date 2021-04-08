---
title: Traduction de la syntaxe d’objet COM pour les langages de programmation
description: Traduction de la syntaxe d’objet COM pour les langages de programmation
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839882"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a>Traduction de la syntaxe d’objet COM pour les langages de programmation

Pour appeler un objet COM à partir d’une application écrite dans un langage de programmation autre que celui utilisé pour écrire l’objet COM, vous devez d’abord traduire la syntaxe de l’objet dans votre langage de programmation. Ceci peut être effectué en suivant les étapes suivantes :

1.  Affichez la bibliothèque de types de l’objet COM dans la syntaxe de votre langage de programmation. Cela vous fournit des descriptions des classes, des interfaces, des méthodes, des propriétés et des événements de l’objet dans la syntaxe de langage que vous utilisez.

    Les produits de développement Microsoft proposent plusieurs outils pour vous aider à afficher et à convertir les bibliothèques de types. Pour plus d’informations, consultez [visionneuses de bibliothèques de types et outils de conversion](type-library-viewers-and-conversion-tools.md) et [Comment outils de développement utiliser des bibliothèques de types](how-developer-tools-use-type-libraries.md).

    Une fois que vous pouvez afficher la bibliothèque de types de l’objet dans votre langage de programmation préféré, vous pouvez comparer sa syntaxe à celle figurant dans la documentation de l’objet. Si l’objet est documenté dans un langage de programmation autre que celui que vous utilisez, les types de données et la syntaxe peuvent différer, mais les descriptions des paramètres, les valeurs de retour et les fonctionnalités de l’objet doivent être identiques.

2.  Prenez en compte les considérations spéciales relatives à la traduction de votre langage de programmation.

    Étant donné que chaque langage de programmation définit des concepts qui peuvent ne pas avoir d’équivalent dans d’autres langages, certaines des fonctionnalités d’un objet peuvent fonctionner différemment dans un autre langage ou ne pas être disponibles du tout. Par exemple, le langage de programmation Visual Basic ne reconnaît pas les types de données non signés C++, tels que **unsignedÂ long**. Une application écrite en Visual Basic ne peut pas utiliser les méthodes COM qui acceptent ou retournent des variables de type de données non signées.

3.  Ajoutez le code compilé de l’objet COM à votre projet. Le code compilé est généralement contenu dans un fichier. dll ou. ocx. Cette étape est nécessaire pour que le compilateur reconnaisse les classes de l’objet COM. Une fois que vous avez ajouté l’objet COM, votre application peut utiliser ses classes et interfaces.

Les rubriques suivantes décrivent comment traduire et utiliser des objets COM dans différents langages de programmation :

-   [Traduire en C++](translating-to-c--.md)
-   [Conversion en Visual Basic](translating-to-visual-basic.md)
-   [Conversion en Java](translating-to-java.md)

Ces rubriques décrivent les outils et les processus de conversion fournis par les produits de développement Microsoft. Pour obtenir des instructions sur la façon de programmer des objets COM à l’aide des outils de développement créés par d’autres sociétés, consultez la documentation de ces outils de développement.

 

 




