---
title: À propos de l’objet réseau
description: À propos de l’objet réseau
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Lecteur Windows Media, objet réseau
- Modèle objet du lecteur Windows Media, objet réseau
- modèle objet, objet réseau
- Contrôle ActiveX du lecteur Windows Media, objet réseau
- Contrôle ActiveX, objet réseau
- Contrôle ActiveX Windows Media Player Mobile, objet réseau
- Windows Media Player Mobile, objet réseau
- Objet réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671401"
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

 

 




