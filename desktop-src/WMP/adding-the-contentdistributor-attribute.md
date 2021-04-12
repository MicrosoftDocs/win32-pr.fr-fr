---
title: Ajout de l’attribut ContentDistributor
description: Ajout de l’attribut ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player Online stores, ajout de l’attribut ContentDistributor
- magasins en ligne, ajouter un attribut ContentDistributor
- types 1 magasins en ligne, ajout de l’attribut ContentDistributor
- type 2 magasins en ligne, ajout de l’attribut ContentDistributor
- Windows Media Player Online stores, attribut ContentDistributor
- magasins en ligne, attribut ContentDistributor
- types 1 magasins en ligne, attribut ContentDistributor
- types 2 magasins en ligne, attribut ContentDistributor
- ajout de l’attribut ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310090"
---
# <a name="adding-the-contentdistributor-attribute"></a>Ajout de l’attribut ContentDistributor

Quand l’utilisateur tente de lire le contenu de la boutique en ligne ou de copier le contenu sur un CD ou un périphérique, le lecteur Windows Media appelle certaines méthodes dans votre objet COM. Pour ce faire, le joueur a besoin d’un moyen de différencier votre contenu de celui d’autres fournisseurs de magasins en ligne. En ajoutant le nom de votre clé de magasin en ligne comme valeur de **ContentDistributor** (qui est un alias de l’attribut **WM/ContentDistributor**) du kit de développement logiciel (SDK) du format Windows Media à votre contenu Windows Media, vous vous assurez que le lecteur peut identifier le contenu associé à votre service.

L’ajout d’une valeur pour **ContentDistributor** garantit également que le lecteur Windows Media va créer un nœud dans la bibliothèque pour le contenu que vous fournissez. Consultez [intégration](library-integration.md)de la bibliothèque.

Vous pouvez spécifier cette valeur de deux manières :

-   Utilisez le modèle objet du lecteur Windows Media. Dans ce cas, le lecteur Windows Media ajoute la valeur que vous spécifiez à la base de données de bibliothèque. Finalement, le lecteur écrira également la valeur de l’attribut dans le fichier multimédia numérique.
-   Utilisez le kit de développement logiciel (SDK) de format Windows Media pour ajouter par programmation l’attribut **WM/ContentDistributor** . Dans ce cas, le lecteur Windows Media lit la valeur de l’attribut et l’ajoute à la base de données lorsque le fichier multimédia numérique est ajouté à la bibliothèque.

Lorsque vous créez votre objet COM de magasin en ligne, la valeur d’attribut de fichier que vous définissez pour **ContentDistributor** et la valeur assignée à la constante KszContentDistributorID dans YourProject. h doivent correspondre exactement. Rappelez-vous que vous avez spécifié cette valeur constante pour votre objet COM lorsque vous avez créé le projet à l’aide de l’Assistant projet. Vous pouvez modifier cette valeur manuellement. Veillez simplement à utiliser une chaîne qui identifie de façon unique votre service.

## <a name="using-the-windows-media-player-object-model"></a>Utilisation du modèle objet du lecteur Windows Media

Pour spécifier une valeur pour **ContentDistributor** à l’aide du modèle objet du lecteur Windows Media, utilisez la méthode [Media. setItemInfo](media-setiteminfo.md) . L’exemple de code suivant spécifie la valeur « Proseware » pour **ContentDistributor** pour l’élément multimédia en cours de diffusion :


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



## <a name="using-the-windows-media-format-sdk"></a>Utilisation du kit de développement logiciel (SDK) Windows Media format

Le kit de développement logiciel (SDK) du lecteur Windows Media comprend un exemple de fichier C++, nommé SetContentDistributor. cpp, qui montre comment utiliser le kit de développement logiciel (SDK) Windows Media Format 9 pour ajouter l’attribut **WM/ContentDistributor** . Vous pouvez trouver cet exemple de fichier dans le dossier nommé Metadata où vous avez installé le kit de développement logiciel (SDK). Pour utiliser ce code, vous devez effectuer les étapes suivantes :

1.  Installez le kit de développement logiciel (SDK) Windows Media Format 9 Series et configurez le runtime comme décrit dans la documentation.
2.  Créez un projet C++ vide dans Visual Studio et ajoutez l’exemple de fichier nommé SetContentDistributor. cpp au projet.
3.  Ajoutez le chemin d’accès aux dossiers lib du kit de développement logiciel (SDK) Windows Media Format 9 Series dans votre liste de chemins d’accès aux fichiers. Dans le menu **Outils** , choisissez **Options**.
4.  Dans la boîte de dialogue **options** , cliquez sur **projets**, puis sur **Répertoires VC + +**.
5.  Dans la zone de liste déroulante **afficher les répertoires pour** , cliquez sur **fichiers de bibliothèque**.
6.  Utilisez les boutons pour ajouter les chemins d’accès aux zones de liste.
7.  Ouvrez la boîte de dialogue pages de propriétés de votre projet. Choisissez **Propriétés de configuration**, puis **éditeur de liens**, puis **entrée**. Tapez « wmvcore. lib » dans la zone de texte **dépendances supplémentaires** .

L’exemple de code crée un programme de ligne de commande. Les arguments que vous fournissez lors de l’exécution du programme spécifient le chemin d’accès au fichier multimédia numérique à modifier et une chaîne pour la valeur de l’attribut **ContentDistributor** . Le code utilise **IWMHeaderInfo :: setAttribute** pour ajouter l’attribut au fichier que vous avez spécifié. Vous pouvez utiliser cet exemple tel quel ou l’utiliser comme point de départ pour votre propre programme.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




