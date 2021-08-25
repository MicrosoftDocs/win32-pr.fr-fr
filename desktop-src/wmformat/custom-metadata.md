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
ms.openlocfilehash: cdbbc9fdfc07500e43a3a3875bbb62a77ed176df7a1607a6cb902cef24160e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809449"
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

 

 




