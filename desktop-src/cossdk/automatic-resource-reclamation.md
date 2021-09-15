---
description: Récupération automatique des ressources
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Récupération automatique des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403561"
---
# <a name="automatic-resource-reclamation"></a>Récupération automatique des ressources

COM+ notifie le gestionnaire de distribution à chaque expiration de la durée de vie d’un objet. Le gestionnaire de distribution avertit ensuite le détenteur de chaque distributeur de ressources inscrit pour voir s’il possède des ressources encore détenues par cet objet. Si c’est le cas, ces ressources sont libérées, empêchant les fuites de ressources par les composants qui obtiennent des ressources via un distributeur de ressources.

La fonctionnalité de récupération automatique est une option qui est désactivée par défaut. Un distributeur de ressources peut choisir d’activer cette option et, à cette fin, garantit qu’une référence à une ressource distribuée à un objet n’est jamais retournée par les méthodes d’objet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts du distributeur de ressources COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



