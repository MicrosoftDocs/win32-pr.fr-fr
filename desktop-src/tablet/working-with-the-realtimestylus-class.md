---
description: La classe RealTimeStylus fait partie des interfaces de programmation d’applications (API) StylusInput. Les sections suivantes décrivent les éléments clés de la classe RealTimeStylus et les API StylusInput.
ms.assetid: 6385c387-5b11-4719-a6ec-e0bebe875348
title: Utilisation de la classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11f61390c39284ccee235294612b621ac09c8d766fd1e7e18686d1bf479c553
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708229"
---
# <a name="working-with-the-realtimestylus-class"></a>Utilisation de la classe RealTimeStylus

La classe [**RealTimeStylus**](realtimestylus-class.md) fait partie des interfaces de programmation d’applications (API) StylusInput. Les sections suivantes décrivent les éléments clés de la classe **RealTimeStylus** et les API StylusInput.

## <a name="instantiating-the-realtimestylus-class"></a>Instanciation de la classe RealTimeStylus

Lorsque vous créez un objet [**RealTimeStylus**](realtimestylus-class.md) , vous avez la possibilité de l’attacher à un handle de fenêtre ou à un contrôle. L’attachement de l’objet **RealTimeStylus** à un handle de fenêtre requiert des autorisations supplémentaires. Pour plus d’informations sur ces autorisations, consultez [considérations relatives à la confiance partielle pour les API StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md).

> [!Note]  
> Vous ne pouvez pas attacher l’objet [**RealTimeStylus**](realtimestylus-class.md) à une fenêtre ou à un contrôle dans un processus différent.

 

Si vous utilisez le constructeur par défaut, vous créez un objet [**RealTimeStylus**](realtimestylus-class.md) qui peut uniquement accepter l’entrée d’un autre objet **RealTimeStylus** . Pour plus d’informations sur la connexion de deux objets **RealTimeStylus** , consultez [le modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md).

L’objet [**RealTimeStylus**](realtimestylus-class.md) implémente l’interface [IDisposable](/dotnet/api/system.idisposable) .

## <a name="extending-the-realtimestylus-class"></a>Extension de la classe RealTimeStylus

Pour permettre à vos plug-ins d’interagir avec le flux de données à partir du stylet, l’objet [**RealTimeStylus**](realtimestylus-class.md) gère deux collections de plug-in, qui sont accessibles par les méthodes [**GetStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylussyncplugin) et [**GetStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylusasyncplugin) en C++ et par les propriétés [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) et [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) en code managé. Vous pouvez ajouter un plug-in en appelant la méthode [**AddStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylussyncplugin) ou [**AddStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylusasyncplugin) de la collection dans la propriété appropriée. Pour plus d’informations sur la création et l’utilisation de plug-ins, consultez [plug-ins et la classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md). Pour plus d’informations sur la création d’un plug-in synchrone ou asynchrone pour une tâche particulière, consultez [Considérations sur les threads pour les API StylusInput](threading-considerations-for-the-stylusinput-apis.md) et [Considérations sur les performances pour les API StylusInput](performance-considerations-for-the-stylusinput-apis.md).

