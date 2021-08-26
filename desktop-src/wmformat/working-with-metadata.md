---
title: Utilisation des métadonnées
description: Utilisation des métadonnées
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows Media Format SDK, vue d’ensemble des métadonnées
- ASF (Advanced Systems Format), vue d’ensemble des métadonnées
- ASF (format des systèmes avancés), vue d’ensemble des métadonnées
- métadonnées, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c001eed5330d3d90cdbf42cc52cfef3f048a25f7d8f72fe4402a48ccbb42480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109879"
---
# <a name="working-with-metadata"></a>Utilisation des métadonnées

La prise en charge des métadonnées est fournie par l’objet Writer, le lecteur et les objets lecteur synchrones, ainsi que l’objet éditeur de métadonnées. Pour obtenir des informations générales sur les métadonnées, consultez [métadonnées](metadata.md). pour plus d’informations sur les fonctionnalités de prise en charge des métadonnées dans Windows le kit de développement logiciel (SDK) Media Format, consultez [fonctionnalités de métadonnées](metadata-features.md)

L’interface pour la modification des métadonnées est [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), que vous pouvez obtenir en appelant la méthode **QueryInterface** de n’importe quelle interface dans l’un des objets mentionnés ci-dessus. **IWMHeaderInfo3** hérite des méthodes de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) et [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2). Les méthodes de **IWMHeaderInfo3** qui traitent des attributs de métadonnées représentent une approche différente de l’accès aux métadonnées que celle utilisée par les méthodes de **IWMHeaderInfo**. Vous devez toujours utiliser les méthodes plus récentes.

Les métadonnées d’un fichier ASF sont identifiées par un index et un numéro de flux. Un numéro de flux 0 est assigné aux attributs au niveau du fichier. dans les versions précédentes du kit de développement logiciel (SDK) Windows Media Format, les attributs pouvaient être identifiés par leur nom. Toutefois, étant donné que vous pouvez désormais dupliquer des noms d’attribut dans un flux, ce n’est plus possible. Au lieu de cela, vous pouvez récupérer tous les index correspondant à un nom. Pour plus d’informations, consultez [récupération des attributs de métadonnées](retrieving-metadata-attributes.md).

Pour faciliter la recherche d’attributs rapidement, vous pouvez utiliser un numéro de flux spécial, 0xFFFF. Utilisez ce numéro de flux pour identifier l’ensemble du fichier, plutôt qu’un flux spécifique ou les attributs au niveau du fichier. les objets du kit de développement logiciel (SDK) de Format multimédia Windows gèrent des index distincts pour chaque flux et pour les attributs de niveau fichier. Lorsque vous utilisez Stream 0xFFFF, les index sont différents de ceux que vous utilisez lors de la spécification d’un flux spécifique. Par exemple, l’attribut qui est l’index 0 pour le flux 0 ne sera pas le même que l’attribut index 0 pour Stream 0xFFFF.

Les sections suivantes décrivent l’utilisation des métadonnées plus en détail.



| Section                                                                    | Description                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Récupération des attributs de métadonnées](retrieving-metadata-attributes.md)       | Décrit comment lire les attributs de métadonnées d’un en-tête de fichier.                     |
| [Définition des attributs de métadonnées](setting-metadata-attributes.md)             | Décrit comment ajouter de nouveaux attributs de métadonnées à un en-tête de fichier.                    |
| [Modification des attributs de métadonnées](editing-metadata-attributes.md)             | Décrit comment modifier des attributs de métadonnées existants.                               |
| [Supprimer des attributs de métadonnées](removing-metadata-attributes.md)           | Décrit comment supprimer des attributs de métadonnées existants.                             |
| [Utilisation d’attributs de métadonnées complexes](using-complex-metadata-attributes.md) | Décrit comment utiliser des attributs dont les valeurs sont représentées par des structures. |



 

Plusieurs des exemples d’applications montrent comment récupérer et modifier des métadonnées. En particulier, consultez l’exemple MetadataEdit, qui se trouve à la fois dans les versions C++ et C#.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs**](attributes.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> <dt>

[**Exemples d’applications**](sample-applications.md)
</dt> </dl>

 

 




