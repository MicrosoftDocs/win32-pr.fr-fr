---
description: Types utilisés dans les interfaces de distributeur de ressources COM+
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: Types utilisés dans les interfaces de distributeur de ressources COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c4d0f62ec7c61a9bc0f189c1ee02d1868a3242
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310830"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a>Types utilisés dans les interfaces de distributeur de ressources COM+

Les types suivants sont utilisés dans les interfaces du distributeur de ressources.



| Type           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RESTYPID**   | **Valeur DWORD** qui identifie un type de ressource, et non une ressource particulière. Un **RESTYPID** est généralement un pointeur vers une structure dans la mémoire du distributeur, qui décrit le type de ressource. Le gestionnaire de distribution ne comprend pas (et n’a pas besoin de comprendre) cette structure dans la mémoire du distributeur de ressources. Le gestionnaire de distribution utilise **RESTYPID** uniquement pour faire référence à un type de ressource dans un distributeur de ressources.                                                                                                                                   |
| **RESID**      | **Valeur DWORD** qui identifie une ressource particulière, par opposition à un type de ressource. Un **RESID** est généralement un (**void \* *_) qui pointe vers une structure de la mémoire du distributeur de ressources qui représente la ressource. Le gestionnaire de distribution n’a pas besoin de comprendre cette structure dans la mémoire du distributeur de ressources. Le gestionnaire de distribution utilise _* RESID** pour faire référence à une ressource particulière dans un distributeur de ressources.                                                                                                                                 |
| **SRESID**     | Une version de chaîne Unicode de **RESID**, utilisée dans les méthodes [**IHolder :: TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) et [**IHolder :: UntrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) . Les chaînes sont parfois utiles lorsque seule une petite quantité d’informations doit être enregistrée sur une ressource et que l’intégralité de la description de la ressource peut être contenue dans le **SRESID**. En particulier, l’utilisation de **SRESID** peut parfois éliminer la nécessité d’une carte dans le distributeur de ressources lorsque la ressource représente une relation entre deux (ou plus) choses. |
| **TRANSID**    | Identifie une transaction. Ce type peut être converti en interface **ITransaction** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **TIMEINSECS** | Indique la durée pendant laquelle une ressource peut être inactive avant d’être détruite.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts du distributeur de ressources COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfaces du distributeur de ressources COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



