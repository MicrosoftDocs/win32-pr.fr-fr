---
title: Attributs (kit de développement logiciel (SDK) Windows Media format 11)
description: Attributs
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK, attributs
- ASF (Advanced Systems Format), attributs
- ASF (format des systèmes avancés), attributs
- attributs, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c209558ed4803fee96e9b482302af1864cbf988b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383687"
---
# <a name="attributes-windows-media-format-11-sdk"></a>Attributs (kit de développement logiciel (SDK) Windows Media format 11)

Un attribut est un élément individuel de métadonnées. La plupart des attributs peuvent être définis par votre application et sont écrits dans l’en-tête d’un fichier ASF.

Certains des attributs prédéfinis sont des attributs codés. Ces attributs ne sont pas stockés dans l’en-tête d’un fichier ASF, mais sont calculés par les objets du kit de développement logiciel (SDK) du format Windows Media lorsque le fichier est chargé. Étant donné que les attributs codés sont toujours calculés, ils sont en lecture seule par nature.

Ce kit de développement logiciel (SDK) comprend de nombreuses définitions d’attributs que vous pouvez utiliser. Vous pouvez également créer vos propres attributs pour décrire le contenu.

Les sections suivantes décrivent les attributs prédéfinis.



| Section                                                                | Description                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Liste d’attributs](attribute-list.md)                                   | Fournit une liste alphabétique de tous les attributs prédéfinis. Après la liste, chaque attribut est décrit individuellement.                                                                          |
| [Attributs avec plusieurs valeurs](attributes-with-multiple-values.md) | Répertorie les attributs qui peuvent être ajoutés plusieurs fois à un fichier.                                                                                                                                      |
| [Attributs par type](attributes-by-type.md)                           | Contient des listes d’attributs triés par type. Il s’agit notamment des listes d’attributs à usage spécifique (comme ceux qui traitent de la gestion des droits numériques) et des listes d’attributs suggérés par type de contenu. |
| [Prise en charge des balises ID3](id3-tag-support.md)                                 | Répertorie les attributs qui sont compatibles avec les balises ID3.                                                                                                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMHeaderInfo::GetAttributeByIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[**IWMHeaderInfo :: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




