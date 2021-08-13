---
title: Ajout de l’attribut ContentDistributor
description: Ajout de l’attribut ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Lecteur Windows Media les magasins en ligne, ajout de l’attribut ContentDistributor
- magasins en ligne, ajouter un attribut ContentDistributor
- types 1 magasins en ligne, ajout de l’attribut ContentDistributor
- type 2 magasins en ligne, ajout de l’attribut ContentDistributor
- Lecteur Windows Media les magasins en ligne, attribut ContentDistributor
- magasins en ligne, attribut ContentDistributor
- types 1 magasins en ligne, attribut ContentDistributor
- types 2 magasins en ligne, attribut ContentDistributor
- ajout de l’attribut ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66871f73c03e73c08b5ae7e72518a48817192def22c8dfce4caf2ce12d36fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391789"
---
# <a name="adding-the-contentdistributor-attribute"></a>Ajout de l’attribut ContentDistributor

quand l’utilisateur tente de lire le contenu de la boutique en ligne ou de copier le contenu sur un CD ou un périphérique, Lecteur Windows Media appelle certaines méthodes dans votre objet COM. Pour ce faire, le joueur a besoin d’un moyen de différencier votre contenu de celui d’autres fournisseurs de magasins en ligne. en ajoutant le nom de votre clé de magasin en ligne comme valeur pour **ContentDistributor** (qui est un alias pour l’attribut Windows media Format SDK nommé **WM/ContentDistributor**) à votre contenu multimédia Windows, vous vous assurez que le lecteur peut identifier le contenu associé à votre service.

l’ajout d’une valeur pour **ContentDistributor** permet également de s’assurer que Lecteur Windows Media créera un nœud dans la bibliothèque pour le contenu que vous fournissez. Consultez [intégration](library-integration.md)de la bibliothèque.

Vous pouvez spécifier cette valeur de deux manières :

-   utilisez le modèle objet Lecteur Windows Media. dans ce cas, Lecteur Windows Media ajoute la valeur que vous spécifiez à la base de données de bibliothèque. Finalement, le lecteur écrira également la valeur de l’attribut dans le fichier multimédia numérique.
-   utilisez le kit de développement logiciel (SDK) de Format multimédia Windows pour ajouter par programmation l’attribut **WM/ContentDistributor** . dans ce cas, Lecteur Windows Media lit la valeur de l’attribut et l’ajoute à la base de données lorsque le fichier multimédia numérique est ajouté à la bibliothèque.

Lorsque vous créez votre objet COM de magasin en ligne, la valeur d’attribut de fichier que vous définissez pour **ContentDistributor** et la valeur assignée à la constante KszContentDistributorID dans YourProject. h doivent correspondre exactement. Rappelez-vous que vous avez spécifié cette valeur constante pour votre objet COM lorsque vous avez créé le projet à l’aide de l’Assistant projet. Vous pouvez modifier cette valeur manuellement. Veillez simplement à utiliser une chaîne qui identifie de façon unique votre service.

## <a name="using-the-windows-media-player-object-model"></a>utilisation du modèle objet Lecteur Windows Media

pour spécifier une valeur pour **ContentDistributor** à l’aide du modèle objet Lecteur Windows Media, utilisez la méthode [Media. setItemInfo](media-setiteminfo.md) . L’exemple de code suivant spécifie la valeur « Proseware » pour **ContentDistributor** pour l’élément multimédia en cours de diffusion :


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a>utilisation du kit de développement logiciel (SDK) Windows Media Format

le kit de développement logiciel (sdk) Lecteur Windows Media comprend un exemple de fichier C++, nommé SetContentDistributor. cpp, qui montre comment utiliser le kit de développement logiciel (sdk) de série Windows Media Format 9 pour ajouter l’attribut **WM/ContentDistributor** . Vous pouvez trouver cet exemple de fichier dans le dossier nommé Metadata où vous avez installé le kit de développement logiciel (SDK). Pour utiliser ce code, vous devez effectuer les étapes suivantes :

1.  installez le kit de développement logiciel (SDK) de la série Media Format 9 Windows et configurez le runtime comme décrit dans la documentation.
2.  créez un projet C++ vide dans Visual Studio et ajoutez l’exemple de fichier nommé SetContentDistributor. cpp au projet.
3.  ajoutez le chemin d’accès aux dossiers Lib du kit de développement logiciel (SDK) de la série 9 Windows Media dans votre liste de chemins d’accès aux fichiers. Dans le menu **Outils** , choisissez **Options**.
4.  dans la boîte de dialogue **Options** , cliquez sur **projets**, puis sur **VC++ répertoires**.
5.  Dans la zone de liste déroulante **afficher les répertoires pour** , cliquez sur **fichiers de bibliothèque**.
6.  Utilisez les boutons pour ajouter les chemins d’accès aux zones de liste.
7.  Ouvrez la boîte de dialogue pages de propriétés de votre projet. Choisissez **Propriétés de configuration**, puis **éditeur de liens**, puis **entrée**. Tapez « wmvcore. lib » dans la zone de texte **dépendances supplémentaires** .

L’exemple de code crée un programme de ligne de commande. Les arguments que vous fournissez lors de l’exécution du programme spécifient le chemin d’accès au fichier multimédia numérique à modifier et une chaîne pour la valeur de l’attribut **ContentDistributor** . Le code utilise **IWMHeaderInfo :: setAttribute** pour ajouter l’attribut au fichier que vous avez spécifié. Vous pouvez utiliser cet exemple tel quel ou l’utiliser comme point de départ pour votre propre programme.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




