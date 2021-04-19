---
description: Événements de session multimédia
ms.assetid: 882a01f2-8f5c-4640-a8ac-f4f5860d7ed1
title: Événements de session multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e128fc5e11f70fe47d02356ce44629b98bfdfe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106531457"
---
# <a name="media-session-events"></a>Événements de session multimédia

La plupart des opérations de la session de média sont exécutées de façon asynchrone, de sorte que l’application doit écouter les événements à l’aide de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la session multimédia. (L’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) hérite de **IMFMediaEventGenerator**.) La séquence exacte d’événements dépend de votre application, mais les événements suivants sont déclenchés par la session multimédia dans pratiquement toutes les situations.



| Événement                                                                  | Description                                                                                                                                                                                                                    |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEEndOfPresentation](meendofpresentation.md)                         | Déclenché lorsque la source du média a terminé la présentation. Les données peuvent quand même être déplacées dans le pipeline pour l’instant.                                                                                                     |
| [MEError](meerror.md)                                                 | Déclenché si une erreur se produit pendant la diffusion en continu.                                                                                                                                                                                    |
| [MESessionClosed](mesessionclosed.md)                                 | Déclenché lorsque la méthode [**Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) est terminée. Cet événement est le dernier événement mis en file d’attente par la session multimédia. Une fois cet événement reçu, il est possible d’arrêter en toute sécurité les sources multimédias que vous avez créées. |
| [MESessionEnded](mesessionended.md)                                   | Déclenché lorsque la session multimédia est terminée avec la dernière présentation.                                                                                                                                                              |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) | Indique à l’application l’heure de la présentation à laquelle la nouvelle présentation doit commencer.                                                                                                                                        |
| [MESessionStarted](mesessionstarted.md)                               | Déclenché lorsque la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) se termine. À moins qu’une erreur ne se produise, les données sont déplacées dans le pipeline à ce stade.                                                                          |
| [MESessionTopologySet](mesessiontopologyset.md)                       | Déclenché lorsque la méthode [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se termine. À moins qu’une erreur ne se produise, l’application n’a pas besoin d’effectuer aucune action.                                                                 |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                 | Déclenché à différents moments de modification de l’état d’une topologie.                                                                                                                                                                 |



 

La méthode [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) ne déclenche pas d’événement. La méthode **Shutdown** est synchrone. Une fois que cette méthode a retourné une valeur, il est possible de libérer en toute sécurité votre pointeur de rappel d’événement.

En plus des événements de la session multimédia, l’application peut recevoir des événements des récepteurs de média dans la topologie. Il peut s’agir d’événements personnalisés définis par le récepteur multimédia, qui peuvent contenir des données arbitraires. Par exemple, le récepteur peut dériver les données d’événement à partir des données sources, qui peuvent provenir d’une source externe non approuvée. Une application doit ignorer les événements qu’elle ne reconnaît pas et faire preuve de prudence lors de l’analyse des données d’événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> </dl>

 

 



