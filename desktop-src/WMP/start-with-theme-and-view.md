---
title: Démarrer avec un thème et une vue
description: Démarrer avec un thème et une vue
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- créer des apparences, élément THEMe
- Apparences du lecteur Windows Media, élément de thème
- apparences, élément THEMe
- fichiers de définition d’apparence, élément THEMe
- Élément THEMe
- créer des apparences, élément d’affichage
- Apparences du lecteur Windows Media, élément d’affichage
- Skins, élément VIEW
- fichiers de définition d’apparence, élément de vue
- Élément VIEW
- éléments, vue
- éléments, thème
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840710"
---
# <a name="start-with-theme-and-view"></a>Démarrer avec un thème et une vue

Chaque apparence doit avoir exactement un élément de **thème** et au moins un élément d' **affichage** .

À l’aide de votre éditeur de texte, créez le texte suivant :


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



Laissez des lignes vides avant la balise de **vue** de fermeture, car vous ajouterez plus de code ici ultérieurement.

Enregistrez votre fichier avec le nom de fichier de votre choix, mais assurez-vous que l’extension est. WMS. Par exemple, un nom de fichier classique peut être skinone. WMS.

Chaque apparence doit commencer par <THEME> et se terminer par </THEME>. Vous ne pouvez avoir qu’un seul élément **Theme** dans votre apparence, mais vous devez en avoir un.

Vous devez également avoir au moins un élément **View** . Vous pouvez avoir plus d’une **vue**, mais cet exemple n’en a qu’une. Vous devez avoir une ouverture <VIEW> et une fermeture <VIEW>. Notez que la </VIEW> balise d’ouverture ne ferme pas immédiatement la balise, mais qu’elle comprend plusieurs attributs avant le Chevron fermant (>). Les attributs suivants sont utilisés dans l’élément **Theme** dans cet exemple :

**clippingColor**

Vous n’aurez pas toujours besoin de l’attribut **clippingColor** si les bords de votre apparence sont rectangulaires. L’apparence de cet exemple est en forme ovale. vous avez donc besoin d’une couleur de découpage pour les parties de l’apparence sur lesquelles vous souhaitez afficher le Bureau ; essentiellement toutes les parties en dehors de l’ovale. Dans cet exemple d’apparence, nous utilisons un jaune foncé, spécifié comme « \# CCCC00 » dans le format Web. Les raisons de ce choix sont fournies lors de la [création du fichier art principal](creating-the-primary-art-file.md). Fondamentalement, cette valeur sera toujours un nombre que vous obtiendrez de votre programme art.

**backgroundImage**

Il s’agit du nom du fichier art principal. Il doit s’agir du nom de fichier et du chemin d’accès exacts de votre fichier art principal. Seuls les fichiers BMP, JPG, GIF et PNG sont pris en charge et BMP est recommandé.

**Spreadsheet**

Cette apparence n’a pas de **TitleBar**, donc la valeur sera « false ». Vous n’avez besoin que d’une barre de titre si vous souhaitez que votre apparence ait une couleur d’arrière-plan et qu’elle soit rectangulaire.

Veillez à placer le Chevron fermant (>) après la valeur **TitleBar** pour indiquer que vous avez terminé la définition de la **vue**. Laissez quelques lignes vides avant le **mode** de fermeture et les balises de **thème** . Vous aurez besoin des lignes pour le code que vous ajouterez ultérieurement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du fichier de définition d’apparence**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




