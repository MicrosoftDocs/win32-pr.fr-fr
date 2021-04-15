---
description: États des ressources regroupées accessibles au distributeur de ressources COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: États des ressources regroupées accessibles au distributeur de ressources COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483432"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a>États des ressources regroupées accessibles au distributeur de ressources COM+

À tout moment, une ressource est en cours d’utilisation ou n’est pas utilisée et est inscrite ou n’est pas inscrite dans une transaction. Cela donne quatre États de ressources possibles, comme suit :

-   **Ressources dans un inventaire désinscrit.** Une ressource qui n’est pas utilisée par un objet et qui n’est pas inscrit dans une transaction est dans un inventaire non inscrit. Une ressource de l’inventaire général est disponible pour l’attribution.

-   **Ressources dans l’inventaire inscrit.** Une ressource qui n’est pas utilisée par un objet mais qui est inscrit dans une transaction est dans un inventaire inscrit. Une telle ressource est disponible pour une attribution uniquement aux objets s’exécutant dans la même transaction. Une ressource passe d’un inventaire inscrit à un inventaire non inscrit lorsque COM+ notifie le gestionnaire du distributeur que la transaction est terminée.

-   **Ressources dans un usage désinscrit.** Si une ressource est affectée à un objet et que l’instance n’est pas exécutée dans une transaction ou que le distributeur de ressources a identifié la ressource comme non transactionnelle, cette ressource est désinscrite.

-   **Ressources dans un usage inscrit.** Si une ressource est assignée à un objet, l’instance s’exécute dans une transaction et le distributeur de ressources a correctement inscrit la ressource dans la transaction, cette ressource est dans un usage inscrit.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts du distributeur de ressources COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Inscription d’une ressource dans une transaction](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



