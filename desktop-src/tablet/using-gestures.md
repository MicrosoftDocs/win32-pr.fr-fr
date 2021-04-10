---
description: Vue d’ensemble de l’utilisation des gestes.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Utilisation des mouvements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951147"
---
# <a name="using-gestures"></a>Utilisation des mouvements

La plateforme Tablet PC fournit le module de reconnaissance de mouvement Microsoft pour la prise en charge des mouvements d’application. Pour obtenir la liste des mouvements pris en charge par le module de reconnaissance de mouvement de Microsoft, consultez le tableau des mouvements d’application dans l’énumération [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) . Le Tablet PC prend également en charge les gestes système. Pour obtenir la liste des gestes système pris en charge par Tablet PC, consultez la table des gestes système dans l’énumération [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .

## <a name="microsoft-gesture-recognizer"></a>Module de reconnaissance de mouvement Microsoft

Vous pouvez utiliser le module de reconnaissance de mouvement Microsoft à l’aide de la propriété [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) de l’objet [**InkCollector**](inkcollector-class.md) , de l’objet [**InkOverlay**](inkoverlay-class.md) ou du contrôle [InkPicture](inkpicture-control-reference.md) . La définition de la propriété **CollectionMode** en mode mixte (**InkAndGesture**) ou en mode geste uniquement (**GestureOnly**) transmet l’encre à la reconnaissance de mouvement Microsoft par défaut. Vous pouvez utiliser le module de reconnaissance de mouvement Microsoft avec le contrôle [InkEdit](inkedit-control-reference.md) en affectant à la propriété [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) la valeur **InkAndGesture**. Vous pouvez également utiliser la reconnaissance de mouvement avec l’objet [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) en ajoutant un objet [**GestureRecognizer**](gesturerecognizer-class.md) à l’une de ses collections de plug-ins.

Toutefois, si les mouvements que vous souhaitez utiliser ne sont pas pris en charge par la version actuelle du module de reconnaissance de mouvement Microsoft, vous pouvez créer votre propre module de reconnaissance et l’utiliser conjointement avec le module de reconnaissance de mouvement Microsoft. Cela permet la prise en charge complète des mouvements dans votre application.

Le Tablet PC utilise un stylet pour une partie ou la totalité de l’entrée. Il est ainsi très facile d’écrire de l’encre. La plateforme Tablet PC offre une architecture d’entrée de stylet qui prend en charge une structure à plusieurs niveaux de mouvements. Les mouvements et le mappage sont définis pour permettre à l’utilisateur d’écrire et d’appeler des mouvements avancés sur de nouvelles surfaces, tout en réservant les gestes qui appellent des messages de souris traditionnels d’autres applications Windows.

La plateforme Tablet PC introduit deux niveaux de gestes : les gestes système, également appelés événements système et les gestes d’application. L’architecture du stylet prend en charge les gestes du système et de l’application. Les gestes d’application à un seul trait et à plusieurs traits sont pris en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mouvements d’application](application-gestures.md)
</dt> <dt>

[Mouvements de raccourcis](flicks-gestures.md)
</dt> <dt>

[Gestes système](system-gestures.md)
</dt> </dl>

 

 



