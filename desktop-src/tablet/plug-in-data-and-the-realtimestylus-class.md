---
description: Les plug-ins de la classe RealTimeStylus doivent implémenter l’interface IStylusSyncPlugin ou IStylusAsyncPlugin, ou les deux.
ms.assetid: 827ac817-e0e6-4750-9d48-b939ccd5e679
title: Données de plug-in et classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0540d90f291acfef27a09df08ffff645c280d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480965"
---
# <a name="plug-in-data-and-the-realtimestylus-class"></a>Données de plug-in et classe RealTimeStylus

Les plug-ins de la classe [**RealTimeStylus**](realtimestylus-class.md) doivent implémenter l’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , ou les deux. Bien que vous deviez implémenter toutes les méthodes d’interface de plug-in, votre plug-in reçoit uniquement les appels sur les méthodes marquées dans les plug-ins [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) propriété.

Les méthodes définies sur les interfaces utilisent des objets dans l’espace de noms [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) pour passer les données de stylet aux plug-ins. Le tableau suivant décrit les objets de données qui sont des paramètres dans les méthodes de notification et répertorie la valeur [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) associée à la notification.



| Données de plug-in                                                                                          | Valeur DataInterestMask     | Description                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CustomStylusData](/previous-versions/ms824747(v=msdn.10))                     | **CustomStylusDataAdded**  | Données d’application personnalisées qu’ajoute un plug-in.<br/>                                                                                                                                                                                                 |
| [Partagefichiers](/previous-versions/ms824740(v=msdn.10))                                   | **Error**                  | Informations d’erreur que l’objet [**RealTimeStylus**](realtimestylus-class.md) ajoute en réponse à une exception non gérée dans l’un de ses plug-ins.<br/>                                                                                          |
| [InAirPacketsData](/previous-versions/ms824592(v=msdn.10))                     | **InAirPackets**           | Informations de paquet pour le mouvement du stylet lorsque le stylet est dans l’air au-dessus du digitaliseur.<br/>                                                                                                                                                         |
| [PacketsData](/previous-versions/ms824590(v=msdn.10))                               | **Paquets**                | Informations de paquet pour le mouvement du stylet lorsque le stylet touche le digitaliseur.<br/>                                                                                                                                                             |
| [RealTimeStylusDisabledData](/previous-versions/ms824576(v=msdn.10)) | **RealTimeStylusDisabled** | Informations que l’objet [**RealTimeStylus**](realtimestylus-class.md) ajoute lorsqu’il est désactivé.<br/>                                                                                                                                        |
| [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10))   | **RealTimeStylusEnabled**  | Informations que l’objet [**RealTimeStylus**](realtimestylus-class.md) ajoute lorsqu’il est activé.<br/>                                                                                                                                         |
| [StylusButtonDownData](/previous-versions/ms824181(v=msdn.10))             | **StylusButtonDown**       | Informations sur le bouton de stylet particulier qui est enfoncé.<br/>                                                                                                                                                                        |
| [StylusButtonUpData](/previous-versions/ms824172(v=msdn.10))                 | **StylusButtonUp**         | Informations sur le bouton de stylet particulier qui est relâché.<br/>                                                                                                                                                                       |
| [StylusDownData](/previous-versions/ms585582(v=vs.100))                                   | **StylusDown**             | Les informations de paquet pour un stylet en tant que stylet sont mises en contact avec le digitaliseur.<br/>                                                                                                                                                      |
| [StylusInRangeData](/previous-versions/ms824090(v=msdn.10))                   | **StylusInRange**          | Informations sur le stylet particulier qui saisit la zone d’entrée de l’objet [**RealTimeStylus**](realtimestylus-class.md) ou qui introduit la plage de détection du digitaliseur au-dessus de la zone d’entrée de l’objet **RealTimeStylus** .<br/> |
| [StylusOutOfRangeData](/previous-versions/ms824072(v=msdn.10))             | **StylusOutOfRange**       | Informations sur le stylet particulier qui quitte la zone d’entrée de l’objet [**RealTimeStylus**](realtimestylus-class.md) ou la sortie de la plage de détection du digitaliseur au-dessus de la zone d’entrée de l’objet **RealTimeStylus** .<br/>   |
| [StylusUpData](/previous-versions/ms824057(v=msdn.10))                             | **StylusUp**               | Les informations de paquet pour un stylet au fur et à mesure du stylet sont levées sur le digitaliseur.<br/>                                                                                                                                                                  |
| [SystemGestureData](/previous-versions/ms824019(v=msdn.10))                   | **SystemGesture**          | Informations que l’objet [**RealTimeStylus**](realtimestylus-class.md) ajoute lorsqu’il détecte un mouvement système.<br/>                                                                                                                                 |
| [TabletAddedData](/previous-versions/ms824010(v=msdn.10))                       | **TabletAdded**            | Informations sur l’objet [Tablet](/previous-versions/ms827783(v=msdn.10)) qui est ajouté.<br/>                                                                                                                                                |
| [TabletRemovedData](/previous-versions/ms823997(v=msdn.10))                   | **TabletRemoved**          | Informations sur l’objet [Tablet PC](/previous-versions/ms827783(v=msdn.10)) en cours de suppression.<br/>                                                                                                                                              |



 

