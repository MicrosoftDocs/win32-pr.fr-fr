---
title: Éditeur de métadonnées, objet
description: Éditeur de métadonnées, objet
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows Media Format SDK, objets de l’éditeur de métadonnées
- ASF (Advanced Systems Format), objets de l’éditeur de métadonnées
- ASF (format des systèmes avancés), objets de l’éditeur de métadonnées
- objets, objets de l’éditeur de métadonnées
- objets de l’éditeur de métadonnées, à propos de
- métadonnées, objets Editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724098"
---
# <a name="metadata-editor-object"></a>Éditeur de métadonnées, objet

L’objet de l’éditeur de métadonnées permet de modifier les informations stockées dans la section d’en-tête des fichiers ASF. Les éléments les plus courants manipulés par cet objet sont les attributs de métadonnées. En outre, l’éditeur de métadonnées traite des [*marqueurs*](wmformat-glossary.md) et des commandes de script. La seule fois où vous devez utiliser l’éditeur de métadonnées, c’est lorsque vous souhaitez modifier l’en-tête d’un fichier existant sans le visionner.

L’objet de l’éditeur de métadonnées est créé par la fonction [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), qui définit un pointeur vers une interface **IWMMetadataEditor** . Les autres interfaces de l’objet de l’éditeur de métadonnées peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par l’objet de l’éditeur de métadonnées.



| Interface                                        | Description                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | Permet aux applications de modifier d’examiner les propriétés [*DRM*](wmformat-glossary.md) d’un fichier ASF sans disposer de droits pour lire le contenu protégé. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | Manipule les attributs, les marqueurs et les commandes de script dans l’en-tête.                                                                                                                                    |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | Récupère des informations de codec. Hérite de toutes les méthodes de **IWMHeaderInfo**.                                                                                                                         |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | Offre une prise en charge avancée des attributs, y compris des attributs volumineux, des langages multiples et des noms d’attributs en double. Hérite de toutes les méthodes de **IWMHeaderInfo** et **IWMHeaderInfo2**.      |
| [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | Ouvre, ferme et enregistre les modifications apportées à l’en-tête d’un fichier ASF.                                                                                                                                         |
| [**IWMMetadataEditor2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | Ouvre un fichier ASF pour la modification d’en-tête avec plusieurs options d’accès aux fichiers et de partage. Hérite de toutes les méthodes de **IWMMetadataEditor**.                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Marqueurs**](markers.md)
</dt> <dt>

[**Metadata**](metadata.md)
</dt> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Commandes de script**](script-commands.md)
</dt> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




