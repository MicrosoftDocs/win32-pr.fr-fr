---
description: Séparateur ASF
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: Séparateur ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111887"
---
# <a name="asf-splitter"></a>Séparateur ASF

L’objet *séparateur* ASF est un composant de couche WMContainer qui analyse l’objet de données ASF d’un fichier ASF (Advanced Systems Format). Vous pouvez utiliser le séparateur pour lire les paquets de données dans l’objet de données et générer des exemples de flux. Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).

Le séparateur expose l’interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) . Le séparateur analyse les paquets de données ASF pour les flux sélectionnés et les reconditionne dans des exemples d’objets individuels qui exposent l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) . Le séparateur est l’un des composants de niveau plateforme de Media Foundation. La source de média ASF utilise le séparateur en interne pour analyser les fichiers ASF.

Le diagramme suivant illustre la génération d’exemples pour un fichier ASF par le biais du séparateur.

![Diagramme montrant l’exemple de génération d’un fichier ASF](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

Cette section contient les rubriques suivantes :



| Rubrique                                                                                                                        | Description                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Création de l’objet Splitter ASF](creating-the-asf-splitter-object.md)                                                     | Comment créer et initialiser le séparateur.                              |
| [Configuration de l’objet Splitter ASF](configuring-the-asf-splitter-object.md)                                               | Paramètres de configuration pour le séparateur.                                |
| [Génération d’exemples de flux à partir d’un objet de données ASF existant](generating-stream-samples-from-an-existing-asf-data-object.md) | Comment analyser l’objet de données ASF et générer des échantillons de vapeur Packet. |



 

Le tableau suivant présente les attributs d’objet de données pertinents.



| Attribut                                                                                                    | Description                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**\_paquets MF PD \_ ASF FM \_ \_**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Nombre de paquets de données dans l’objet de données ASF.                                                       |
| [**\_taille de \_ paquet min PD ASF \_ FichierPropriétés \_ Min \_ \_ .**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Taille minimale des paquets de données dans le fichier, en octets.                                              |
| [**\_ \_ \_ \_ taille maximale des \_ paquets \_ MF PD ASF FichierPropriétés**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Taille maximale des paquets de données dans le fichier, en octets                                               |
| [**\_longueur des \_ \_ données ASF \_ pour MF**](mf-pd-asf-data-length-attribute.md)                                         | Taille de l’objet de données ASF, en octets.                                                               |
| [**\_décalage de \_ \_ début de données ASF \_ \_ pour MF PD**](mf-pd-asf-data-start-offset-attribute.md)                            | Décalage, en octets, du premier paquet de données de l’objet de données ASF par rapport au début du fichier. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants WMContainer ASF](wmcontainer-asf-components.md)
</dt> <dt>

[Didacticiel : lecture d’un fichier ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



