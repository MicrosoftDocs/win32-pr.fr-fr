---
title: Auteur, objet
description: Auteur, objet
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- Windows Media Format SDK, writer, objets
- ASF (Advanced Systems Format), objets Writer
- ASF (format des systèmes avancés), objets Writer
- objets, objets Writer
- objets Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f76ad82cb56317cef9b70b0412fb79662ef89eacace8668b08a06f4cc5bf420
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119392319"
---
# <a name="writer-object"></a>Auteur, objet

L’objet Writer est utilisé pour écrire des fichiers multimédias numériques à l’aide de la structure de fichiers ASF (Advanced Systems Format). Le processus d’écriture d’un fichier multimédia numérique implique de nombreuses étapes internes à l’enregistreur, qui coordonne la compression, la paquets de paquets et le multiplexage.

L’objet Writer comprend des interfaces pour la sortie vers des fichiers ou un réseau, prend en charge une interface de rappel et peut créer un ou plusieurs objets de propriétés de média d’entrée.

L’objet Writer est créé par la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), qui définit un pointeur vers une interface **IWMWriter** . Les autres interfaces de l’objet Writer peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par l’objet Writer.



| Interface                                          | Description                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | Fournit des méthodes pour générer des clés [*DRM*](wmformat-glossary.md) .                                                                                                |
| [**IWMDRMWriter2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | configure l’objet writer pour écrire un fichier contenant un flux pré-chiffré conforme au protocole Windows Media DRM 10 pour les périphériques réseau.                                                    |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | Gère la spécification et la récupération des informations d’en-tête, telles que les métadonnées, les [*marqueurs*](wmformat-glossary.md), etc.                                                           |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | Gère l’énumération à l’aide des informations de codec disponibles. Hérite de toutes les méthodes de **IWMHeaderInfo**.                                                                                            |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | Gère l’énumération à l’aide des informations de codec disponibles. Hérite de toutes les méthodes de **IWMHeaderInfo** et **IWMHeaderInfo2**.                                                                     |
| [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | Fournit un accès aux informations sur les systèmes de tatouage sur le système.                                                                                                                          |
| [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | Démarre et arrête l’écriture des fichiers ASF ; Il comprend des méthodes pour allouer des mémoires tampons, définir et récupérer des propriétés d’entrée, définir des profils et des noms de fichiers de sortie et déverrouiller le writer.         |
| [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | Ajoute, obtient et supprime les objets récepteurs spécifiés ; Récupère les statistiques, le nombre de récepteurs et l’heure à laquelle l’enregistreur travaille ; et exécute d’autres fonctions avancées.                                |
| [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | Fournit des fonctionnalités avancées, en particulier pour gérer la vidéo désentrelacée. Hérite de toutes les méthodes de **IWMWriterAdvanced**.                                                                 |
| [**IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | Fournit des fonctionnalités d’écriture supplémentaires, notamment la possibilité d’obtenir des statistiques d’enregistreur détaillées. Hérite de toutes les méthodes de **IWMWriterAdvanced** et **IWMWriterAdvanced2**.                       |
| [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | Gère certaines fonctionnalités d’écriture avancées relatives aux exemples postviewing. Postviewing affiche la sortie, généralement à partir d’un encodeur, pour vérifier que le processus d’encodage/décodage fonctionne correctement. |
| [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | Gère les passes de prétraitement effectuées par le writer. Les passes de prétraitement sont utilisées pour améliorer la qualité de la sortie encodée.                                                                                  |



 

L’interface de rappel suivante doit être implémentée par l’application pour suivre la progression de postviewing.



| Interface                                                      | Description                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | Gère le mode de réception des exemples non compressés de l’objet Writer pour afficher un aperçu de ce que fait le codec. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




