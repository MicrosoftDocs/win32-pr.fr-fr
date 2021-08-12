---
title: À propos de l’objet DVD
description: À propos de l’objet DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Lecteur Windows Media, objet DVD
- modèle objet Lecteur Windows Media, objet DVD
- modèle objet, objet DVD
- Lecteur Windows Media ActiveX contrôle, objet DVD
- contrôle ActiveX, objet DVD
- Lecteur Windows Media contrôle Mobile ActiveX, objet DVD
- Lecteur Windows Media Mobile, objet DVD
- Objet DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109587f30e7df0ff49b1cdbe5b45d818decb1a3f50ffe4a4ba9cde53d00833f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583761"
---
# <a name="about-the-dvd-object"></a>À propos de l’objet DVD

L’objet **DVD** ajoute des fonctionnalités spécifiques au support DVD. dans un sens général, les DVD sont traités comme d’autres médias numériques dans Lecteur Windows Media. Par exemple, les lecteurs de DVD sont énumérés à l’aide de l’objet **CdromCollection** et les titres des DVD et les chapitres sont manipulés à l’aide des objets de **sélection** et des objets **multimédias** . Toutefois, certaines fonctionnalités sont spécifiques aux DVD et l’objet **DVD** en fournit. Par exemple, le DVD a un concept appelé domaine. Pour récupérer le domaine actuel pour un support DVD, tapez la commande suivante :


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objet DVD**](dvd-object.md)
</dt> <dt>

[**Modèle objet de lecteur pour les langages de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




