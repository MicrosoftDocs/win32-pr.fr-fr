---
description: Interfaces du distributeur de ressources COM+
ms.assetid: 66ee4dd6-15d2-49e8-89a3-6fbb5770cabf
title: Interfaces du distributeur de ressources COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7fa011681defaddc160e835c7caeb6719054f5e4397903a1716ae76f81c7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991519"
---
# <a name="com-resource-dispenser-interfaces"></a>Interfaces du distributeur de ressources COM+

Les composants d’application utilisent des distributeurs de ressources pour accéder aux informations partagées. Les interfaces décrites dans le tableau suivant fournissent des informations de référence détaillées pour les développeurs de distributeurs de ressources.



| Interfaces                                                | Description                                                                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)<br/>   | Cette interface est appelée par le détenteur du distributeur de ressources pour créer, inscrire, évaluer et détruire une ressource.<br/> |
| [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager)<br/> | Les distributeurs de ressources utilisent cette interface pour se connecter au gestionnaire du distributeur.<br/>                                    |
| [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)<br/>                     | Cette interface est utilisée pour préparer et gérer les ressources.<br/>                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts du distributeur de ressources COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Types utilisés dans les interfaces de distributeur de ressources COM+](types-used-in-com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 