Pour plus d’informations sur la façon dont l’objet [**RealTimeStylus**](realtimestylus-class.md) gère le flux de données de stylet de tablette, consultez [utilisation de la classe RealTimeStylus](working-with-the-realtimestylus-class.md).

## <a name="data-interest"></a>Intérêt pour les données

L’objet [**RealTimeStylus**](realtimestylus-class.md) vérifie la propriété [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) d’un plug-in quand le plug-in est ajouté à la collection de plug-ins synchrone ou asynchrone de l’objet **RealTimeStylus** . Par conséquent, vous devez utiliser la propriété DataInterest pour vous abonner à toutes les notifications utilisées par cette instance de votre plug-in, mais pas rarement, mais pas à l’une des notifications que cette instance de votre plug-in n’utilise jamais. Pour les notifications que votre plug-in utilise occasionnellement, vérifiez d’abord l’état de votre plug-in dans la méthode de notification et retournez si la notification n’est pas utilisée par votre plug-in dans son état actuel.

Un plug-in reçoit uniquement les appels sur les méthodes marquées dans la propriété [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) du plug-in. Pour plus d’informations sur les valeurs possibles de la propriété **DataInterest** d’un plug-in, consultez l’énumération [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .

## <a name="timing"></a>Minutage

Les données sont mises en file d’attente dans l’objet [**RealTimeStylus**](realtimestylus-class.md) avant d’être passées aux plug-ins dans la collection de plug-in asynchrone. La liste suivante décrit certaines situations dont vous devrez peut-être tenir compte lors de la conception d’un plug-in asynchrone.

-   Lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md) est désactivé, le plug-in asynchrone peut recevoir d’autres notifications mises en file d’attente avant l’appel de sa méthode [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) . Dans ce cas, les appels du plug-in à certaines méthodes et propriétés de l’objet **RealTimeStylus** lèvent une exception. Les informations relatives à votre plug-in doivent être mises en cache lorsque l’objet **RealTimeStylus** est activé.
-   La méthode [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) de l’objet [**RealTimeStylus**](realtimestylus-class.md) peut supprimer les informations de la file d’attente de sortie. Par conséquent, les plug-ins asynchrones ne peuvent pas reposer sur la réception de toutes les notifications pertinentes.
-   Lorsqu’un objet [tablette](/previous-versions/ms827783(v=msdn.10)) qui est disponible pour l’objet [**RealTimeStylus**](realtimestylus-class.md) est supprimé, le plug-in asynchrone peut recevoir la notification du stylet en file d’attente pour la tablette avant l’appel de sa méthode [TabletRemoved](/previous-versions/bb361092(v=vs.100)) . Dans ce cas, l’appel de la méthode [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) de l’objet **RealTimeStylus** ne fonctionne pas. Les informations relatives à votre plug-in doivent être mises en cache lorsque l’objet **RealTimeStylus** est activé ou lorsqu’une nouvelle tablette est ajoutée.

Selon votre application, vous pouvez améliorer les performances lors de la désactivation d’un objet [**RealTimeStylus**](realtimestylus-class.md) . Lorsque la propriété [Enabled](/previous-versions/ms824832(v=msdn.10)) de l’objet **RealTimeStylus** est définie sur **false**, les données des files d’attente d’entrée et de sortie sont traitées jusqu’à ce que les files d’attente soient vides. Vous pouvez appeler la méthode [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) de l’objet **RealTimeStylus** pour effacer les files d’attente avant de désactiver l’objet **RealTimeStylus** .

