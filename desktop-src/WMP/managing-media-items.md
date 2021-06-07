---
title: Gestion des éléments multimédias
description: Gestion des éléments multimédias
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Lecteur Windows Media, bibliothèque
- Modèle objet du lecteur Windows Media, bibliothèque
- modèle objet, bibliothèque
- Windows Media Player Mobile, bibliothèque pour le modèle objet
- Contrôle ActiveX du lecteur Windows Media, bibliothèque pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, bibliothèque pour le modèle objet
- Contrôle ActiveX, bibliothèque pour le modèle objet
- Bibliothèque du lecteur Windows Media, gestion des éléments multimédias
- bibliothèque, gestion des éléments multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf984c2f884ae828bd6426dd2a3f6da19a78ddea
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386888"
---
# <a name="managing-media-items"></a>Gestion des éléments multimédias

Un objet **multimédia** représente un élément multimédia. Il possède des propriétés et des méthodes que vous pouvez utiliser pour récupérer des informations et les afficher à l’utilisateur, ou pour effectuer des actions différentes en fonction de la valeur que vous récupérez.

La majeure partie de votre travail avec les objets **multimédias** implique des métadonnées sur le contenu de l’élément multimédia, appelé attributs. La rubrique [attributs d’élément multimédia](media-item-attributes.md) décrit comment lire et modifier des valeurs d’attribut. En plus de cette rubrique, consultez les [instructions relatives à l’utilisation des métadonnées Windows Media](/previous-versions/ms867702(v=msdn.10)) sur le site Web Microsoft pour plus d’informations sur les attributs et leur utilisation.

L’objet **Media** possède des propriétés et des méthodes qui récupèrent des attributs directement, tels que le nom ou la durée de l’élément. Pour les éléments vidéo, vous pouvez récupérer la hauteur et la largeur de l’image, et vous pouvez récupérer les informations de marqueur en fonction du nom ou de l’index d’un marqueur. Vous pouvez également déterminer si un élément multimédia particulier est inclus dans une sélection particulière.

## <a name="retrieving-a-media-object"></a>Récupération d’un objet multimédia

Vous pouvez accéder rapidement à l’élément multimédia actuel à l’aide du *lecteur*. propriété **currentMedia** .

Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



L’exemple C# suivant récupère un objet **multimédia** représentant l’élément actuel.


```C++
IWMPMedia media;
media = Player.currentMedia;

```



Vous pouvez créer un élément multimédia à partir d’un fichier multimédia numérique à l’aide du *lecteur*. méthode **newMedia** . Vous transmettez à la méthode le chemin d’accès de l’URL d’un fichier multimédia numérique et retourne une référence au nouvel objet **Media** . La méthode n’ajoute pas directement le nouvel objet à la bibliothèque. Toutefois, vous pouvez transmettre l’objet à la *sélection*. méthode **appendItem** ou *playlist*. méthode **InsertItem** .

L’exemple C# suivant crée un objet **multimédia** basé sur l’un des exemples de médias numériques installés avec le kit de développement logiciel (SDK) du lecteur Windows Media.


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> Vous devez inclure deux caractères de barre oblique inverse ( \\ ) (ou utiliser le caractère @ en C#) dans une chaîne pour représenter une barre oblique inverse réelle. Cela est dû au fait que C# utilise une barre oblique inverse unique pour définir une séquence d’échappement.

 

Vous pouvez créer un élément multimédia à partir d’un fichier multimédia numérique et l’ajouter à la bibliothèque en une seule étape à l’aide de *MediaCollection*. **Ajouter** une méthode. Comme le *lecteur*. méthode **newMedia** , la méthode **Add** prend le chemin d’accès à un fichier multimédia numérique.

L’exemple C# suivant crée un objet **multimédia** en fonction de l’un des exemples de fichiers du kit de développement logiciel (SDK) et ajoute cet objet à la bibliothèque.


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



Vous pouvez récupérer un objet **multimédia** représentant un élément multimédia dans une sélection à l’aide de la *sélection*. méthode **Item** . L’exemple C# suivant récupère le sixième élément multimédia de la sélection actuelle.


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Controls. currentItem**](controls-currentitem.md)
</dt> <dt>

[**Gestion des sélections**](managing-playlists.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**MediaCollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Utilisation de la bibliothèque**](working-with-the-library.md)
</dt> </dl>

 

 




