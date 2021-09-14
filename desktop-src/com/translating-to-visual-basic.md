---
title: Conversion en Visual Basic
description: Conversion en Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095482"
---
# <a name="translating-to-visual-basic"></a>Conversion en Visual Basic

vous pouvez ajouter un objet COM à votre projet Visual Basic en tant que référence ou composant. Une fois que l’objet est ajouté à votre projet, votre application peut accéder à ses classes et interfaces. vous pouvez ensuite utiliser l’explorateur d’objets Visual Basic pour afficher les informations de la bibliothèque de types de l’objet dans la syntaxe Visual Basic.

En général, les contrôles sont ajoutés à un projet en tant que composants et les éléments qui ne sont pas des contrôles sont ajoutés en tant que références. lorsqu’un objet COM est ajouté en tant que composant, il apparaît dans la boîte à outils Visual Basic. les nouvelles instances de cet objet sont créées en faisant glisser l’icône de l’objet de la boîte à outils vers un formulaire de Visual Basic ou un autre type de conteneur. Les nouvelles instances d’objets COM ajoutées en tant que références sont créées à l’aide du mot clé **New** .

La distinction entre l’utilisation d’une classe comme référence et d’un composant est subtile mais importante. Quand vous ajoutez un objet en tant que référence, vous pouvez utiliser uniquement la bibliothèque de types fournie par le contrôle ou la bibliothèque de types « RAW ».

si vous ajoutez un contrôle en tant que composant, Visual Basic fusionne les propriétés et les méthodes extendeur du formulaire dans lequel le contrôle est incorporé avec la bibliothèque de types du contrôle, fournissant ainsi une version encapsulée et étendue de la bibliothèque de types. Avec cette version de la bibliothèque de types, vous pouvez utiliser des propriétés d’extendeur telles que Top et Left comme si elles faisaient partie du contrôle, au lieu du conteneur du contrôle.

Visual Basic ne prend actuellement pas en charge plusieurs bibliothèques de types intégrées à un seul fichier .dll. Si vous exécutez dans une DLL qui incorpore plusieurs bibliothèques de types, vous devez obtenir des copies autonomes des bibliothèques de types à partir de la source qui a fourni l’objet afin d’utiliser l’objet avec Visual Basic.

Pour plus d'informations, voir les rubriques suivantes :

-   [conversion en Visual Basic à partir de C++](translating-to-visual-basic-from-c--.md)
-   [conversion en Visual Basic à partir de Java](translating-to-visual-basic-from-java.md)
-   [ajout d’un composant à un Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
-   [ajout d’une référence à un Visual Basic Project](adding-a-reference-to-a-visual-basic-project.md)
-   [Visual Basic Explorateur d’objets](visual-basic-object-browser.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traduire en C++](translating-to-c--.md)
</dt> <dt>

[Conversion en Java](translating-to-java.md)
</dt> </dl>

 

 




