---
title: à propos de l’objet Paramètres
description: à propos de l’objet Paramètres
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Lecteur Windows Media, objet Paramètres
- Lecteur Windows Media modèle objet, objet Paramètres
- modèle objet, objet Paramètres
- Lecteur Windows Media contrôle ActiveX, objet Paramètres
- contrôle ActiveX, objet Paramètres
- Lecteur Windows Media contrôle Mobile ActiveX, objet Paramètres
- Lecteur Windows Media Mobile, objet Paramètres
- objet Paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919423"
---
# <a name="about-the-settings-object"></a>à propos de l’objet Paramètres

l’objet **Paramètres** régit les paramètres du contrôle tels que volume, play count, mute, etc. elle est accessible uniquement par le biais de la propriété **Paramètres** de l’objet **Player** . la propriété **Paramètres** retourne l’objet **Paramètres** . vous pouvez uniquement accéder aux propriétés de l’objet **Paramètres** une fois que vous l’avez créé. Par exemple, pour obtenir la valeur de la propriété **volume** , vous devez utiliser le code suivant :


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modèle objet de lecteur pour les langages de script**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> </dl>

 

 




