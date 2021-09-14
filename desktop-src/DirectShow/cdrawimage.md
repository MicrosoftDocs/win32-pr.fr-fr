---
description: La classe CDrawImage est une classe d’assistance qui gère le dessin d’un filtre de convertisseur vidéo.
ms.assetid: 7a6b3726-dbf5-4b60-8cf1-42034a321293
title: CDrawImage, classe (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 001b91338b2956f663d777cbc9597fa2d9a478f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999251"
---
# <a name="cdrawimage-class"></a>CDrawImage, classe

La `CDrawImage` classe est une classe d’assistance qui gère le dessin pour un filtre de convertisseur vidéo. Toutes les opérations de dessin sont effectuées à l’aide de GDI. Cette classe ne fournit aucune prise en charge pour le rendu avec DirectDraw. La `CDrawImage` classe exige que le filtre propriétaire utilise également la classe [**CBaseWindow**](cbasewindow.md) , qui gère la fenêtre vidéo. Le `CDrawImage` constructeur prend un pointeur vers l’objet **CBaseWindow** .

Le diagramme suivant illustre la méthode recommandée pour utiliser cette classe dans un filtre de convertisseur vidéo personnalisé.

![convertisseur vidéo personnalisé à l’aide de cdrawimage](images/videorenderer.png)

Pour utiliser cette classe, procédez comme suit :

-   Lorsque les codes confidentiels se connectent, appelez les méthodes [**CDrawImage :: NotifyMediaType**](cdrawimage-notifymediatype.md) et [**CDrawImage :: NotifyAllocator**](cdrawimage-notifyallocator.md) .
-   Chaque fois que le type de média change, appelez à nouveau **NotifyMediaType** .
-   Avant tout rendu, appelez [**CDrawImage :: SetDrawContext**](cdrawimage-setdrawcontext.md).
-   Appelez [**CDrawImage :: SetSourceRect**](cdrawimage-setsourcerect.md) si le rectangle source change et [**CDrawImage :: SetTargetRect**](cdrawimage-settargetrect.md) si le rectangle cible change.
-   Gérez la palette pour les images en palette, comme décrit dans la section sur les palettes qui suivent.

## <a name="allocators"></a>Allocateurs

Le filtre indiqué dans le diagramme précédent utilise une classe Allocator personnalisée, [**CImageAllocator**](cimageallocator.md). Cet allocateur crée des DIB dans la mémoire partagée, à l’aide de la fonction GDI **CreateDIBSection** . Les exemples créés par l’allocateur sont des objets [**CImageSample**](cimagesample.md) .

Si le filtre est propriétaire de l’allocateur pour la connexion, les exemples de supports sont garantis comme des objets [**CImageSample**](cimagesample.md) . Dans ce cas, l’objet **CDrawImage** peut optimiser le dessin à l’aide de **BitBlt** ou de StretchBlt. Dans le cas contraire, il doit utiliser les fonctions **SetDIBitsToDevice** ou **StretchDIBits** plus lentes. L’option plus rapide est implémentée par la méthode [**CDrawImage :: FastRender**](cdrawimage-fastrender.md) , plus lente par la méthode [**CDrawImage :: SlowRender**](cdrawimage-slowrender.md) . (En dépit du nom, vous ne verrez probablement pas un gain de performances important dans **SlowRender**, en particulier sur du matériel plus récent.)

## <a name="palettes"></a>Palettes

Si la méthode [**FastRender**](cdrawimage-fastrender.md) est utilisée pour le dessin et que l’image est en palette, le filtre doit gérer la palette, comme suit :

-   La classe [**CImageSample**](cimagesample.md) contient un numéro de version de palette, stocké dans la structure [**DIBDATA**](dibdata.md) . La valeur est initialisée lorsque l’allocateur crée l’exemple.
-   La classe **CDrawImage** contient également un numéro de version de palette, qui est initialisé lors de la création.
-   Chaque fois que le type de média passe à un nouveau format en palette, appelez [**CDrawImage :: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md). Cette méthode incrémente le numéro de version de la palette de l’objet **CDrawImage** . Si le filtre utilise la classe [**CImagePalette**](cimagepalette.md) pour gérer les informations de palette, vous pouvez simplement appeler [**CImagePalette ::P reparepalette**](cimagepalette-preparepalette.md) chaque fois que le type de média change. La méthode **PreparePalette** incrémente la version de la palette uniquement lorsque cela est nécessaire.
-   La méthode [**FastRender**](cdrawimage-fastrender.md) compare la version de la palette **CDrawImage** à la version de palette de l’exemple. Si le numéro de version de l’exemple est en retard par rapport au numéro de version **CDrawImage** , la méthode **FastRender** appelle [**CDrawImage :: UpdateColourTable**](cdrawimage-updatecolourtable.md). La méthode **UpdateColourTable** définit la table des couleurs dans le contexte de périphérique, à l’aide de la fonction GDI **SetDIBColorTable** . En outre, la version de palette sur l’exemple est mise à jour avec le numéro de version actuel.
-   Si le code confidentiel se reconnecte, le filtre doit appeler [**CDrawImage :: ResetPaletteVersion**](cdrawimage-resetpaletteversion.md) pour réinitialiser la version de la palette. Lors de la reconnexion du pin, l’allocateur réalloue tous les exemples.



| Variables membres protégées                                            | Description                                                                                                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bStretch**](cdrawimage-m-bstretch.md)                          | Indique si l’image vidéo doit être étirée pour s’ajuster à la fenêtre de destination.                                              |
| [**m \_ bUsingImageAllocator**](cdrawimage-m-busingimageallocator.md)  | Indique si l’allocateur pour la connexion de code confidentiel est un objet **CImageAllocator** .                                         |
| [**m \_ EndSample**](cdrawimage-m-endsample.md)                        | Spécifie l’heure d’arrêt de l’exemple le plus récent.                                                                              |
| [**HDC de m \_**](cdrawimage-m-hdc.md)                                    | Handle vers le contexte de périphérique de la fenêtre propriétaire.                                                                              |
| [**m \_ MemoryDC**](cdrawimage-m-memorydc.md)                          | Handle vers le contexte de périphérique de mémoire de la fenêtre propriétaire.                                                                       |
| [**m \_ PaletteVersion**](cdrawimage-m-paletteversion.md)              | Utilisé pour effectuer le suivi de la modification de la palette.                                                                                         |
| [**m \_ pBaseWindow**](cdrawimage-m-pbasewindow.md)                    | Pointeur vers l’objet **CBaseWindow** propriétaire.                                                                                   |
| [**m \_ pMediaType**](cdrawimage-m-pmediatype.md)                      | Pointeur vers le type de média actuel.                                                                                              |
| [**m \_ SourceRect**](cdrawimage-m-sourcerect.md)                      | Spécifie le rectangle source pour le dessin.                                                                                     |
| [**m \_ StartSample**](cdrawimage-m-startsample.md)                    | Spécifie l’heure de début de l’exemple le plus récent.                                                                             |
| [**m \_ TargetRect**](cdrawimage-m-targetrect.md)                      | Spécifie le rectangle cible pour le dessin.                                                                                     |
| Méthodes protégées                                                     | Description                                                                                                                     |
| [**DisplaySampleTimes**](cdrawimage-displaysampletimes.md)           | Dessine les horodatages d’un échantillon de support en haut de l’image vidéo.                                                              |
| [**FastRender**](cdrawimage-fastrender.md)                           | Dessine l’image vidéo à l’aide des fonctions **BitBlt** ou **StretchBlt** .                                                         |
| [**SetStretchMode**](cdrawimage-setstretchmode.md)                   | Calcule si l’image vidéo doit être étirée.                                                                           |
| [**SlowRender**](cdrawimage-slowrender.md)                           | Dessine l’image vidéo à l’aide des fonctions **SetDIBitsToDevice** ou **StretchDIBits** .                                           |
| [**UpdateColourTable**](cdrawimage-updatecolourtable.md)             | Met à jour la table des couleurs avec une nouvelle palette.                                                                                     |
| M&#233;thodes publiques                                                        | Description                                                                                                                     |
| [**CDrawImage**](cdrawimage-cdrawimage.md)                           | Méthode de constructeur.                                                                                                             |
| [**DrawImage**](cdrawimage-drawimage.md)                             | Dessine une image vidéo dans la fenêtre vidéo.                                                                                        |
| [**DrawVideoImageHere**](cdrawimage-drawvideoimagehere.md)           | Dessine une image à partir d’un exemple de média dans un contexte de périphérique spécifié.                                                               |
| [**GetPaletteVersion**](cdrawimage-getpaletteversion.md)             | Récupère la version de la palette.                                                                                                  |
| [**GetSourceRect**](cdrawimage-getsourcerect.md)                     | Récupère le rectangle source actuel.                                                                                         |
| [**GetTargetRect**](cdrawimage-gettargetrect.md)                     | Récupère le rectangle de destination actuel.                                                                                    |
| [**IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) | Incrémente la version de la palette.                                                                                                 |
| [**NotifyAllocator**](cdrawimage-notifyallocator.md)                 | Informe l' `CDrawImage` objet si l’allocateur pour la connexion est un objet **CImageAllocator** .                       |
| [**NotifyEndDraw**](cdrawimage-notifyenddraw.md)                     | Non pris en charge.                                                                                                                  |
| [**NotifyMediaType**](cdrawimage-notifymediatype.md)                 | Avertit l’objet du type de média actuel.                                                                                  |
| [**NotifyStartDraw**](cdrawimage-notifystartdraw.md)                 | Non pris en charge.                                                                                                                  |
| [**ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)         | Réinitialise la version de la palette.                                                                                                     |
| [**ScaleSourceRect**](cdrawimage-scalesourcerect.md)                 | Met à l’échelle un rectangle source spécifié, s’il existe une différence entre la taille de la vidéo native et le format du type de média. Virtuels. |
| [**SetDrawContext**](cdrawimage-setdrawcontext.md)                   | Définit les contextes de périphérique utilisés pour le dessin.                                                                                      |
| [**SetSourceRect**](cdrawimage-setsourcerect.md)                     | Définit le rectangle source.                                                                                                      |
| [**SetTargetRect**](cdrawimage-settargetrect.md)                     | Définit le rectangle cible.                                                                                                      |
| [**UsingImageAllocator**](cdrawimage-usingimageallocator.md)         | Indique si l’allocateur actuel est un objet [**CImageAllocator**](cimageallocator.md) .                                 |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




