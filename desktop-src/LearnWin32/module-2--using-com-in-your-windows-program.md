---
title: utilisation de COM dans votre application Windows
description: Le module 1 de cette série a montré comment créer une fenêtre et répondre aux messages de fenêtre tels que WM \_ Paint et WM \_ Close. Le module 2 présente le modèle COM (Component Object Model).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094350"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a>Module 2. Utilisation de COM dans votre programme Windows-Based

Le [module 1](your-first-windows-program.md) de cette série a montré comment créer une fenêtre et répondre aux messages de fenêtre tels que [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) et [**WM \_ Close**](/windows/desktop/winmsg/wm-close). Le module 2 présente le modèle COM (Component Object Model).

COM est une spécification permettant de créer des composants logiciels réutilisables. la plupart des fonctionnalités que vous allez utiliser dans un programme Windows moderne reposent sur COM, telles que les suivantes :

-   Graphiques (Direct2D)
-   Texte (DirectWrite)
-   Shell Windows
-   Contrôle de ruban
-   Animation de l’interface utilisateur

(Certaines technologies de cette liste utilisent un sous-ensemble de COM et ne sont donc pas des COM « purs ».)

COM offre une réputation difficile à apprendre. Et il est vrai que l’écriture d’un nouveau module logiciel pour prendre en charge COM peut être délicate. Mais si votre programme est strictement un *consommateur* de com, vous constaterez peut-être que com est plus facile à comprendre que prévu.

Ce module montre comment appeler des API COM dans votre programme. Elle décrit également quelques-unes des raisons de la conception de COM. Si vous comprenez pourquoi COM est conçu comme c’est le cas, vous pouvez le programmer plus efficacement. La deuxième partie du module décrit quelques pratiques de programmation recommandées pour COM.

COM a été introduit dans 1993 pour prendre en charge la liaison et l’incorporation d’objets (OLE) 2,0. Les gens pensent parfois que COM et OLE sont identiques. Il peut s’agir d’une autre raison de croire que COM est difficile à apprendre. OLE 2,0 repose sur COM, mais vous n’avez pas besoin de connaître OLE pour comprendre COM.

COM est une *norme binaire*, et non une norme de langage : elle définit l’interface binaire entre une application et un composant logiciel. En tant que norme binaire, COM est indépendant du langage, bien qu’il corresponde naturellement à certaines constructions C++. Ce module se concentrera sur trois objectifs principaux de COM :

-   Séparation de l’implémentation d’un objet de son interface.
-   Gestion de la durée de vie d’un objet.
-   Découverte des fonctionnalités d’un objet au moment de l’exécution.

## <a name="in-this-section"></a>Dans cette section

-   [Qu’est-ce qu’une interface COM ?](what-is-a-com-interface-.md)
-   [Initialisation de la bibliothèque COM](initializing-the-com-library.md)
-   [Codes d’erreur dans COM](error-codes-in-com.md)
-   [Création d’un objet dans COM](creating-an-object-in-com.md)
-   [Exemple : la boîte de dialogue Ouvrir](example--the-open-dialog-box.md)
-   [Gestion de la durée de vie d’un objet](managing-the-lifetime-of-an-object.md)
-   [Demande d’un objet pour une interface](asking-an-object-for-an-interface.md)
-   [Allocation de mémoire dans COM](memory-allocation-in-com.md)
-   [Pratiques de codage COM](com-coding-practices.md)
-   [Gestion des erreurs dans COM](error-handling-in-com.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Apprendre à programmer pour Windows en C++](learn-to-program-for-windows.md)
</dt> </dl>

 

 