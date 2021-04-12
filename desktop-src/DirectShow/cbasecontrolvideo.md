---
description: La classe CBaseControlVideo implémente l’interface IBasicVideo et contrôle les propriétés vidéo d’une fenêtre vidéo générique. En règle générale, un objet CBaseControlVideo est un convertisseur vidéo qui dessine une vidéo dans une fenêtre à l’écran.
ms.assetid: 16fc1b0a-e5b5-4f33-ac2b-5acff61bab81
title: CBaseControlVideo, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo
api_type:
- COM
api_location: ''
ms.openlocfilehash: e2e5962eb9d175bfbbeadd149a547f0d36fbf49f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482209"
---
# <a name="cbasecontrolvideo-class"></a>CBaseControlVideo, classe

![hiérarchie de la classe cbasecontrolvideo](images/wctrl02.png)

La classe **CBaseControlVideo** implémente l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) et contrôle les propriétés vidéo d’une fenêtre vidéo générique. En règle générale, un objet **CBaseControlVideo** est un convertisseur vidéo qui dessine une vidéo dans une fenêtre à l’écran.

De nombreuses fonctions membres **CBaseControlVideo** requièrent uniquement que le convertisseur vidéo soit connecté à un graphique de filtre. S’il n’est pas connecté, les fonctions membres retournent **VFW \_ E \_ non \_ connecté**. Les propriétés définies sur un convertisseur vidéo sont conservées entre les connexions successives et les déconnexions. Toutes les applications doivent s’assurer qu’elles réinitialisent les propriétés du convertisseur avant de démarrer une présentation.

Lorsque vous utilisez la vidéo, l’application peut sélectionner une partie de la vidéo à utiliser. Cette partie est le rectangle source que l’objet **CBaseControlVideo** contrôle. **CBaseControlVideo** permet à votre application de définir et de récupérer le rectangle source. Tous les rectangles utilisés par **CBaseControlVideo** utilisent des valeurs de largeur et de hauteur plutôt que des valeurs à droite et en bas. Quand aucun rectangle source n’a été défini, les propriétés du rectangle source retournent la taille vidéo native complète.



