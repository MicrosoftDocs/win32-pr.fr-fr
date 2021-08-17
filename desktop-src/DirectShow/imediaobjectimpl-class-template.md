---
description: Le modèle de classe IMediaObjectImpl fournit une implémentation de base pour l’interface IMediaObject. pour plus d’informations sur l’utilisation de ce modèle, consultez utilisation du modèle de classe DMO.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Modèle de classe IMediaObjectImpl (Dmoimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b166836ff4da6100f61fca5d3a0c2887462b37adcbdd2ec61abeb919553a59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015577"
---
# <a name="imediaobjectimpl-class-template"></a>Modèle de classe IMediaObjectImpl

Le `IMediaObjectImpl` modèle de classe fournit une implémentation de base pour l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . pour plus d’informations sur l’utilisation de ce modèle, consultez [utilisation du modèle de classe DMO](using-the-dmo-class-template.md).

Ce `IMediaObjectImpl` modèle expose les membres suivants.



| Classe imbriquée                              | Description                                  |
|-------------------------------------------|----------------------------------------------|
| [**LockIt**](imediaobjectimpl-lockit.md) | Classe d’assistance qui verrouille et déverrouille l’DMO. |



 



| Méthode                                                                      | Description                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))                     | Détermine si tous les flux non facultatifs ont des types de média. |
| [**InputType**](/previous-versions/ms807633(v=msdn.10))                             | Récupère le type de média actuel pour un flux d’entrée spécifié.       |
| [**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))                       | Interroge si le type de média a été défini sur un flux d’entrée.           |
| [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))   | Interroge si un flux d’entrée peut accepter davantage d’entrées.               |
| [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))   | Interroge si un flux d’entrée peut accepter un type de média donné.       |
| [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10)) | Interroge si un flux de sortie peut accepter un type de média donné.      |
| [**Verrouillage**](/previous-versions/ms809100(v=msdn.10))                                       | Verrouille le DMO                                                        |
| [**OutputType**](/previous-versions/ms807644(v=msdn.10))                           | Récupère le type de média actuel pour un flux de sortie spécifié.      |
| [**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))                     | Interroge si le type de média a été défini sur un flux de sortie.          |
| [**Bloquer**](/previous-versions/ms809101(v=msdn.10))                                   | Déverrouille le DMO                                                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Dmoimpl. h</dt> </dl>                                                                     |
| Bibliothèque<br/> | <dl> <dt>Dmoguids. lib ; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DMO Faire](dmo-reference.md)
</dt> <dt>

[utilisation du modèle de classe DMO](using-the-dmo-class-template.md)
</dt> </dl>

 

 
