---
description: Les considérations suivantes relatives aux threads Tablet PC sont spécifiques à l’utilisation du modèle COM (Component Object Model) et de l’automatisation.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Considérations relatives aux threads COM et Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515400"
---
# <a name="com-and-automation-threading-considerations"></a>Considérations relatives aux threads COM et Automation

Les considérations suivantes relatives aux threads Tablet PC sont spécifiques à l’utilisation du modèle COM (Component Object Model) et de l’automatisation.

-   [Cohérence de thread](#thread-safety)
-   [Applications STA et MTA](#sta-and-mta-applications)
-   [InkCollector et InkOverlay](#inkcollector-and-inkoverlay)
-   [Récepteurs d’événements](#event-sinks)
-   [Exceptions dans les gestionnaires d’événements](#exceptions-within-event-handlers)
-   [Rubriques connexes](#related-topics)

## <a name="thread-safety"></a>Cohérence de thread

À l’exception des contrôles [InkPicture](inkpicture-control.md) et [InkEdit](inkedit-control.md) , les objets Tablet PC sont thread-safe et sont marqués comme les deux. Si elles sont marquées comme étant toutes les deux, elles peuvent s’exécuter dans un thread cloisonné (STA, Single-Threaded Apartment) ou un cloisonnement multithread (MTA).

Windows Forms utilise le modèle STA, car les Windows Forms sont basés sur des fenêtres Win32 natives qui sont intrinsèquement des threads cloisonnés.

## <a name="sta-and-mta-applications"></a>Applications STA et MTA

Si votre application s’exécute dans un MTA ou utilise le marshaleur de thread libre (FTM), vous devez écrire du code thread-safe. Toutefois, en procédant ainsi, vous pouvez améliorer certains problèmes de performances de gestion des événements.

## <a name="inkcollector-and-inkoverlay"></a>InkCollector et InkOverlay

Votre application ne doit pas libérer sa référence finale à l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) , ce qui a pour conséquence la destruction de l’objet, directement à partir du thread Ink. Au lieu de cela, l’application doit libérer l’objet **InkCollector** ou **InkOverlay** à partir d’un thread d’application.

**Attention :** Une application marquée comme MTA ou utilisant FTM, qui autorise les appels directs à partir du thread Ink dans le cloisonnement de l’application, peut libérer sa référence finale à l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) directement à partir du thread d’encre. Toutefois, cela provoque l’échec d’une application irrécupérable.

## <a name="event-sinks"></a>Récepteurs d’événements

Si votre application n’utilise pas FTM et qu’un objet et que son récepteur d’événements sont créés dans différents cloisonnements, l’événement s’exécute sur le thread qui dessert le récepteur d’événements.

## <a name="exceptions-within-event-handlers"></a>Exceptions dans les gestionnaires d’événements

Les exceptions levées à partir des gestionnaires d’événements Tablet PC sont consommées et ne sont pas visibles par le reste ou votre application. De même, les valeurs HRESULT ne sont pas propagées à partir des gestionnaires d’événements Tablet PC. Si une application utilisant la couche COM lève une exception, le thread d’arrière-plan se termine et l’exception est perdue. Aucun gestionnaire d’événements supplémentaire n’est appelé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de récepteurs d’événements C++](c---event-sinks-sample.md)
</dt> <dt>

[Considérations générales sur les threads](general-threading-considerations.md)
</dt> <dt>

[Considérations sur les threads de bibliothèque managée](managed-library-threading-considerations.md)
</dt> </dl>

 

 



