---
title: Incorporation du contrôle du lecteur Windows Media dans un programme personnalisé
description: Incorporation du contrôle du lecteur Windows Media dans un programme personnalisé
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Contrôle ActiveX, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- incorporation, programmes personnalisés
- incorporation de programme personnalisé
- incorporation, programmes basés sur des Visual Basic
- Incorporation de programmes basés sur Visual Basic
- incorporation, utilisation manuelle des méthodes COM
- incorporation manuelle à l’aide de méthodes COM
- incorporation, programmes C++
- Incorporation de programmes C++
- incorporation, programmes Visual Studio
- Visual Studio, incorporation de programmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028986"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a>Incorporation du contrôle du lecteur Windows Media dans un programme personnalisé

Étant donné que le contrôle ActiveX du lecteur Windows Media est basé sur la technologie COM (Component Object Model) Microsoft, vous pouvez l’incorporer dans des programmes écrits avec de nombreux langages de programmation différents. Le contrôle du lecteur Windows Media représente un moyen simple d’ajouter des fonctionnalités multimédias numériques sophistiquées à n’importe quel programme.

Dans Microsoft Visual Basic, vous pouvez ajouter le contrôle à la boîte à outils du contrôle, le placer dans un formulaire et ajuster les propriétés du contrôle dans la fenêtre Propriétés. Si vous souhaitez une interface utilisateur personnalisée, vous pouvez placer des boutons de commande sur le formulaire et ajouter du code qui gère le contrôle du lecteur Windows Media. L’incorporation du contrôle dans un programme Visual Basic est très similaire à son incorporation dans un document Office et à sa programmation avec VBA.

Vous pouvez également incorporer manuellement le contrôle à l’aide de méthodes COM pour instancier le contrôle et accéder aux interfaces COM documentées dans [Référence du modèle objet pour C++](object-model-reference-for-c.md).

Lorsque vous incorporez le contrôle du lecteur Windows Media dans un programme C++, vous avez la possibilité d’implémenter des interfaces COM qui permettent au contrôle de s’exécuter en mode distant. Cela signifie que le contrôle incorporé partage le même moteur de lecture que le mode complet du joueur, et les utilisateurs peuvent basculer entre le mode plein et l’état ancré sans interrompre la lecture des médias numériques. Vous pouvez également contrôler ce qui est affiché dans les différents volets du lecteur en mode complet lorsque vos utilisateurs basculent vers l’état non ancré.

Avec l’incorporation C++, vous avez également la possibilité d’appliquer un fichier de définition d’apparence au contrôle de lecteur incorporé. Il s’agit d’un moyen simple de créer du code d’interface utilisateur léger que vous pouvez gérer séparément de votre code de programme principal.

Microsoft Visual Studio prend en charge l’incorporation de contrôles ActiveX, y compris le contrôle du lecteur Windows Media. Lorsque vous choisissez cette solution, Visual Studio crée un nouvel assembly d’interopérabilité de substitution pour gérer l’interopérabilité entre le .NET Framework et le contrôle du lecteur Windows Media. Visual Studio utilise l’outil .NET Framework tlbimp.exe pour créer l’assembly d’interopérabilité. Cela signifie que les signatures affichées lors de l’utilisation de la fonctionnalité IntelliSense dans Visual Studio utilisent la sémantique déterminée par la version actuelle de Tlbimp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Incorporation du contrôle du lecteur Windows Media**](embedding-the-windows-media-player-control.md)
</dt> <dt>

[**Utilisation du contrôle du lecteur Windows Media dans un programme C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[**Utilisation du contrôle du lecteur Windows Media dans une solution .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Utilisation du contrôle du lecteur Windows Media avec Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




