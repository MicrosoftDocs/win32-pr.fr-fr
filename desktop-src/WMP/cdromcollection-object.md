---
title: Objet CdromCollection
description: L’objet CdromCollection permet d’organiser et d’accéder à une collection de lecteurs de CD ou DVD.
ms.assetid: 02429ba7-a053-42bf-9ed5-c05e13c964c0
keywords:
- objet CdromCollection Lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f8fe20bc138feb3eb1ad5bc937ef1f53f0e6b08e5757bbe03791177fe4c3531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863949"
---
# <a name="cdromcollection-object"></a>Objet CdromCollection

L’objet **CdromCollection** permet d’organiser et d’accéder à une collection de lecteurs de CD ou DVD.

L’objet **CdromCollection** prend en charge la propriété suivante.



| Propriété                           | Description                                                        |
|------------------------------------|--------------------------------------------------------------------|
| [count](cdromcollection-count.md) | Récupère le nombre de lecteurs de CD et de DVD disponibles sur le système. |



 

L’objet **CdromCollection** prend en charge les méthodes suivantes.



| Méthode                                                         | Description                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [getByDriveSpecifier](cdromcollection-getbydrivespecifier.md) | Récupère l’objet [cdrom](cdrom-object.md) associé à une lettre de lecteur particulière. |
| [item](cdromcollection-item.md)                               | Récupère l’objet [cdrom](cdrom-object.md) à l’index donné.                        |



 

L’objet **CdromCollection** est accessible par le biais de la propriété suivante.



| Object                      | Propriété                                      |
|-----------------------------|-----------------------------------------------|
| [Lecteur](player-object.md) | [cdromCollection](player-cdromcollection.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