## <a name="enabled-and-disabled-data"></a>Données activées et désactivées

Lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md) est activé, chaque plug-in reçoit un appel à sa méthode [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) . L’objet **RealTimeStylusEnabledData** passé dans la notification contient une collection d’identificateurs de contexte pour les tablettes disponibles au moment où l’objet **RealTimeStylus** est activé.

> [!Note]  
> Étant donné que les données de plug-in de la collection de plug-in asynchrone de l’objet [**RealTimeStylus**](realtimestylus-class.md) sont mises en file d’attente, les plug-ins asynchrones peuvent recevoir des données avant de recevoir un appel à sa méthode [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) , mais une fois l’objet **RealTimeStylus** désactivé. Notez que certaines des méthodes et propriétés de l’objet **RealTimeStylus** lèvent une exception si l’objet **RealTimeStylus** est désactivé.

 

L’objet [**RealTimeStylus**](realtimestylus-class.md) appelle les méthodes [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) et [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) sur le thread à partir duquel l’objet **RealTimeStylus** est activé ou à partir duquel le plug-in synchrone est ajouté.

En règle générale, ajoutez ou supprimez des plug-ins pendant que l’objet [**RealTimeStylus**](realtimestylus-class.md) est désactivé. Pour plus d’informations sur l’ajout et la suppression de plug-ins à l’objet **RealTimeStylus** , consultez [plug-ins et la classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="tablet-data"></a>Données de tablette

Quand une tablette que l’objet [**RealTimeStylus**](realtimestylus-class.md) peut utiliser est ajoutée ou supprimée du Tablet PC pendant que l’objet **RealTimeStylus** est activé, l’objet **RealTimeStylus** notifie ses plug-ins qu’un objet [tablette](/previous-versions/ms827783(v=msdn.10)) a été ajouté ou supprimé. Chaque objet **RealTimeStylus** gère une liste d’identificateurs uniques pour les objets tablette avec lesquels il peut interagir. L’objet **RealTimeStylus** a deux méthodes pour la traduction entre l’identificateur unique et l’objet Tablet, les méthodes [GetTabletContextIdFromTablet](/previous-versions/ms825922(v=msdn.10)) et [GetTabletFromTabletContextId](/previous-versions/ms825929(v=msdn.10)) .

> [!Note]  
> Les informations sur une tablette ne sont plus disponibles à partir de l’objet [**RealTimeStylus**](realtimestylus-class.md) après la suppression de la tablette du Tablet PC.

 

## <a name="tablet-pen-data"></a>Données du stylet de tablette

L’objet [**RealTimeStylus**](realtimestylus-class.md) passe des informations sur le stylet de tablette à ses plug-ins dans un certain nombre de méthodes de notification. Les informations sur le stylet du Tablet PC sont représentées par un objet [stylet](/previous-versions/ms824824(v=msdn.10)) . Cet objet est un instantané de l’état du stylet du Tablet PC au moment où les données ont été rassemblées. Étant donné que les plug-ins reçoivent les données du stylet dans le flux de données du stylet, les plug-ins doivent utiliser les informations de l’objet stylet au lieu de vérifier l’état actuel d’un stylet de tablette particulier à l’aide de la classe [Cursor](/previous-versions/ms839521(v=msdn.10)) .

Chaque objet [stylet](/previous-versions/ms824824(v=msdn.10)) contient l’identificateur de contexte de tablette pour la tablette qui a généré les données.

## <a name="system-gesture-data"></a>Données de mouvement du système

L’objet [**RealTimeStylus**](realtimestylus-class.md) reçoit des données sur les gestes système lorsqu’ils sont reconnus par le Tablet PC. Le tableau suivant décrit l’ordre dans lequel les objets [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) se produisent dans le flux de données de stylet de tablette par rapport à d’autres données de stylet de tablette.




| <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesture</a> | Objets qui précèdent l’objet <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> | Objets qui viennent après l’objet <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> | 
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <strong>Taper</strong> | Objet <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br /> | Objet [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br /> | 
| <strong>DoubleTap</strong> | L’objet <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> , l’objet <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> pour le mouvement du système <strong>Tap</strong> et les objets [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br /> | Deuxième objet <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br /> | 
| <strong>RightTap</strong> | L’objet <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> et l’objet <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> pour le membre <strong>HoldEnter</strong> de l’énumération <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesure</a> .<br /> | Objet [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br /> | 
| <strong>Déplacez</strong> | Objet <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br /> | Objet [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br /> | 
| <strong>RightDrag</strong> | Objet <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br /> | Objet [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br /> | 
| <strong>HoldEnter</strong> | Objet <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br /> | Objet [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br /><blockquote>[!Note]<br />Ce mouvement système n’est pas reconnu si l’utilisateur commence un mouvement de système <strong>Drag</strong> ou <strong>RightDrag</strong> .</blockquote><br /> | 
| <strong>HoldLeave</strong> | Non implémenté.<br /> | Non implémenté.<br /> | 
| <strong>HoverEnter</strong> | Plusieurs objets <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData</a> de vitesse moyenne faible.<br /> | <blockquote>[!Note]<br />Il peut y avoir un délai notable avant de recevoir le mouvement du système <strong>HoverEnter</strong> . L’objet <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> reçoit uniquement ces données si l’objet <strong>RealTimeStylus</strong> est attaché à la fenêtre ou au contrôle qui se trouve directement sous le stylet au moment du mouvement du système.</blockquote><br /> | 
| <strong>HoverLeave</strong> | Objet <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> pour le mouvement de système <strong>HoverEnter</strong> et plusieurs objets <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData</a> de rapidité moyenne suffisante.<br /> | <blockquote>[!Note]<br />Il peut y avoir un délai notable avant de recevoir le mouvement du système <strong>HoverLeave</strong> . L’objet <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> reçoit uniquement ces données si l’objet <strong>RealTimeStylus</strong> est attaché à la fenêtre ou au contrôle qui se trouve directement sous le stylet au moment du mouvement du système.</blockquote><br /> | 




 

## <a name="custom-stylus-data"></a>Données personnalisées du stylet

Des données de stylet personnalisées peuvent être ajoutées à l’objet [**RealTimeStylus**](realtimestylus-class.md) en appelant la méthode [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) . Les données de stylet personnalisées peuvent être ajoutées aux files d’attente de l’objet **RealTimeStylus** dans l’un des trois emplacements.

-   Lorsque le paramètre de *file d’attente* a la valeur **Output**, les données personnalisées sont ajoutées à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) après les données en cours de traitement par la collection de plug-ins synchrone.
-   Lorsque le paramètre de *file d’attente* a la valeur **OutputImmediate**, les données personnalisées sont ajoutées à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) avant les données en cours de traitement par la collection de plug-ins synchrone.
-   Lorsque le paramètre de *file d’attente* est défini sur **Input**, les données personnalisées sont ajoutées à la file d’attente d’entrée de l’objet [**RealTimeStylus**](realtimestylus-class.md) et sont envoyées à la collection de plug-ins synchrone avant les nouvelles données du flux de données du stylet du Tablet PC.

Dans chacun des cas précédents, les données ajoutées par les plug-ins suivants dans la collection de plug-in synchrone sont ajoutées après les données ajoutées par les plug-ins précédents.

> [!Note]  
> Si l’appel à la méthode [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) est effectué à partir d’un plug-in synchrone en réponse à un appel à l’une de ses méthodes [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) , les données de stylet personnalisées sont ajoutées au flux de données du stylet de tablette de manière prévisible ; dans le cas contraire, il est ajouté à la file d’attente par rapport aux données de stylet actuelles que l’objet [**RealTimeStylus**](realtimestylus-class.md) traite, et non par rapport aux données traitées par le plug-in asynchrone. La méthode AddCustomStylusDataToQueue lève une exception si l’objet **RealTimeStylus** est désactivé.

 

Les données de stylet personnalisées sont ajoutées à la file d’attente en tant qu’objet [CustomStylusData](/previous-versions/ms824747(v=msdn.10)) et les plug-ins reçoivent ces données par le biais de leur méthode [Microsoft. StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. CustomStylusDataAdded](/previous-versions/ms824770(v=msdn.10)) .

Les objets [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) et [**GestureRecognizer**](gesturerecognizer-class.md) peuvent ajouter des données de stylet personnalisées à la file d’attente. Pour plus d’informations sur le **DynamicRenderer** et les objets **GestureRecognizer** , consultez Plug- [ins de rendu dynamique](dynamic-renderer-plug-ins.md) et [plug-ins de reconnaissance](recognizer-plug-ins.md).

L’objet [**RealTimeStylus**](realtimestylus-class.md) appelle la méthode [Microsoft. StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) sur le thread à partir duquel il reçoit l’appel à sa méthode [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) .

Le diagramme suivant illustre l’ajout de données de stylet personnalisées à la file d’attente de sortie avec le paramètre de *file d’attente* défini sur **Output**.

![Illustration montrant un flot de données de stylet personnalisé vers la file d’attente de sortie ](images/27bc3672-41bc-432e-bf41-18e4ccec78f5.gif)

Dans ce diagramme, les cercles « A » et « B » représentent les données du stylet de tablette qui ont déjà été ajoutées à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) et qui n’ont pas encore été envoyées à la collection de plug-in asynchrone. Le cercle « C » indique les données du stylet du Tablet PC actuellement traitées par l’objet **RealTimeStylus** . Il est envoyé à la collection de plug-ins synchrone et placé dans la file d’attente de sortie. Les cercles numérotés « 1 », « 2 » et « 3 » représentent les données personnalisées du stylet qui ont été ajoutées à la file d’attente de sortie par les premier, deuxième et troisième plug-ins synchrones, respectivement en réponse aux données du stylet de tablette représentées par « C ». Les plug-ins ont ajouté les données de stylet personnalisées avec le paramètre de *file d’attente* défini sur **StylusQueues**. Le cercle vide représente la position dans la file d’attente de sortie où les futures données de stylet du Tablet PC sont ajoutées.

Le diagramme suivant illustre l’ajout de données de stylet personnalisées à la file d’attente de sortie avec le paramètre de *file d’attente* défini sur **OutputImmediate**.

![Diagramme qui montre le flot de données personnalisé du stylet vers la file d’attente de sortie.](images/bcf45325-5557-47a2-af43-142c7684e482.gif)

Dans ce diagramme, les cercles « A » et « B » représentent les données du stylet de tablette qui ont déjà été ajoutées à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) et qui n’ont pas encore été envoyées à la collection de plug-in asynchrone. Le cercle « C » indique les données du stylet du Tablet PC actuellement traitées par l’objet **RealTimeStylus** . Il est envoyé à la collection de plug-ins synchrone et placé dans la file d’attente de sortie. Les cercles numérotés « 1 », « 2 » et « 3 » représentent les données personnalisées du stylet qui ont été ajoutées à la file d’attente de sortie par les premier, deuxième et troisième plug-ins synchrones, respectivement en réponse aux données du stylet de tablette représentées par « C ». Les plug-ins ont ajouté les données de stylet personnalisées avec le paramètre de *file d’attente* défini sur **OutputImmediate**. Le cercle vide représente la position dans la file d’attente de sortie où les futures données de stylet du Tablet PC sont ajoutées.

Le diagramme suivant illustre l’ajout de données de stylet personnalisées à la file d’attente d’entrée.

![Illustration montrant un flot de données de stylet personnalisé vers la file d’attente de sortie](images/5dd2cfcc-1086-49b0-a0d5-9276c13c7f61.gif)

Dans ce diagramme, les cercles « A » et « B » représentent les données du stylet de tablette qui ont déjà été ajoutées à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) et qui n’ont pas encore été envoyées à la collection de plug-in asynchrone. Le cercle « C » indique les données du stylet du Tablet PC actuellement traitées par l’objet **RealTimeStylus** . Il est envoyé à la collection de plug-ins synchrone et placé dans la file d’attente de sortie. Les cercles numérotés « 1 », « 2 » et « 3 » représentent les données personnalisées du stylet qui ont été ajoutées à la file d’attente d’entrée par les premier, deuxième et troisième plug-ins synchrones, respectivement en réponse aux données du stylet de tablette représentées par « C ». Les plug-ins ont ajouté les données de stylet personnalisées avec le paramètre de *file d’attente* défini sur **entrée**. Les données personnalisées du stylet numérotées « 1 » sont ensuite transmises aux plug-ins synchrones, puis à la file d’attente de sortie avant le traitement des données personnalisées du stylet « 2 » et « 3 », les deux étant traitées avant le traitement des données du stylet de tablette suivant. Le cercle vide représente la position dans la file d’attente de sortie où les futures données de stylet du Tablet PC sont ajoutées.

## <a name="error-data"></a>Données d’erreur

Lorsqu’un plug-in lève une exception, le workflow normal de données est interrompu. L’objet [**RealTimeStylus**](realtimestylus-class.md) génère un objet [ErrorData](/previous-versions/ms824740(v=msdn.10)) et appelle :

-   Méthode [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) du plug-in qui a levé l’exception.
-   Méthode [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) des plug-ins restants de cette collection.

Si le plug-in qui a levé l’exception est un plug-in synchrone, l’objet [ErrorData](/previous-versions/ms824740(v=msdn.10)) est ajouté à la file d’attente de sortie. L’objet [**RealTimeStylus**](realtimestylus-class.md) reprend ensuite le traitement normal des données d’origine.

Le diagramme suivant illustre l’ajout de données d’erreur aux données du stylet de tablette.

![transmission de données de stylet personnalisées vers la file d’attente de sortie avec ajout de données d’erreur](images/c2f79abe-aeb5-498f-b389-1fad9bf01a13.gif)

Dans ce diagramme, les cercles « A » et « B » représentent les données du stylet de tablette qui ont déjà été ajoutées à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) et qui n’ont pas encore été envoyées à la collection de plug-in asynchrone. Le cercle « C » indique les données du stylet du Tablet PC actuellement traitées par l’objet **RealTimeStylus** . Le cercle « e » représente un objet [ErrorData](/previous-versions/ms824740(v=msdn.10)) généré par l’objet **RealTimeStylus** lorsque le second plug-in synchrone, plug-in 2, lève une exception pendant qu’il traite « C ». L’objet **RealTimeStylus** interrompt ensuite son traitement de « C » et passe « e » au plug-in qui a généré l’exception et tous les plug-ins suivants. L’objet **RealTimeStylus** place ensuite « e » dans la file d’attente de sortie et reprend son traitement de « C », qui est passé aux plug-ins restants dans la collection de plug-in synchrone et est placé dans la file d’attente de sortie après « e ». Le cercle vide représente la position dans la file d’attente de sortie où les futures données de stylet du Tablet PC sont ajoutées.

Si un plug-in lève une exception à partir de sa méthode d’erreur, l’objet [**RealTimeStylus**](realtimestylus-class.md) intercepte l’exception, mais ne génère pas de nouvel objet [ErrorData](/previous-versions/ms824740(v=msdn.10)) . Cela permet d’éviter la récursivité.

Les données d’erreur sont ajoutées à la file d’attente de sortie après toute donnée de stylet personnalisée ajoutée à la position **OutputImmediate** avant l’exception qui a créé les données d’erreur et avant les données de stylet personnalisées ajoutées à la position **OutputImmediate** par les plug-ins suivants dans la collection de plug-ins synchrone.

Le diagramme suivant illustre la façon dont les données d’erreur sont ajoutées à la file d’attente de sortie par rapport aux données personnalisées ajoutées à la file d’attente **OutputImmediate** .

![données d’erreur ajoutées à la file d’attente de sortie par rapport aux données personnalisées ajoutées à la file d’attente OutputImmediate.](images/b00320c4-6fe7-439d-9855-e5f131feeb69.gif)

Dans ce diagramme, les cercles « A » et « B » représentent les données du stylet de tablette qui ont déjà été ajoutées à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) et qui n’ont pas encore été envoyées à la collection de plug-in asynchrone. Le cercle « C » indique les données du stylet du Tablet PC actuellement traitées par l’objet **RealTimeStylus** . Les cercles numérotés « 1 », « 2 » et « 3 » sont ajoutés respectivement par le premier, le deuxième et le troisième plug-ins synchrones à la file d’attente **OutputImmediate** en réponse aux données représentées par le cercle lettre « C ». Le cercle « e » indique les données d’erreur générées en réponse à une exception levée par le second plug-in après que le second plug-in a ajouté des données personnalisées à la file d’attente de sortie à la position **OutputImmediate** .

Si un plug-in synchrone ajoute des données de stylet personnalisées à la file d’attente d’entrée en réponse aux données d’erreur, les données sont ajoutées immédiatement avant les données d’erreur. Si l’un des plug-ins synchrones ajoute des données de stylet personnalisées à la file d’attente de sortie à la position de **sortie** en réponse aux données d’erreur, les données sont ajoutées immédiatement après les données d’erreur.

L’objet [**RealTimeStylus**](realtimestylus-class.md) appelle la méthode [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) sur le thread à partir duquel l’exception est levée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft. Ink. Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Utilisation de la classe RealTimeStylus](working-with-the-realtimestylus-class.md)
</dt> </dl>

 

 
