---
title: À propos de l’objet Settings
description: À propos de l’objet Settings
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player, objet Settings
- Modèle d’objet du lecteur Windows Media, objet paramètres
- modèle objet, objet Settings
- Contrôle ActiveX du lecteur Windows Media, objet paramètres
- Contrôle ActiveX, objet Settings
- Contrôle ActiveX Windows Media Player Mobile, paramètres (objet)
- Windows Media Player Mobile, objet Settings
- Settings (objet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839453"
---
# <a name="about-the-settings-object"></a>À propos de l’objet Settings

L’objet **Settings** régit les paramètres du contrôle tels que volume, Play Count, MUTE, etc. Elle est accessible uniquement par le biais de la propriété **Settings** de l’objet **Player** . La propriété **Settings** retourne l’objet **Settings** . Vous pouvez uniquement accéder aux propriétés de l’objet **Settings** après l’avoir créé. Par exemple, pour obtenir la valeur de la propriété **volume** , vous devez utiliser le code suivant :


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modèle objet de lecteur pour les langages de script**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Settings (objet)**](settings-object.md)
</dt> </dl>

 

 




