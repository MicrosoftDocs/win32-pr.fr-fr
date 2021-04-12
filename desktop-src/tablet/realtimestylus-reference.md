---
description: Fournit l’accès aux événements de stylet provenant des numériseurs de stylet ou tactile.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Référence RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203811"
---
# <a name="realtimestylus-reference"></a>Référence RealTimeStylus

Fournit l’accès aux événements de stylet provenant des numériseurs de stylet ou tactile.

## <a name="in-this-section"></a>Dans cette section

-   [Classes et interfaces RealTimeStylus](realtimestylus-classes-and-interfaces.md)
-   [Énumérations RealTimeStylus](realtimestylus-enumerations.md)
-   [Structures RealTimeStylus](realtimestylus-structures.md)

## <a name="remarks"></a>Notes

Cet objet implémente l’interface com [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Vous pouvez contrôler complètement, restituer dynamiquement, modifier et même supprimer des données du flux de paquets dans les plug-ins synchrones et asynchrones de l’objet de [**classe RealTimeStylus**](realtimestylus-class.md) .

Le stylet en temps réel permet de créer un objet **InkCollecting** qui est monothread et qui réside dans le thread d’interface utilisateur de l’application. Cet objet **InkCollecting** accède aux données de stylet en temps réel à partir de la file d’attente. Un objet **InkCollecting** conjointement avec le stylet en temps réel permet la modification en temps réel de la sélection et l’édition en temps réel des données d’encre collectées. Pour plus d’informations, consultez [accès et manipulation de l’entrée du stylet](accessing-and-manipulating-stylus-input.md).

Utilisez l’objet de [**classe RealTimeStylus**](realtimestylus-class.md) pour interagir directement avec le flux de données du stylet de tablette ou pour bloquer l’encrage en temps réel. Utilisez l’objet de [**classe InkCollector**](inkcollector-class.md) , l’objet de [**classe InkOverlay**](inkoverlay-class.md) , le contrôle de [contrôle InkPicture](inkpicture-control-reference.md) ou le contrôle de [contrôle InkEdit](inkedit-control-reference.md) lorsque le comportement par défaut de ces objets fournit le comportement dont vous avez besoin.

Les événements de stylet en temps réel se trouvent sur un handle de fenêtre spécifique dans un rectangle d’entrée de fenêtre spécifique. Le RealTimeStylusService peut envoyer des données de stylet à plusieurs objets de [**classe RealTimeStylus**](realtimestylus-class.md) . Chaque objet de **classe RealTimeStylus** reçoit des données de stylet pour une section spécifique d’une fenêtre en fonction de la [**propriété IRealTimeStylus :: WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) définie pour cet objet de **classe RealTimeStylus** . L’objet de **classe RealTimeStylus** obtient les données de stylet, puis les traite via une liste de plug-ins synchrones et asynchrones.

La différence entre les plug-ins synchrones et les plug-ins asynchrones réside dans le thread dans lequel ils s’exécutent et dans la séquence d’appel. Les plug-ins synchrones sont appelés par le thread dans lequel s’exécute l’objet de [**classe RealTimeStylus**](realtimestylus-class.md) . Chaque fois que l’objet de **classe RealTimeStylus** est instancié, un thread d’exécution est instancié. Les plug-ins synchrones sont exécutés sur ce nouveau thread instancié pour l’instance de l’objet de **classe RealTimeStylus** . Les plug-ins asynchrones sont appelés par le biais du thread d’interface utilisateur ou d’application après que le flux de paquets a été traité par les plug-ins synchrones et stockés dans la file d’attente de sortie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
