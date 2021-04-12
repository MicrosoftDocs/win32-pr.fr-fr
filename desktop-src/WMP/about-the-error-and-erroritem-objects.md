---
title: À propos des objets Error et ErrorItem
description: À propos des objets Error et ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Lecteur Windows Media, objet d’erreur
- Modèle d’objet du lecteur Windows Media, objet d’erreur
- modèle objet, objet d’erreur
- Contrôle ActiveX du lecteur Windows Media, objet d’erreur
- Contrôle ActiveX, objet d’erreur
- Contrôle ActiveX Windows Media Player Mobile, objet d’erreur
- Windows Media Player Mobile, objet d’erreur
- Objet d’erreur
- Lecteur Windows Media, objet ErrorItem
- Modèle objet du lecteur Windows Media, objet ErrorItem
- modèle objet, objet ErrorItem
- Contrôle ActiveX du lecteur Windows Media, objet ErrorItem
- Contrôle ActiveX, objet ErrorItem
- Contrôle ActiveX Windows Media Player Mobile, objet ErrorItem
- Windows Media Player Mobile, objet ErrorItem
- Objet ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310261"
---
# <a name="about-the-error-and-erroritem-objects"></a>À propos des objets Error et ErrorItem

Les objets **Error** et **ErrorItem** régissent les fonctionnalités de gestion des erreurs du lecteur Windows Media. L’objet **Error** est obtenu à partir de l’objet **Player** via la propriété **Error** . Vous pouvez obtenir un code spécifique à partir de l’objet d' **erreur** à l’aide de la propriété **Item** de l’objet **Error** pour créer l’objet **ErrorItem** . Par exemple, pour obtenir le code d’erreur du premier élément d’erreur, tapez :


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

 

 




