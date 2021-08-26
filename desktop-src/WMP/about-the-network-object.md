---
title: À propos de l’objet réseau
description: À propos de l’objet réseau
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Lecteur Windows Media, objet réseau
- Lecteur Windows Media modèle objet, objet réseau
- modèle objet, objet réseau
- Lecteur Windows Media ActiveX contrôle, objet réseau
- contrôle ActiveX, objet réseau
- Lecteur Windows Media contrôle Mobile ActiveX, objet réseau
- Lecteur Windows Media Mobile, objet réseau
- Objet réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0378b1cd4469f6141a4ea60021f2d54e5c32b33ae1943624f7c65f70aa2a655f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903289"
---
# <a name="about-the-network-object"></a>À propos de l’objet réseau

L’objet **réseau** régit les propriétés qui vous permettent de déterminer le degré de diffusion du contenu sur le réseau. Par exemple, vous pouvez déterminer si les paquets sont perdus et prendre les mesures appropriées. L’objet **réseau** est accessible uniquement par le biais de la propriété **réseau** de l’objet **Player** . La propriété **Network** retourne l’objet **réseau** . Vous pouvez uniquement accéder aux propriétés de l’objet **réseau** après l’avoir créé. Par exemple, pour utiliser la propriété **Bandwidth** , vous devez utiliser le code suivant :


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objet réseau**](network-object.md)
</dt> <dt>

[**Modèle objet de lecteur pour les langages de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




