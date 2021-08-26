---
title: À propos des objets Error et ErrorItem
description: À propos des objets Error et ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Lecteur Windows Media, objet d’erreur
- Lecteur Windows Media modèle objet, objet d’erreur
- modèle objet, objet d’erreur
- Lecteur Windows Media ActiveX contrôle, objet d’erreur
- contrôle ActiveX, objet Error
- Lecteur Windows Media contrôle de ActiveX Mobile, objet d’erreur
- Lecteur Windows Media Mobile, objet d’erreur
- Objet d’erreur
- Lecteur Windows Media, objet ErrorItem
- Lecteur Windows Media modèle objet, objet ErrorItem
- modèle objet, objet ErrorItem
- Lecteur Windows Media ActiveX contrôle, objet ErrorItem
- contrôle ActiveX, objet ErrorItem
- Lecteur Windows Media contrôle Mobile ActiveX, objet ErrorItem
- Lecteur Windows Media Mobile, objet ErrorItem
- Objet ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84dcd8e0961007c185640b32ac53d249d2e739ca5e1aa4247a6735e09b2a3242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004399"
---
# <a name="about-the-error-and-erroritem-objects"></a>À propos des objets Error et ErrorItem

les objets **error** et **ErrorItem** régissent les fonctionnalités de gestion des erreurs de Lecteur Windows Media. L’objet **Error** est obtenu à partir de l’objet **Player** via la propriété **Error** . Vous pouvez obtenir un code spécifique à partir de l’objet d' **erreur** à l’aide de la propriété **Item** de l’objet **Error** pour créer l’objet **ErrorItem** . Par exemple, pour obtenir le code d’erreur du premier élément d’erreur, tapez :


```C++
myerrorcode = player.error.item(0).errorCode;

```



Vous pouvez également appeler l’aide Web avec l’objet d' **erreur** à l’aide du code suivant :


```C++
player.error.webHelp();

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Error, objet**](error-object.md)
</dt> <dt>

[**Objet ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Modèle objet de lecteur pour les langages de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




