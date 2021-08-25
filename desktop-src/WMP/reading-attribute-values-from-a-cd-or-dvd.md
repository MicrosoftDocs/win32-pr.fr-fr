---
title: Lecture des valeurs d’attribut à partir d’un CD ou d’un DVD
description: Lecture des valeurs d’attribut à partir d’un CD ou d’un DVD
ms.assetid: 441916fb-f66d-4a12-a95c-b47561c93e64
keywords:
- Lecteur Windows Media, attributs pour les éléments multimédias
- Lecteur Windows Media modèle objet, attributs pour les éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Lecteur Windows Media Mobile, attributs pour les éléments multimédias
- Lecteur Windows Media ActiveX contrôle, attributs pour les éléments multimédias
- Lecteur Windows Media contrôle de ActiveX Mobile, attributs pour les éléments multimédias
- contrôle ActiveX, attributs pour les éléments multimédias
- bibliothèque de Lecteur Windows Media, attributs des éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, lire des valeurs
- lecture des valeurs d’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fda1bf3002f015873b69e29503ecba637a978bac1b167724c04f5f15228b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861769"
---
# <a name="reading-attribute-values-from-a-cd-or-dvd"></a>Lecture des valeurs d’attribut à partir d’un CD ou d’un DVD

Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



L’exemple de code C# suivant récupère les valeurs de tous les attributs du disque actif qui se trouvent dans le lecteur et les écrit dans un fichier.


```C++
private void logDiscAttributes()
{
    int iCDCount = 0; // Count of CD and DVD drives
    int iAttrCount = 0; // Attribute count.
    int iPLCount = 0; // Playlist item count.

    IWMPCdromCollection cdCollection;
    IWMPPlaylist playlist;
    IWMPMedia media;
    string strAttribName = "";
    string strAttribValue = "";
    string strText = "";

    // Create a StreamWriter object to write
    // the output to a file.
    StreamWriter sw = new StreamWriter(strOutFile, true);

    cdCollection = Player.cdromCollection;
    iCDCount = cdCollection.count;

    // Loop through the CD and DVD drives.
    for (int i = 0; i < iCDCount; i++)
    {
        playlist = cdCollection.Item(i).Playlist;

        // Loop through the playlist attributes.
        iAttrCount = playlist.attributeCount;
        for (int j = 0; j < iAttrCount; j++)
        {
            strText += "Playlist Attribute: \t";
            strAttribName = playlist.get_attributeName(j);
            strText += "\t" + strAttribName + "\t";
            strAttribValue = playlist.getItemInfo(strAttribName);
            strText += strAttribValue + "\n";
        }

        // Loop through the playlist.
        iPLCount = playlist.count;
        for (int k = 0; k < iPLCount; k++)
        {
            media = playlist.get_Item(k);

            // Loop through the media attributes.
            iAttrCount = media.attributeCount;
            for (int m = 0; m < iAttrCount; m++)
            {
                strText += "Track or Chapter [" + m.ToString() + "]";
                strAttribName = media.getAttributeName(m);
                strText += "\t" + strAttribName + "\t";
                strText += "Read Only: " + media.isReadOnlyItem(strAttribName) + "\t";
                strAttribValue = media.getItemInfo(strAttribName);
                strText += strAttribValue + "\n";
            }
        }
    }

    sw.Write(strText);
    sw.Close();

    MessageBox.Show(strOutFile + " created");
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs d’élément multimédia**](media-item-attributes.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> </dl>

 

 




