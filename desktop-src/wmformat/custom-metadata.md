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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226017"
---
# <a name="custom-metadata"></a>Métadonnées personnalisées

outre les nombreux attributs pris en charge fournis avec le kit de développement logiciel (SDK) Windows Media Format, vous pouvez créer des attributs de métadonnées avec vos propres spécifications. Lorsque vous créez des attributs de métadonnées personnalisés, vous devez utiliser une convention d’affectation de noms facilement identifiable pour éviter tout conflit possible avec les attributs créés par d’autres.

Il est recommandé d’utiliser les méthodes de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) pour créer vos métadonnées en raison de la flexibilité ajoutée qu’elles offrent sur les méthodes de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs**](attributes.md)
</dt> <dt>

[**Fonctionnalités de métadonnées**](metadata-features.md)
</dt> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




