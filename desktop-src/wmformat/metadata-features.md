---
title: Fonctionnalités de métadonnées
description: Les métadonnées sont utilisées dans les fichiers ASF pour décrire le contenu et les propriétés d’un fichier.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Media Format SDK, fonctionnalités de métadonnées
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités
- ASF (Advanced Systems Format), fonctionnalités de métadonnées
- ASF (format de systèmes avancés), fonctionnalités de métadonnées
- ASF (Advanced Systems Format), fonctionnalités
- ASF (format des systèmes avancés), fonctionnalités
- métadonnées, fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104381693"
---
# <a name="metadata-features"></a>Fonctionnalités de métadonnées

Les métadonnées sont utilisées dans les fichiers ASF pour décrire le contenu et les propriétés d’un fichier. Tous les fichiers ASF que vous créez doivent inclure les métadonnées appropriées. (Pour une vue d’ensemble, consultez [Metadata](metadata.md).) Le kit de développement logiciel (SDK) Windows Media format prend en charge la modification des métadonnées via l’objet Writer, l’objet éditeur de métadonnées et les objets lecteur et lecteur synchrone. La prise en charge native d’un large éventail d’attributs de métadonnées est incluse. Pour obtenir la liste des attributs prédéfinis, consultez [attributs](attributes.md) .

La prise en charge des métadonnées fournie par les différents objets du kit de développement logiciel (SDK) du format Windows Media est flexible et puissante. Les principales fonctionnalités de métadonnées sont résumées dans la liste suivante :

-   Taille d’attribut flexible. La taille des attributs de métadonnées n’est pas limitée.
-   Attributs au niveau du flux. Les métadonnées des fichiers ASF peuvent être assignées au fichier dans son ensemble ou à un flux de données particulier.
-   Attributs dupliqués. Un attribut nommé peut être utilisé plusieurs fois dans le même fichier. Cette fonctionnalité est particulièrement utilisée lors de l’affectation d’attributs descriptifs de contenu. Par exemple, une chanson peut avoir plusieurs auteurs, chacun requérant un attribut **Author** distinct dans le fichier.
-   Plusieurs langues. Chaque attribut est associé à une langue. Vous pouvez définir les langues prises en charge, puis en affecter une à chaque attribut que vous écrivez. Étant donné que vous pouvez dupliquer des attributs, vous pouvez fournir les attributs les plus importants dans plusieurs langues pour atteindre un public plus large. Si vous ne spécifiez pas de langue, la langue par défaut (obtenue à partir du système d’exploitation de l’ordinateur exécutant votre application) sera utilisée.
-   Attributs complexes. Certains des attributs prédéfinis prennent en charge les données structurées. Pour ces attributs, le type de données est Binary, mais la valeur est une structure définie dans ce kit de développement logiciel (SDK).

Les rubriques suivantes abordent les autres fonctionnalités de métadonnées prises en charge.



| Rubrique                                  | Description                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [Prise en charge d’ID3](id3.md)                 | Décrit la prise en charge des frames ID3 à l’aide des objets du kit de développement logiciel (SDK) Windows Media format. |
| [Métadonnées personnalisées](custom-metadata.md) | Décrit les implications de l’utilisation de métadonnées personnalisées.                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités**](features.md)
</dt> <dt>

[**Interface IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**Interface IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[**Interface IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[**Métadonnées**](metadata.md)
</dt> </dl>

 

 




