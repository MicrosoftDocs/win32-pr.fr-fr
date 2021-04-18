---
title: Error, objet (kit de développement logiciel (SDK) WMP)
description: L’objet Error donne accès à une collection d’objets ErrorItem.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Objet d’erreur Windows Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2019
ms.locfileid: "106512487"
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
| [aide à la](error-webhelp.md)                 | Ouvre la page d’aide Web du lecteur Windows Media pour afficher des informations supplémentaires sur l’erreur. |



 

L’objet d' **erreur** est accessible via la propriété suivante.



| Object                      | Propriété                  |
|-----------------------------|---------------------------|
| [Lecteur](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




