---
title: Lecture des valeurs d’attribut
description: Lecture des valeurs d’attribut
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Lecteur Windows Media, attributs des éléments multimédias
- Modèle objet du lecteur Windows Media, attributs des éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Windows Media Player Mobile, attributs pour les éléments multimédias
- Contrôle ActiveX du lecteur Windows Media, attributs des éléments multimédias
- Contrôle ActiveX Windows Media Player Mobile, attributs des éléments multimédias
- Contrôle ActiveX, attributs pour les éléments multimédias
- Bibliothèque du lecteur Windows Media, attributs pour les éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, lire des valeurs
- lecture des valeurs d’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512270"
---
# <a name="reading-attribute-values"></a>Lecture des valeurs d’attribut

Les attributs que vous pouvez trouver dans la bibliothèque et dans les fichiers Windows Media ont des noms prédéfinis. Vous pouvez écrire du code qui récupère la valeur d’un attribut en passant le nom de cet attribut au *média*. **getItemInfo** ou *Media*. **getItemInfoByType**. Vous pouvez également écrire du code qui récupère les valeurs de tous les attributs d’un fichier ou d’un élément.

L’exemple C# suivant récupère la valeur de l’attribut **title** et l’affiche dans une boîte de message. Dans cet exemple, l’objet **Player** a été défini en tant que AxWMPLib. AxWindowsMediaPlayer Player.


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



Dans l’appel à **getItemInfoByType**, le deuxième paramètre est une chaîne qui spécifie la langue. Si vous transmettez une chaîne vide comme indiqué dans cet exemple, la méthode récupère la valeur dans la langue par défaut. Pour plus d’informations sur le troisième paramètre, consultez [attributs avec plusieurs valeurs](attributes-with-multiple-values.md).

L’exemple C# suivant récupère les valeurs d’un attribut donné dans l’élément multimédia actuel. Elle retourne ces valeurs sous la forme d’une chaîne délimitée par des points-virgules. Notez que pour les attributs représentés sous forme d’objets, tels que **WM/paroles \_ synchronisés**, **WM/Picture** et **WM/UserWebURL**, la fonction retourne une chaîne vide.


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



Le troisième argument passé à la méthode **getItemInfoByType** est l’index d’un attribut particulier dans un ensemble d’attributs portant le même nom.

Vous pouvez utiliser du code similaire pour récupérer des attributs qui ont des noms uniques. Dans ce cas, **getAttributeCountByType** retourne 1. Dans l’exemple ci-dessus, l’appel à **getItemInfoByType** ne s’exécute qu’une seule fois.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modification des valeurs d’attribut**](changing-attribute-values.md)
</dt> <dt>

[**Attributs d’élément multimédia**](media-item-attributes.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Lecture des valeurs d’attribut à partir d’un CD ou d’un DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




