---
description: Un plug-in de module de reconnaissance est un objet qui surveille le mouvement du stylet pour le mouvement, l’écriture manuscrite ou d’autres objets.
ms.assetid: 764a327e-1da0-487f-9245-b6a4f3f43502
title: Plug-ins de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf3ac866a211a78e2d8f347e89ca20a1906f436
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411450"
---
# <a name="recognizer-plug-ins"></a>Plug-ins de reconnaissance

Un plug-in de module de reconnaissance est un objet qui surveille le mouvement du stylet pour le mouvement, l’écriture manuscrite ou d’autres objets.

## <a name="system-gestures"></a>Gestes système

L’objet [**RealTimeStylus**](realtimestylus-class.md) reconnaît les gestes système. L’objet **RealTimeStylus** ajoute un objet [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) à la file d’attente [StylusQueues](/previous-versions/ms824786(v=msdn.10)) en réponse aux données qui terminent le mouvement, par exemple un objet [StylusUpData](/previous-versions/ms824057(v=msdn.10)) pour [SystemGesture](/previous-versions/bb345349(v=vs.100)). Pour plus d’informations, consultez [données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-gesturerecognizer-object"></a>Objet GestureRecognizer

L’objet [**GestureRecognizer**](gesturerecognizer-class.md) implémente les interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) et [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . L’objet **GestureRecognizer** reconnaît les gestes d’application. En interne, l’objet **GestureRecognizer** utilise le module de reconnaissance de mouvement Microsoft pour effectuer la reconnaissance de mouvement.

Lorsque l’objet [**GestureRecognizer**](gesturerecognizer-class.md) reconnaît un mouvement, il ajoute des données de stylet personnalisées à la file d’attente [StylusQueues](/previous-versions/ms824786(v=msdn.10)) en réponse à l’objet [StylusUpData](/previous-versions/ms824057(v=msdn.10)) pour le trait. La propriété [CustomDataId](/previous-versions/ms824748(v=msdn.10)) de l’objet [CustomStylusData](/previous-versions/ms575208(v=vs.100)) est définie sur la valeur [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) et la propriété [Data](/previous-versions/ms824749(v=msdn.10)) de l’objet CustomStylusData contient un objet [GestureRecognitionData](/previous-versions/ms824594(v=msdn.10)) .

Le diagramme suivant illustre la façon dont l’objet [**GestureRecognizer**](gesturerecognizer-class.md) ajoute des données aux données du stylet de tablette.

![illustration du GestureRecognizer Data Flow](images/c4c77c33-deee-49d0-84bc-12612575ec66.gif)

Dans ce diagramme, le cercle « SD » représente un objet [StylusDownData](/previous-versions/ms824107(v=msdn.10)) et les cercles « P » représentent des objets [PacketsData](/previous-versions/ms824590(v=msdn.10)) qui ont déjà été ajoutés à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) et qui n’ont pas encore été envoyés à la collection de plug-ins asynchrone. Le cercle « SU » est représenté par un objet [StylusUpData](/previous-versions/ms824057(v=msdn.10)) que l’objet **RealTimeStylus** est en train de traiter. Il est envoyé à la collection de plug-ins synchrone, puis placé dans la file d’attente de sortie. Les cercles « GR » représentent les données personnalisées du stylet qui sont ajoutées à la file d’attente d’entrée par le plug-in [**GestureRecognizer**](gesturerecognizer-class.md) en réponse à la notification du stylet associée à « su ». Les données de stylet personnalisées « GR » sont ensuite transmises aux plug-ins synchrones, puis à la file d’attente de sortie avant le traitement des données du stylet de tablette suivant. Le cercle vide représente la position dans la file d’attente de sortie où les futures données de stylet du Tablet PC sont ajoutées.