Les plug-ins synchrones doivent implémenter l’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) , et les plug-ins asynchrones doivent implémenter l’interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Chaque plug-in a une propriété [**IStylusSyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) ou [**IStylusAsyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) . L’objet [**RealTimeStylus**](realtimestylus-class.md) appelle uniquement les méthodes de notification du plug-in pour les méthodes auxquelles le plug-in s’est abonné. Pour plus d’informations sur les méthodes de notification, consultez [données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

L’objet [**RealTimeStylus**](realtimestylus-class.md) implémente l’interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . La seule façon d’instancier un objet **RealTimeStylus** qui accepte l’entrée d’un autre objet **RealTimeStylus** consiste à utiliser le constructeur par défaut et à implémenter le modèle **RealTimeStylus** monté en cascade. Pour plus d’informations sur la connexion de deux objets **RealTimeStylus** , consultez [le modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md).

L’objet [**RealTimeStylus**](realtimestylus-class.md) possède deux files d’attente internes qui contiennent les données du stylet de tablette, la file d’attente d’entrée et la file d’attente de sortie. Les données de stylet sont converties en instances des classes de l’espace de noms [Microsoft. StylusInput. PluginData](/previous-versions/ms574862(v=vs.100)) . La liste suivante décrit comment l’objet **RealTimeStylus** gère les données du stylet de tablette.

1.  L’objet [**RealTimeStylus**](realtimestylus-class.md) recherche d’abord les objets de données de plug-in dans sa file d’attente d’entrée, puis à partir du flux de données de stylet de tablette.
2.  L’objet [**RealTimeStylus**](realtimestylus-class.md) envoie un objet de données de plug-in aux objets dans sa collection de plug-ins synchrone. Chaque plug-in synchrone peut ajouter des données à la file d’attente d’entrée ou de sortie.
3.  Une fois que l’objet de données de plug-in a été envoyé à tous les membres de la collection de plug-ins synchrone, l’objet de données de plug-in est placé dans la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) .
4.  L’objet [**RealTimeStylus**](realtimestylus-class.md) recherche ensuite l’objet de données de plug-in suivant à traiter.
5.  Alors que la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) contient des données, l’objet **RealTimeStylus** envoie un objet de données de plug-in à partir de sa file d’attente de sortie aux objets de sa collection de plug-ins asynchrone. Chaque plug-in asynchrone peut ajouter des données à la file d’attente d’entrée ou de sortie, mais étant donné que les plug-ins asynchrones s’exécutent sur le thread d’interface utilisateur, les données sont ajoutées à la file d’attente par rapport aux données de stylet actuelles que l’objet **RealTimeStylus** traite, et non par rapport aux données traitées par le plug-in asynchrone.

Le diagramme suivant illustre le déroulement des données du stylet de tablette par le biais de l’objet [**RealTimeStylus**](realtimestylus-class.md) et de ses collections de plug-ins.

![illustratiom présentant le flot de données de stylet Tablet PC](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

Dans ce diagramme, les cercles « A » et « B » représentent les données du stylet de tablette qui ont déjà été ajoutées à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) et qui n’ont pas encore été envoyées à la collection de plug-in asynchrone. Le cercle « C » indique les données du stylet du Tablet PC actuellement traitées par l’objet **RealTimeStylus** . Il est envoyé à la collection de plug-ins synchrone et placé dans la file d’attente de sortie. Le cercle vide représente la position dans la file d’attente de sortie où les futures données de stylet du Tablet PC sont ajoutées.

