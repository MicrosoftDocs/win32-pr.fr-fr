---
description: Les API StylusInput vous permettent d’interagir avec le flux de données de stylet de tablette. Pour interagir avec le flux de données, ajoutez un objet RealTimeStylus à votre application, puis ajoutez des plug-ins à l’objet RealTimeStylus.
ms.assetid: 88bab0ab-df9f-4813-9a9f-9a137813f0b4
title: Architecture des API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 961d6e3e94d47054afb28948685fce5fe1cafe9cbb0fa2f36e5a2d8508f28b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093156"
---
# <a name="architecture-of-the-stylusinput-apis"></a>Architecture des API StylusInput

Les API StylusInput vous permettent d’interagir avec le flux de données de stylet de tablette. Pour interagir avec le flux de données, ajoutez un objet [**RealTimeStylus**](realtimestylus-class.md) à votre application, puis ajoutez des plug-ins à l’objet **RealTimeStylus** .

Deux plug-ins sont fournis dans les API StylusInput. L’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) implémente l’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . L’objet **DynamicRenderer** restitue l’encre en temps réel, lors de son dessin. L’objet [**GestureRecognizer**](gesturerecognizer-class.md) implémente les interfaces **IStylusSyncPlugin** et [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . L’objet **GestureRecognizer** reconnaît les gestes d’application.

## <a name="definitions"></a>Définitions

Les termes suivants sont utilisés dans les sections décrivant les API StylusInput :

Plug-in synchrone

Classe qui implémente l’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . Les plug-ins synchrones sont généralement appelés directement par l’objet [**RealTimeStylus**](realtimestylus-class.md) .

Plug-in asynchrone

Classe qui implémente l’interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Les plug-ins asynchrones sont généralement appelés sur le thread d’interface utilisateur de l’application.

Collection de plug-ins synchrone

Collection [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) , qui est une collection ordonnée d’objets [IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10)) . Une collection de plug-ins synchrone fait généralement référence à la collection assignée à la propriété [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) d’un objet [RealTimeStylus](/previous-versions/ms824830(v=msdn.10)) . Seuls les plug-ins synchrones peuvent être ajoutés à une collection de plug-ins synchrone.

Collection de plug-ins asynchrone

Collection [StylusAsyncPluginCollection](/previous-versions/ms824808(v=msdn.10)) , qui est une collection ordonnée d’objets [IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10)) . Une collection de plug-ins asynchrone fait généralement référence à la collection assignée à la propriété [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) d’un objet [RealTimeStylus](/previous-versions/ms824830(v=msdn.10)) . Seuls les plug-ins asynchrones peuvent être ajoutés à une collection de plug-ins asynchrone.

## <a name="synchronous-and-asynchronous-plug-ins"></a>Plug-ins synchrones et asynchrones

L’objet [**RealTimeStylus**](realtimestylus-class.md) est conçu pour fournir un accès en temps réel au flux de données à partir d’un stylet. Créez ou utilisez des plug-ins synchrones pour les tâches qui nécessitent un accès en temps réel au flux de données et qui font l’objet d’une indemande de calcul, comme pour le filtrage de paquets. Créez ou utilisez des plug-ins asynchrones pour les tâches qui ne nécessitent pas d’accès en temps réel au flux de données, par exemple pour créer et stocker des traits dans un objet [**InkDisp**](inkdisp-class.md) .

Certaines tâches peuvent nécessiter un calcul exigeant un accès en temps réel au flux de données, par exemple la reconnaissance de mouvement à multitrait. Pour répondre à ces besoins, les API StylusInput fournissent un modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade qui vous permet d’utiliser deux objets **RealTimeStylus** , chacun s’exécutant sur son propre thread. Pour plus d’informations sur le modèle **RealTimeStylus** monté en cascade, consultez [le modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md).

Pour plus d’informations sur l’utilisation et la création de plug-ins, consultez [utilisation des API StylusInput](working-with-the-stylusinput-apis.md).

## <a name="the-tablet-pen-data-stream"></a>Flux de données du stylet de tablette

L’objet [**RealTimeStylus**](realtimestylus-class.md) possède deux files d’attente internes qui contiennent les données du stylet de tablette, la file d’attente d’entrée et la file d’attente de sortie. Les données de stylet sont converties en instances des classes de l’espace de noms [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) . La liste suivante décrit comment l’objet **RealTimeStylus** gère les données du stylet de tablette :

L’objet [**RealTimeStylus**](realtimestylus-class.md) recherche d’abord les objets de données de plug-in dans sa file d’attente d’entrée, puis à partir du flux de données de stylet de tablette.

L’objet [**RealTimeStylus**](realtimestylus-class.md) envoie un objet de données de plug-in aux objets dans sa collection de plug-ins synchrone. Chaque plug-in synchrone peut ajouter des données à la file d’attente d’entrée ou de sortie.

Une fois que l’objet de données de plug-in a été envoyé à tous les membres de la collection de plug-ins synchrone, l’objet de données de plug-in est placé dans la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) .

L’objet [**RealTimeStylus**](realtimestylus-class.md) recherche ensuite l’objet de données de plug-in suivant à traiter.

Alors que la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) contient des données, l’objet **RealTimeStylus** envoie un objet de données de plug-in à partir de sa file d’attente de sortie aux objets de sa collection de plug-ins asynchrone. Chaque plug-in asynchrone peut ajouter des données à la file d’attente d’entrée ou de sortie. Toutefois, étant donné que les plug-ins asynchrones s’exécutent sur le thread d’interface utilisateur, les données sont ajoutées à la file d’attente par rapport aux données de stylet actuelles que l’objet **RealTimeStylus** traite, et non par rapport aux données traitées par le plug-in asynchrone.

Le diagramme suivant illustre le déroulement des données du stylet de tablette par le biais de l’objet [**RealTimeStylus**](realtimestylus-class.md) et de ses collections de plug-ins.

![Flow des données du stylet de tablette via l’objet RealTimeStylus et ses collections de plug-in](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

Dans ce diagramme, les cercles étiquetés « A » et « B » représentent des données de stylet de tablette qui ont déjà été ajoutées à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) et qui n’ont pas encore été envoyées à la collection de plug-ins asynchrone. Le cercle intitulé « C » représente les données du stylet de tablette que l’objet **RealTimeStylus** est en train de traiter. Il est envoyé à la collection de plug-ins synchrone et placé dans la file d’attente de sortie. Le cercle vide représente la position dans la file d’attente de sortie où les futures données de stylet du Tablet PC sont ajoutées.

Pour plus d’informations sur la façon dont des données spécifiques sont ajoutées à la file d’attente et traitées, consultez [données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-stylusinput-apis"></a>API StylusInput

Les API StylusInput résident principalement dans les espaces de noms [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) et [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) . Toutefois, les API StylusInput référencent également certaines classes dans l’espace de noms [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) , telles que la classe [Tablet](/previous-versions/ms827783(v=msdn.10)) , la collection [TabletPropertyDescriptionCollection](/previous-versions/ms827760(v=msdn.10)) , et les énumérations [ApplicationGesture](/previous-versions/ms827547(v=msdn.10)) et [SystemGesture](/previous-versions/ms827134(v=msdn.10)) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))
</dt> <dt>

[**GestureRecognizer**](gesturerecognizer-class.md)
</dt> <dt>

[**Participent**](realtimestylus-class.md)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[Utilisation des API StylusInput](working-with-the-stylusinput-apis.md)
</dt> <dt>

[Modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md)
</dt> </dl>

 

 
