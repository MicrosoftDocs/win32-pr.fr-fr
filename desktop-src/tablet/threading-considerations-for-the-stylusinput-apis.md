---
description: Vue d’ensemble des considérations relatives aux threads lors de l’utilisation de l’interface de programmation d’applications (API) StylusInput.
ms.assetid: 5d98768a-c60b-4bb0-8640-9bf38254d41f
title: Considérations relatives aux threads pour l’API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27f9a26da86295a322d926278eda87388c0105132eafd2dfa3d7a9f6c6655e48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819639"
---
# <a name="threading-considerations-for-the-stylusinput-api"></a>Considérations relatives aux threads pour l’API StylusInput

L’objet [**RealTimeStylus**](realtimestylus-class.md) est conçu pour fournir un accès en temps réel au flux de données à partir du stylet du Tablet PC. Les plug-ins, objets qui implémentent l’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) peuvent être ajoutés à un objet **RealTimeStylus** . Les plug-ins synchrones sont généralement appelés directement par l’objet **RealTimeStylus** sur un thread de priorité élevée, tandis que les plug-ins asynchrones sont généralement appelés sur le thread d’interface utilisateur de l’application. Créez ou utilisez des plug-ins synchrones pour les tâches qui nécessitent un accès en temps réel au flux de données et qui font l’objet d’une indemande de calcul, comme le filtrage de paquets. Créez ou utilisez des plug-ins asynchrones pour les tâches qui ne nécessitent pas d’accès en temps réel au flux de données, telles que la collecte d’encres.

Étant donné que les données de plug-in de la collection de plug-in asynchrone de l’objet [**RealTimeStylus**](realtimestylus-class.md) sont mises en file d’attente, les plug-ins asynchrones peuvent recevoir des données avant de recevoir un appel à sa méthode [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) , mais une fois l’objet **RealTimeStylus** désactivé. Notez que certaines des méthodes et propriétés de l’objet **RealTimeStylus** lèvent une exception si l’objet **RealTimeStylus** est désactivé.

Les méthodes d’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) suivantes peuvent appeler sur un thread autre que le thread de données de stylet de tablette.

-   Les méthodes [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) et [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) sont appelées sur le thread qui met à jour la propriété [Enabled](/previous-versions/ms585380(v=vs.100)) de l’objet [**RealTimeStylus**](realtimestylus-class.md) ou qui ajoute ou supprime le plug-in pendant que l’objet **RealTimeStylus** est activé.
-   La méthode [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) est appelée sur le thread qui appelle la méthode [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) de l’objet [**RealTimeStylus**](realtimestylus-class.md) .
-   La méthode d' [erreur](/previous-versions/ms824754(v=msdn.10)) est appelée sur le thread sur lequel le plug-in synchrone s’exécute lorsqu’il lève une exception.

Pour interagir avec votre application à partir d’un plug-in synchrone, utilisez la méthode [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) de l’objet [**RealTimeStylus**](realtimestylus-class.md) et gérez les données personnalisées du stylet dans l’un de vos plug-ins asynchrones. Si vous effectuez un appel synchrone à un autre thread à partir d’un plug-in synchrone, vous risquez de bloquer l’objet **RealTimeStylus** et donc de bloquer la collecte d’encres.

Certaines tâches peuvent être exigeantes en termes de calcul, tout en nécessitant un accès en temps réel au flux de données du stylet, par exemple pour la reconnaissance de mouvement multitrait. Les API StylusInput fournissent un modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade qui vous permet d’utiliser deux objets **RealTimeStylus** , chacun appelant ses plug-ins synchrones à partir de différents threads. Pour plus d’informations sur le modèle **RealTimeStylus** monté en cascade, consultez [le modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md).

> [!Note]  
> Vous ne pouvez pas attacher l’objet [**RealTimeStylus**](realtimestylus-class.md) à une fenêtre ou à un contrôle dans un processus différent.

 

Pour plus d’informations sur les considérations relatives aux threads pour Tablet PC en général, consultez Considérations sur les [Threads Tablet PC](tablet-pc-threading-considerations.md)

 

 