Par défaut, l’objet [**GestureRecognizer**](gesturerecognizer-class.md) reconnaît uniquement les gestes à un seul trait ; Toutefois, l’objet **GestureRecognizer** peut être défini pour reconnaître les gestes multitraits. Pour les gestes multitraits, l’objet [CustomStylusData](/previous-versions/ms575208(v=vs.100)) est ajouté à la file d’attente [StylusQueues](/previous-versions/ms824786(v=msdn.10)) en réponse à l’objet [StylusUpData](/previous-versions/ms824057(v=msdn.10)) pour le trait final du mouvement. Lors de la reconnaissance de mouvements à traits, vous pouvez recevoir des notifications pour les jeux de traits qui se chevauchent. Par exemple, les premier et deuxième traits ensemble peuvent être reconnus comme un mouvement et le deuxième trait seul peut être reconnu comme un geste. Pour plus d’informations sur la reconnaissance des mouvements multitraits, consultez la classe **GestureRecognizer** et la propriété [MaxStrokeCount](/previous-versions/ms826053(v=msdn.10)) .

Si vous utilisez l’objet [**GestureRecognizer**](gesturerecognizer-class.md) pour la reconnaissance de mouvement multitrait, vous pouvez obtenir des performances optimales en utilisant un modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade et en joignant l’objet **GestureRecognizer** à l’objet **RealTimeStylus** secondaire. Pour plus d’informations sur le modèle **RealTimeStylus** en cascade, consultez [le modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md).

### <a name="special-considerations"></a>Considérations spéciales

La liste suivante décrit d’autres points à prendre en compte lors de l’utilisation de l’objet [**GestureRecognizer**](gesturerecognizer-class.md) .

-   Vous ne devez pas attacher un objet [**GestureRecognizer**](gesturerecognizer-class.md) à plusieurs objets [**RealTimeStylus**](realtimestylus-class.md) . Une fois que deux objets **RealTimeStylus** auxquels l’objet **GestureRecognizer** est attaché sont activés, les éléments suivants se produisent.
    -   L’objet [**GestureRecognizer**](gesturerecognizer-class.md) lève une exception en réponse au deuxième appel à sa méthode RealTimeStylusEnabled.
    -   Le deuxième objet [**RealTimeStylus**](realtimestylus-class.md) qui a été activé génère un objet [ErrorData](/previous-versions/ms824740(v=msdn.10)) et notifie les autres plug-ins dans ses collections de plug-ins de l’erreur.
    -   L’objet [**GestureRecognizer**](gesturerecognizer-class.md) arrête de reconnaître les gestes.
-   L’objet [**RealTimeStylus**](realtimestylus-class.md) lève une exception lorsque sa méthode [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) est appelée avec le paramètre *GUID* défini sur l’identificateur global unique (Guid) [Microsoft. StylusInput. GestureRecognizer. GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) .
-   L’objet [**GestureRecognizer**](gesturerecognizer-class.md) est implémenté en tant que wrapper COM (Component Object Model) et vous ne pouvez pas appeler directement ses méthodes d’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Pour plus d’informations sur l’implémentation COM et l’objet [**RealTimeStylus**](realtimestylus-class.md) , consultez [Remarques d’implémentation pour les API StylusInput](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-gesture-recognition"></a>Reconnaissance personnalisée des mouvements

Vous pouvez créer un plug-in de reconnaissance personnalisé qui reconnaît l’écriture manuscrite, les gestes ou d’autres objets en procédant comme suit :

-   Passage des informations de trait à un objet de module de [reconnaissance](/previous-versions/ms829434(v=msdn.10)) existant et utilisation de la méthode [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) pour ajouter les résultats au flux de données de stylet de tablette.
-   La reconnaissance au sein de votre plug-in et l’utilisation de la méthode [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) pour ajouter les résultats au flux de données du stylet de tablette.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mouvements d’application](application-gestures.md)
</dt> <dt>

[Gestes système](system-gestures.md)
</dt> <dt>

[Chronologie des messages de la souris et des événements système](timeline-of-mouse-messages-and-system-events.md)
</dt> </dl>

 

 
