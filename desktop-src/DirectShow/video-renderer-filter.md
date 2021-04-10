---
description: Filtre de convertisseur vidéo
ms.assetid: 7719ed9d-e3b9-4c84-b587-4e120b5cabf8
title: Filtre de convertisseur vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71e72375a43a57ce94b38d01f48abba9309e603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201838"
---
# <a name="video-renderer-filter"></a>Filtre de convertisseur vidéo

Le filtre de convertisseur vidéo est un convertisseur vidéo robuste et polyvalent.

> [!Note]  
> Sur Windows XP et versions ultérieures, le convertisseur vidéo par défaut est le [filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7). VMR-7 et le convertisseur vidéo ont tous les deux le nom convivial « Render vidéo ». Sur les plateformes antérieures, le convertisseur vidéo est le convertisseur par défaut. Consultez [choix du convertisseur approprié](choosing-the-right-renderer.md).

 

Le convertisseur vidéo utilise DirectDraw et des surfaces de recouvrement, si la carte vidéo les prend en charge. Le gestionnaire de graphique de filtre expose l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , qui permet aux applications de définir et de récupérer des propriétés sur le convertisseur vidéo. Avec les cartes vidéo plus récentes, le convertisseur vidéo prend en charge le rendu plein écran. Dans le cas contraire, le gestionnaire de graphique de filtre bascule automatiquement vers le filtre de [convertisseur plein écran](full-screen-renderer-filter.md) pour le mode plein écran. Pour plus d’informations, consultez [**IVideoWindow ::p ut \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode) .

-   \[! Précieuse\]  
    > Normalement, la fenêtre vidéo de ce filtre traite les messages sur un thread de travail créé par le gestionnaire de graphique de filtre. Cependant, si une application crée directement le filtre à l’aide de **CoCreateInstance**, la fenêtre vidéo traite les messages sur le thread d’application. Dans ce cas, le thread d’application doit avoir une boucle de message pour distribuer les messages dans la fenêtre vidéo. En outre, le thread ne doit pas quitter jusqu’à l’appel de la **version** finale du convertisseur vidéo, qui se produit lorsque le gestionnaire de graphique de filtre s’arrête. Dans le cas contraire, l’application peut se bloquer.

     



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2), [**IDirectDrawVideo**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo), [**IKsPropertySet**](ikspropertyset.md), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) |
| Types de média de broche d’entrée                    | Formats vidéo non compressés.                                                                                                                                                                                                                                                                                                                                                                              |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                           |
| Types de média de broche de sortie                   | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                          |
| Interfaces de broche de sortie                    | Non applicable.                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID du filtre                             | CLSID \_ VideoRenderer                                                                                                                                                                                                                                                                                                                                                                                     |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                                                                                                                                                                                                                                                                                                                                        |
| Exécutable                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                                               |
| [Mérite](merit.md)                       | Windows XP et versions ultérieures : **méritent \_ peu probable**                                                                                                                                                                                                                                                                                                                                                                |
| [Catégorie de filtre](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Notes

Dans la version Debug de Quartz.dll, si le \_ niveau de débogage de trace du journal est défini à 5 ou plus, le convertisseur vidéo affiche les horodatages de chaque image dans la fenêtre vidéo. Ces chiffres n’apparaissent pas dans la version commercialisée de la DLL. Pour plus d’informations, consultez [fonctions de sortie de débogage](debug-output-functions.md).

Les remarques suivantes sont destinées aux développeurs de filtres :

Le convertisseur vidéo accepte les formats YUV si la carte vidéo graphique prend en charge les surfaces de recouvrement YUV. Toutefois, lorsqu’il se connecte pour la première fois au filtre en amont, le convertisseur vidéo requiert un format RVB qui correspond à la profondeur des couleurs des paramètres actuels de l’analyse. Par exemple, si le paramètre d’affichage actuel est couleur 24 bits, le filtre en amont doit être en mesure de fournir une vidéo RGB de 24 bits. Lorsque le graphique de filtre passe à l’État en exécution, le convertisseur vidéo négocie une modification de format dynamique vers l’espace de couleurs YUV approprié.

En se connectant avec un type RGB, le convertisseur vidéo s’assure qu’il peut utiliser GDI au cas où DirectDraw n’est pas disponible. Il bascule sur GDI si une autre application utilise la mémoire vidéo, si le rectangle vidéo chevauche deux moniteurs sur un système à plusieurs écrans, ou si le rectangle vidéo est complètement masqué par une autre fenêtre.

> [!Note]  
> Le convertisseur de mixage vidéo n’effectue pas ce type de modification de format dynamique et ne nécessite pas de type de média RVB, car il n’utilise jamais GDI pour le rendu.

 

Pour négocier une modification de format, le convertisseur vidéo appelle [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) avec le nouveau type de média. Si le filtre amont retourne la valeur \_ OK, le convertisseur vidéo joint le nouveau support à l’exemple suivant. Le filtre amont doit appeler [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) sur chaque échantillon. Si **GetMediaType** retourne une valeur non **null** , il indique une modification de format et le filtre amont doit répondre en basculant les types de sortie. (Ne pas basculer entre les types dans la méthode **QueryAccept** .) Le filtre amont doit accepter au moins les types RVB principaux et, idéalement, doit prendre en charge les types YUV courants. Pendant la diffusion en continu, le convertisseur vidéo peut basculer entre les types YUV et RVB un nombre quelconque de fois. Le convertisseur vidéo n’accepte pas les modifications de format dynamique initiées par le filtre amont.

Quand le convertisseur vidéo dessine sur une surface de superposition DirectDraw, il alloue une seule mémoire tampon pour sa broche d’entrée. Si le filtre amont tente de forcer une connexion à l’aide de plusieurs mémoires tampons, le convertisseur vidéo ne pourra pas utiliser la surface de recouvrement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



