---
title: Métadonnées personnalisées
description: Métadonnées personnalisées
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- Windows Media Format SDK, métadonnées personnalisées
- ASF (Advanced Systems Format), métadonnées personnalisées
- ASF (format de systèmes avancés), métadonnées personnalisées
- Windows Media Format SDK, interface IWMHeaderInfo3
- ASF (Advanced Systems Format), interface IWMHeaderInfo3
- ASF (format des systèmes avancés), interface IWMHeaderInfo3
- métadonnées, personnalisation
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a795ab184e5bd6120278f61c0d3654679fd79c28
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724026"
---
# <a name="custom-metadata"></a>Métadonnées personnalisées

Outre les nombreux attributs pris en charge fournis avec le kit de développement logiciel (SDK) Windows Media format, vous pouvez créer des attributs de métadonnées pour vos propres spécifications. Lorsque vous créez des attributs de métadonnées personnalisés, vous devez utiliser une convention d’affectation de noms facilement identifiable pour éviter tout conflit possible avec les attributs créés par d’autres.

Il est recommandé d’utiliser les méthodes de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) pour créer vos métadonnées en raison de la flexibilité ajoutée qu’elles offrent sur les méthodes de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs**](attributes.md)
</dt> <dt>

[**Fonctionnalités de métadonnées**](metadata-features.md)
</dt> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




