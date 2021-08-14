---
description: Interfaces pour les Services d’édition DirectShow
ms.assetid: e7fdb387-83b3-4fa2-9608-2f5dc95975bf
title: Interfaces pour les Services d’édition DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e913ec6bf17a11a4b772d288b9404113cd6bdc70bf441ed20dcbc69a086f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397590"
---
# <a name="interfaces-for-directshow-editing-services"></a>Interfaces pour les Services d’édition DirectShow

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

cette section contient des rubriques de référence sur les interfaces des [Services d’édition de DirectShow](directshow-editing-services.md) .



| Interface                                                  | Description                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IAMErrorLog**](iamerrorlog.md)                         | Fournit une méthode de rappel pour la journalisation des erreurs.                                                                                  |
| [**IAMSetErrorLog**](iamseterrorlog.md)                   | Définit ou récupère un journal des erreurs.                                                                                                |
| [**IAMTimeline**](iamtimeline.md)                         | Fournit des méthodes pour manipuler la chronologie.                                                                                |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Insère ou récupère des pistes virtuelles sur une composition.                                                                          |
| [**IAMTimelineEffect**](iamtimelineeffect.md)             | Fournit des méthodes pour manipuler les effets de la chronologie.                                                                            |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | Fournit des méthodes pour ajouter des effets à un objet Timeline.                                                                      |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Définit et récupère des propriétés sur des groupes.                                                                                       |
| [**IAMTimelineObj**](iamtimelineobj.md)                   | Fournit des méthodes pour manipuler des objets Timeline.                                                                            |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | Fractionne un objet Timeline.                                                                                                      |
| [**IAMTimelineSrc**](iamtimelinesrc.md)                   | Fournit des méthodes pour manipuler et définir des propriétés sur les objets sources.                                                    |
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Fournit des méthodes pour manipuler des objets Track.                                                                               |
| [**IAMTimelineTrans**](iamtimelinetrans.md)               | Fournit des méthodes pour manipuler des objets de transition.                                                                          |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | Ajoute des transitions à un objet.                                                                                                 |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Fournit des méthodes pour travailler avec des pistes virtuelles.                                                                              |
| [**IDxtAlphaSetter**](idxtalphasetter.md)                 | Définit des propriétés sur l’effet d' [accesseur Set alpha](alpha-setter-effect.md) .                                                         |
| [**IDxtCompositor**](idxtcompositor.md)                   | Définit les propriétés de la transition du [compositeur](compositor-transition.md) .                                                     |
| [**IDxtJpeg**](idxtjpeg.md)                               | Définit les propriétés de la transition de [réinitialisation SMPTE](smpte-wipe-transition.md) .                                                     |
| [**IDxtKey**](idxtkey.md)                                 | Définit les propriétés de la transition de [clé](key-transition.md) .                                                                   |
| [**IFindCompressorCB**](ifindcompressorcb.md)             | Non pris en charge.                                                                                                                 |
| [**IGrfCache**](igrfcache.md)                             | Non pris en charge.                                                                                                                 |
| [**IMediaDet**](imediadet.md)                             | Récupère des informations sur un fichier multimédia, telles que le nombre de flux et le type, la durée et la fréquence d’images de chaque flux. |
| [**IMediaLocator**](imedialocator.md)                     | Fournit des méthodes pour valider des noms de fichiers.                                                                                    |
| [**IPropertySetter**](ipropertysetter.md)                 | Définit des propriétés sur un effet ou une transition.                                                                                    |
| [**IRenderEngine**](irenderengine.md)                     | Restitue un projet DES en construisant un graphique de filtre à partir d’une chronologie.                                                          |
| [**IRenderEngine2**](irenderengine2.md)                   | Permet à l’application de remplacer le filtre de redimensionnement vidéo par défaut utilisé par DES.                                              |
| [**IResize**](iresize.md)                                 | Doit être pris en charge par un filtre de redimensionnement vidéo personnalisé.                                                                          |
| [**ISampleGrabber**](isamplegrabber.md)                   | Récupère des échantillons de médias individuels lorsqu’ils se déplacent dans le graphique de filtre.                                                      |
| [**ISampleGrabberCB**](isamplegrabbercb.md)               | Interface de rappel de l’interface [**ISampleGrabber**](isamplegrabber.md) .                                                 |
| [**ISmartRenderEngine**](ismartrenderengine.md)           | Fournit des méthodes qui prennent en charge la recompression intelligente.                                                                             |
| [**IXml2Dex**](ixml2dex.md)                               | Enregistre et charge les fichiers projet DES dans Extensible Markup Language (XML).                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Référence C++ des services de modification](directshow-editing-services-c---reference.md)
</dt> </dl>

 

 



