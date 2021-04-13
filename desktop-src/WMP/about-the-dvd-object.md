---
title: À propos de l’objet DVD
description: À propos de l’objet DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Lecteur Windows Media, objet DVD
- Modèle objet lecteur Windows Media, objet DVD
- modèle objet, objet DVD
- Contrôle ActiveX du lecteur Windows Media, objet DVD
- Contrôle ActiveX, objet DVD
- Contrôle ActiveX mobile du lecteur Windows Media, objet DVD
- Windows Media Player Mobile, objet DVD
- Objet DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309302"
---
# <a name="about-the-dvd-object"></a>À propos de l’objet DVD

L’objet **DVD** ajoute des fonctionnalités spécifiques au support DVD. Dans un sens général, les DVD sont traités comme d’autres médias numériques dans le lecteur Windows Media. Par exemple, les lecteurs de DVD sont énumérés à l’aide de l’objet **CdromCollection** et les titres des DVD et les chapitres sont manipulés à l’aide des objets de **sélection** et des objets **multimédias** . Toutefois, certaines fonctionnalités sont spécifiques aux DVD et l’objet **DVD** en fournit. Par exemple, le DVD a un concept appelé domaine. Pour récupérer le domaine actuel pour un support DVD, tapez la commande suivante :


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objet DVD**](dvd-object.md)
</dt> <dt>

[**Modèle objet de lecteur pour les langages de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




