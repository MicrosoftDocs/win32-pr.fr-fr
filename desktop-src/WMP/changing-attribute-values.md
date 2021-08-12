---
title: Modification des valeurs d’attribut
description: Modification des valeurs d’attribut
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Lecteur Windows Media, attributs pour les éléments multimédias
- Lecteur Windows Media modèle objet, attributs pour les éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Lecteur Windows Media Mobile, attributs pour les éléments multimédias
- Lecteur Windows Media ActiveX contrôle, attributs pour les éléments multimédias
- Lecteur Windows Media contrôle de ActiveX Mobile, attributs pour les éléments multimédias
- contrôle ActiveX, attributs pour les éléments multimédias
- bibliothèque de Lecteur Windows Media, attributs des éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, modification des valeurs
- modification des valeurs d’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870d8bfa13012bd79fdd672f1543db4a484ca5d9674ef1a9e48e832119ea1b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581115"
---
# <a name="changing-attribute-values"></a>Modification des valeurs d’attribut

Vous pouvez modifier la valeur d’un attribut si votre page Web ou application dispose d’un accès en lecture/écriture à la bibliothèque et que l’attribut peut être à la fois lu et écrit.

Vous pouvez modifier un attribut de l’élément multimédia actuel. Pour modifier les attributs de plusieurs éléments multimédias, vous pouvez les affecter à leur tour au *lecteur*. propriété **currentMedia** .

Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Pour modifier un attribut, appelez le *lecteur*. *currentMedia*. méthode **setItemInfo** comme indiqué dans l’exemple C# suivant.


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



Nous vous recommandons d’appeler le *support*. méthode **isReadOnlyItem** pour déterminer si vous pouvez modifier un attribut particulier.

> [!Note]  
> si vous incorporez le contrôle dans votre application, les attributs de fichier que vous modifiez ne seront pas écrits dans le fichier multimédia numérique tant que l’utilisateur n’aura pas Lecteur Windows Media. Si vous utilisez le contrôle dans une application distante écrite en C++, les attributs de fichier que vous modifiez seront écrits dans le fichier multimédia numérique peu après que vous avez apporté les modifications. Dans les deux cas, les modifications sont immédiatement disponibles dans la bibliothèque.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs d’élément multimédia**](media-item-attributes.md)
</dt> <dt>

[**Accès à la bibliothèque**](library-access.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Lecture des valeurs d’attribut**](reading-attribute-values.md)
</dt> </dl>

 

 




