---
title: incorporation du contrôle Lecteur Windows Media dans un programme personnalisé
description: incorporation du contrôle Lecteur Windows Media dans un programme personnalisé
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet, incorporation ActiveX contrôle
- contrôle de ActiveX Lecteur Windows Media, incorporation
- contrôle de ActiveX, incorporation
- Lecteur Windows Media contrôle de ActiveX Mobile, incorporation
- Lecteur Windows Media Mobile, incorporation ActiveX contrôle
- incorporation, programmes personnalisés
- incorporation de programme personnalisé
- incorporation, programmes basés sur des Visual Basic
- incorporation de programmes basés sur Visual Basic
- incorporation, utilisation manuelle des méthodes COM
- incorporation manuelle à l’aide de méthodes COM
- incorporation, programmes C++
- Incorporation de programmes C++
- incorporation, Visual Studio des programmes
- Visual Studio, incorporation de programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b700f1ad4609f36750148c90ab26661498a0cc6186dba2928e90bcec9e63bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862999"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a>incorporation du contrôle Lecteur Windows Media dans un programme personnalisé

étant donné que le contrôle Lecteur Windows Media ActiveX est basé sur la technologie COM (component Object Model) Microsoft, vous pouvez l’incorporer dans des programmes écrits avec de nombreux langages de programmation différents. le contrôle Lecteur Windows Media représente un moyen simple d’ajouter des fonctionnalités multimédias numériques sophistiquées à n’importe quel programme.

dans Microsoft Visual Basic, vous pouvez ajouter le contrôle à la boîte à outils du contrôle, le placer dans un formulaire et ajuster les propriétés du contrôle dans la fenêtre propriétés. si vous souhaitez une interface utilisateur personnalisée, vous pouvez placer des boutons de commande sur le formulaire et ajouter du code qui gère le contrôle de Lecteur Windows Media. l’incorporation du contrôle dans un programme Visual Basic est très similaire à son incorporation dans un document Office et à sa programmation avec VBA.

Vous pouvez également incorporer manuellement le contrôle à l’aide de méthodes COM pour instancier le contrôle et accéder aux interfaces COM documentées dans [Référence du modèle objet pour C++](object-model-reference-for-c.md).

lorsque vous incorporez le contrôle Lecteur Windows Media dans un programme C++, vous avez la possibilité d’implémenter des interfaces COM qui permettent au contrôle de s’exécuter en mode distant. Cela signifie que le contrôle incorporé partage le même moteur de lecture que le mode complet du joueur, et les utilisateurs peuvent basculer entre le mode plein et l’état ancré sans interrompre la lecture des médias numériques. Vous pouvez également contrôler ce qui est affiché dans les différents volets du lecteur en mode complet lorsque vos utilisateurs basculent vers l’état non ancré.

Avec l’incorporation C++, vous avez également la possibilité d’appliquer un fichier de définition d’apparence au contrôle de lecteur incorporé. Il s’agit d’un moyen simple de créer du code d’interface utilisateur léger que vous pouvez gérer séparément de votre code de programme principal.

Microsoft Visual Studio prend en charge l’incorporation de contrôles ActiveX, y compris le contrôle Lecteur Windows Media. lorsque vous choisissez cette solution, Visual Studio crée un nouvel assembly d’interopérabilité de substitution pour gérer l’interopérabilité entre le .NET Framework et le contrôle Lecteur Windows Media. Visual Studio utilise l’outil de tlbimp.exe .NET Framework pour créer l’assembly d’interopérabilité. cela signifie que les signatures affichées lors de l’utilisation de la fonctionnalité IntelliSense dans Visual Studio utilisent la sémantique déterminée par la version actuelle de tlbimp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**incorporation du contrôle Lecteur Windows Media**](embedding-the-windows-media-player-control.md)
</dt> <dt>

[**utilisation du contrôle Lecteur Windows Media dans un programme C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[**utilisation du contrôle Lecteur Windows Media dans une Solution .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**utilisation du contrôle Lecteur Windows Media avec Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




