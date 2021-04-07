---
title: Utilisation des méthodes de rappel
description: Utilisation des méthodes de rappel
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows Media Format SDK, méthodes de rappel
- Windows Media Format SDK, méthodes appelées de façon asynchrone
- méthodes de rappel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723418"
---
# <a name="using-the-callback-methods"></a>Utilisation des méthodes de rappel

Plusieurs interfaces du kit de développement logiciel (SDK) de format Windows Media contiennent des méthodes appelées de façon asynchrone. La plupart de ces méthodes utilisent des fonctions de rappel pour transmettre des informations à l’application de contrôle.

Les sections suivantes décrivent certains des problèmes généraux relatifs à l’utilisation des méthodes de rappel avec le kit de développement logiciel (SDK) de format Windows Media.



| Section                                                                          | Description                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Utilisation du rappel OnStatus](using-the-onstatus-callback.md)                   | Décrit comment implémenter la méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , qui est utilisée par plusieurs objets pour informer les applications de la progression de l’opération du kit de développement logiciel (SDK). |
| [Utilisation d’événements avec des appels asynchrones](using-events-with-asynchronous-calls.md) | Décrit une technique courante pour gérer les appels de méthode asynchrones dans une application.                                                                                                                  |
| [Utilisation du paramètre de contexte](using-the-context-parameter.md)                   | Présente le paramètre *pvContext* , partagé par plusieurs rappels et leurs méthodes d’appel, et explique comment l’utiliser.                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 




