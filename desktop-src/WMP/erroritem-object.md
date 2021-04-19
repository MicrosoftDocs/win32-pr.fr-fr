---
title: Objet ErrorItem
description: L’objet ErrorItem permet d’accéder aux informations sur les erreurs.
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- Objet ErrorItem lecteur Windows Media
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c273d00477363c66c49dfa1f77a66dab42c711cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509013"
---
# <a name="erroritem-object"></a>Objet ErrorItem

L’objet **ErrorItem** permet d’accéder aux informations sur les erreurs.

L’objet **ErrorItem** prend en charge les propriétés suivantes.



| Propriété                                           | Description                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [condition](erroritem-condition.md)               | Récupère une valeur indiquant la condition de l’erreur.                                       |
| [customUrl](erroritem-customurl.md)               | Récupère l’URL d’un site Web qui affiche des informations spécifiques sur l’échec du téléchargement du codec. |
| [errorCode](erroritem-errorcode.md)               | Récupère le code d’erreur actuel.                                                               |
| [errorContext](erroritem-errorcontext.md)         | Récupère une valeur indiquant le contexte de l’erreur.                                          |
| [errorDescription](erroritem-errordescription.md) | Récupère une description de l’erreur.                                                           |
| **corriger**                                         | Réservé pour un usage futur.                                                                        |



 

L’objet **ErrorItem** est accessible par le biais des méthodes suivantes.



| Object                    | Méthode                   |
|---------------------------|--------------------------|
| [Error](error-object.md) | [item](error-item.md)   |
| [Média](media-object.md) | [error](media-error.md) |



 

À des fins d’illustration, *joueur*. *erreur*. *Item*(*index*) est utilisé dans les sections de syntaxe de référence.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