| Membres de données protégés                                                                   | Description                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| m \_ pFilter                                                                               | Pointeur vers un filtre de média propriétaire.                                                              |
| m \_ pInterfaceLock                                                                        | Section critique définie de manière externe.                                                            |
| m \_ pPin                                                                                  | Contrôle des types de médias pour la connexion.                                                      |
| Fonctions de membre                                                                         | Description                                                                                     |
| [**CBaseControlVideo**](cbasecontrolvideo-cbasecontrolvideo.md)                         | Construit un objet **CBaseControlVideo** .                                                      |
| [**CopyImage**](cbasecontrolvideo-copyimage.md)                                         | Crée une copie de mémoire d’une image vidéo.                                                         |
| [**GetImageSize**](cbasecontrolvideo-getimagesize.md)                                   | Récupère des informations sur la taille de l’image vidéo.                                                         |
| [**SetControlVideoPin**](cbasecontrolvideo-setcontrolvideopin.md)                       | Définit le code confidentiel avec lequel cet objet doit se synchroniser.                                         |
| Fonctions membres substituables                                                             | Description                                                                                     |
| [**CheckSourceRect**](cbasecontrolvideo-checksourcerect.md)                             | Détermine si un rectangle source est valide.                                                      |
| [**CheckTargetRect**](cbasecontrolvideo-checktargetrect.md)                             | Détermine si un rectangle cible est valide.                                                      |
| [**GetSourceRect**](cbasecontrolvideo-getsourcerect.md)                                 | Récupère le rectangle vidéo source actuel (virtuel pur).                                    |
| [**GetStaticImage**](cbasecontrolvideo-getstaticimage.md)                               | Retourne l’image actuelle dans une mémoire tampon (virtuelle pure).                                    |
| [**GetTargetRect**](cbasecontrolvideo-gettargetrect.md)                                 | Récupère le rectangle vidéo cible actuel (virtuel pur).                                    |
| [**GetVideoFormat**](cbasecontrolvideo-getvideoformat.md)                               | Récupère la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contenant le format vidéo. |
| [**IsDefaultSourceRect**](cbasecontrolvideo-isdefaultsourcerect.md)                     | Détermine si le convertisseur utilise le rectangle source par défaut (virtuel pur).                |
| [**IsDefaultTargetRect**](cbasecontrolvideo-isdefaulttargetrect.md)                     | Détermine si le convertisseur utilise le rectangle cible par défaut (virtuel pur).                |
| [**OnUpdateRectangles**](cbasecontrolvideo-onupdaterectangles.md)                       | Appelé lorsque le rectangle source ou cible change.                                             |
| [**OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)                         | Transmet \_ \_ la taille vidéo \_ de ce passé à l’application.                                             |
| [**SetDefaultSourceRect**](cbasecontrolvideo-setdefaultsourcerect.md)                   | Définit le rectangle de la vidéo source par défaut (virtuel pur).                                         |
| [**SetDefaultTargetRect**](cbasecontrolvideo-setdefaulttargetrect.md)                   | Définit le rectangle vidéo cible par défaut (virtuel pur).                                         |
| [**SetSourceRect**](cbasecontrolvideo-setsourcerect.md)                                 | Définit le rectangle vidéo source actuel (virtuel pur).                                         |
| [**SetTargetRect**](cbasecontrolvideo-settargetrect.md)                                 | Définit le rectangle cible actuel (virtuel pur).                                               |
| Méthodes IBasicVideo                                                                      | Description                                                                                     |
| [**Obtient \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)                    | Récupère une durée moyenne approximative par frame.                                                |
| [**Obtient \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)                          | Récupère un taux d’erreur de bit approximatif.                                                        |
| [**Obtient le \_ débit binaire**](cbasecontrolvideo-get-bitrate.md)                                    | Récupère une vitesse de transmission approximative de la vidéo.                                                |
| [**GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)                             | Récupère un rendu de mémoire de l’image actuelle.                                              |
| [**Obtient \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)                | Récupère la hauteur du rectangle de destination actuel.                                           |
| [**Obtient \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)                    | Récupère la coordonnée gauche du rectangle de destination actuel.                                  |
| [**GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)               | Récupère la position de destination actuelle.                                                     |
| [**Obtient \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)                      | Récupère la coordonnée supérieure du rectangle de destination actuel.                                   |
| [**Obtient \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)                  | Récupère la largeur du rectangle de destination actuel.                                            |
| [**Obtient \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)                          | Récupère la hauteur du rectangle source actuel.                                                |
| [**Obtient \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)                              | Récupère la coordonnée gauche du rectangle source actuel.                                       |
| [**GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)                         | Récupère la position de la source actuelle.                                                          |
| [**Obtient \_ sourceTop**](cbasecontrolvideo-get-sourcetop.md)                                | Récupère la coordonnée supérieure du rectangle source actuel.                                        |
| [**Obtient \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)                            | Récupère la largeur du rectangle source actuel.                                                 |
| [**Obtient \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)                            | Récupère la hauteur vidéo native.                                                              |
| [**GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)               | Récupère une plage d’entrées de palette pour la vidéo.                                             |
| [**GetVideoSize**](cbasecontrolvideo-getvideosize.md)                                   | Récupère la largeur et la hauteur de la vidéo native.                                             |
| [**Obtient \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)                              | Récupère la largeur vidéo native.                                                               |
| [**IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md)         | Détermine si le convertisseur utilise la fenêtre de destination par défaut.                             |
| [**IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md)                   | Détermine si le convertisseur utilise la fenêtre source par défaut.                                  |
| [**put \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)                | Définit la hauteur du rectangle de destination.                                                        |
| [**put \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)                    | Définit la coordonnée gauche du rectangle de destination.                                               |
| [**put \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)                      | Définit la coordonnée supérieure du rectangle de destination.                                                |
| [**put \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)                  | Définit la largeur du rectangle de destination.                                                         |
| [**put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)                          | Définit la hauteur du rectangle source.                                                             |
| [**put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)                              | Définit la coordonnée gauche du rectangle source.                                                    |
| [**put \_ sourceTop**](cbasecontrolvideo-put-sourcetop.md)                                | Définit la coordonnée supérieure du rectangle source.                                                     |
| [**put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)                            | Définit la largeur du rectangle source.                                                              |
| [**SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) | Rétablit la position par défaut de la destination.                                                    |
| [**SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)           | Rétablit la position de la source par défaut.                                                         |
| [**SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)               | Définit la position du rectangle de destination.                                                        |
| [**SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)                         | Définit la position du rectangle source.                                                             |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes de base DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 



