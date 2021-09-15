---
title: Flux arbitraire
description: Flux arbitraire
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows Media Format SDK, flux arbitraires
- ASF (Advanced Systems Format), flux arbitraires
- ASF (Advanced Systems Format), flux arbitraires
- Windows Media Format SDK, Streams
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- flux arbitraires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521105"
---
# <a name="arbitrary-streams"></a>Flux arbitraire

En plus des flux audio et vidéo et des flux d’images, un fichier ASF peut accueillir des flux contenant une variété de données. les objets du Windows Media Format SDK prennent en charge les flux de script, les flux de transfert de fichiers, les flux Web et les flux de données arbitraires. Tous ces types de flux sont arbitraires, ce qui signifie qu’aucune validation de données n’est effectuée par l’objet de lecture. Lorsque vous incluez des flux de ces types dans vos fichiers, assurez-vous que l’application de lecture effectue la validation ou la vérification des données pour vous assurer que votre contenu n’a pas été endommagé ou déformé intentionnellement par un tiers malveillant.

Bien que les objets de ce kit de développement logiciel ne vérifient pas ou ne valident pas les données dans des flux arbitraires, plusieurs types de flux arbitraires sont pris en charge en mode natif. Le tableau suivant répertorie les types de flux arbitraires prédéfinis. Les flux de script sont également pris en charge, mais sont décrits séparément dans la section [commandes de script](script-commands.md) . Pour plus d’informations sur la création de types personnalisés, consultez [données arbitraires personnalisées flux](custom-arbitrary-data-streams.md).



| Type arbitraire                   | Description                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [Flux de texte](text-streams.md) | Contiennent des chaînes de texte.                                             |
| [Flux de fichiers](file-streams.md) | Contiennent un ou plusieurs fichiers de données.                                   |
| [Flux Web](web-streams.md)   | Contiennent des fichiers de données équivalents à la version mise en cache des pages Web. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Flux audio et vidéo**](audio-and-video-streams.md)
</dt> <dt>

[**Configuration de types de flux arbitraires**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




