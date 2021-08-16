---
title: Error, objet (kit de développement logiciel (SDK) WMP)
description: L’objet Error donne accès à une collection d’objets ErrorItem.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- objet d’erreur Lecteur Windows Media
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c8e5b7627db2c55eb41a267f6c8d3a7a779e2f20190ca3061a49a41eb8577adb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748468"
---
# <a name="error-object"></a>Error, objet

L’objet **Error** donne accès à une collection d’objets [ErrorItem](erroritem-object.md) .

L’objet **Error** prend en charge la propriété suivante.



| Propriété                           | Description                                        |
|------------------------------------|----------------------------------------------------|
| [errorCount](error-errorcount.md) | Récupère le nombre d’erreurs dans la file d’attente d’erreurs. |



 

L’objet **Error** prend en charge les méthodes suivantes.



| Méthode                                       | Description                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [clearErrorQueue](error-clearerrorqueue.md) | Efface les erreurs de la file d’attente des erreurs.                                                         |
| [item](error-item.md)                       | Récupère un objet [ErrorItem](erroritem-object.md) à partir de la file d’attente des erreurs.                     |
| [aide à la](error-webhelp.md)                 | lance la Lecteur Windows Media page d’aide Web pour afficher des informations supplémentaires sur l’erreur. |



 

L’objet d' **erreur** est accessible via la propriété suivante.



| Object                      | Propriété                  |
|-----------------------------|---------------------------|
| [Lecteur](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