Pour plus d’informations sur la façon dont des données spécifiques sont ajoutées à la file d’attente et traitées, consultez [données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Voici un scénario minimal pour l’utilisation de l’objet [**RealTimeStylus**](realtimestylus-class.md) sur un formulaire qui collecte de l’encre.

1.  Créez un formulaire qui implémente l’interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .
2.  Créez un objet [**RealTimeStylus**](realtimestylus-class.md) attaché à un contrôle du formulaire.
3.  Définissez l’intérêt pour les notifications StylusDown, paquets et StylusUp dans la propriété [**IStylusAsyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) du formulaire.
4.  Dans les méthodes [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)et [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) du formulaire, ajoutez du code pour gérer les notifications de stylet, de paquets et de stylet qui sont envoyées à partir de l’objet [**RealTimeStylus**](realtimestylus-class.md) du formulaire.

Pour obtenir un exemple d’une telle application, consultez l’exemple d’une [collection d’encres RealTimeStylus](realtimestylus-ink-collection-sample.md).

## <a name="working-with-tablet-objects"></a>Utilisation des objets tablette

Chaque objet [**RealTimeStylus**](realtimestylus-class.md) activé gère une liste d’identificateurs uniques pour les objets [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) avec lesquels il peut interagir. L’objet **RealTimeStylus** expose deux méthodes pour la traduction entre l’identificateur unique et l’objet **Tablet** : les méthodes [**GetTabletContextIdFromTablet**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet) et [**GetTabletFromTabletContextId**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid) .

L’objet [TabletPropertyDescription](/previous-versions/ms827769(v=msdn.10)) (en code managé) contient une propriété [PacketPropertyId](/previous-versions/ms827780(v=msdn.10)) et une structure [TabletPropertyMetrics](/previous-versions/ms827781(v=msdn.10)) qui décrit la plage, la résolution et les unités de la propriété pour un objet [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) spécifique. La méthode [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) de l’objet [**RealTimeStylus**](realtimestylus-class.md) retourne un tableau d’identificateurs globaux uniques (Guid) pour les propriétés de paquet que l’objet **RealTimeStylus** transfère à ses plug-ins lorsque ces propriétés de paquet sont disponibles. Pour modifier le jeu de propriétés de paquet que l’objet **RealTimeStylus** transmet à ses plug-ins, appelez la méthode [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) de l’objet **RealTimeStylus** . La méthode [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) (dans le code managé) de l’objet **RealTimeStylus** prend un identificateur de tablette unique et retourne une collection d’objets [TabletPropertyDescription](/previous-versions/ms827760(v=msdn.10)) . Ces propriétés de paquet représentent le sous-ensemble de propriétés prises en charge par la tablette qui sont retournées par la méthode **GetDesiredPacketDescription** .

Pour obtenir la liste des GUID de propriété de paquet standard, consultez la classe [constantes PacketPropertyGuids](packetpropertyguids-constants.md) .

## <a name="special-considerations"></a>Considérations spéciales

La liste suivante décrit d’autres points à prendre en compte lors de l’utilisation de l’objet [**RealTimeStylus**](realtimestylus-class.md) avec un objet [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .

-   La méthode [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) peut uniquement être appelée lorsque l’objet [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est désactivé. L’objet [**RealTimeStylus**](realtimestylus-class.md) peut modifier la liste des propriétés de paquet souhaitées ; par conséquent, appelez la méthode [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) après l’appel à la méthode **SetDesiredPacketDescription** pour déterminer les propriétés de paquet que l’objet **RealTimeStylus** peut transférer à ses plug-ins. Une tablette n’est garantie que pour prendre en charge les valeurs **X**, **Y** et **PacketStatus** pour le [PacketProperty](packetproperty-guids.md). Par conséquent, votre conception de plug-in peut être amenée à tenir compte de la réception de propriétés de paquet moins nombreuses que vous le souhaitez.
-   La méthode [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) (pour le code managé) peut être appelée uniquement lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md) est activé. Étant donné que la notification peut être envoyée aux plug-ins Async après la désactivation de l’objet **RealTimeStylus** , vous devrez peut-être mettre en cache les informations pour chaque objet [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . La méthode GetTabletPropertyDescriptionCollection retourne une liste des propriétés de paquet souhaitées prises en charge par la tablette spécifiée.
-   Lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md) est activé, chaque plug-in reçoit un appel à sa méthode [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) . L’objet [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10)) passé dans la notification contient une collection d’identificateurs de contexte pour les tablettes disponibles au moment où l’objet **RealTimeStylus** est activé.
-   Quand une tablette que l’objet [**RealTimeStylus**](realtimestylus-class.md) peut utiliser est ajoutée ou supprimée du Tablet PC pendant que l’objet **RealTimeStylus** est activé, l’objet **RealTimeStylus** notifie ses plug-ins qu’un objet [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) a été ajouté ou supprimé. Pour plus d’informations, consultez [données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="working-with-tablet-pens"></a>Utilisation des stylets de tablette

L’objet [**RealTimeStylus**](realtimestylus-class.md) passe des informations sur le stylet de tablette à ses plug-ins dans un certain nombre de méthodes de notification. Les informations sur le stylet du Tablet PC sont représentées par un objet de [stylet](/previous-versions/ms824824(v=msdn.10)) , obtenu via la méthode [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) . Cet objet est une représentation du stylet au moment où les données ont été rassemblées. Étant donné que les plug-ins reçoivent les données du stylet dans le flux de données du stylet, les plug-ins doivent utiliser les informations de l’objet stylet au lieu de vérifier l’état actuel d’un stylet de tablette particulier à l’aide de la classe [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) . Pour plus d’informations sur la façon dont les données du stylet du Tablet PC et du stylet sont transmises aux plug-ins, consultez [données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Pour récupérer un tableau des objets [Stylus](/previous-versions/ms824824(v=msdn.10)) que l’objet [**RealTimeStylus**](realtimestylus-class.md) a rencontrés depuis sa dernière activation, utilisez la méthode [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) de l’objet **RealTimeStylus** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft. Ink. Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms585724(v=vs.100))
</dt> <dt>

[Modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Considérations relatives à la confiance partielle pour les API StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Considérations relatives aux threads pour les API StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
