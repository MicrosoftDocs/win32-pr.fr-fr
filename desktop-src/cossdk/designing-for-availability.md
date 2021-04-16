---
description: La disponibilité est la capacité d’une application à tolérer les défaillances dans les ressources du serveur.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Conception pour la disponibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523548"
---
# <a name="designing-for-availability"></a>Conception pour la disponibilité

La disponibilité est la capacité d’une application à tolérer les défaillances dans les ressources du serveur. Cela signifie que le client continue à être traité par la défaillance et que, idéalement, l’échec est transparent pour le client. Évidemment, l’échec peut provenir de sources matérielles ou logicielles. vous devez donc développer dans les deux cas.

La disponibilité peut être affectée par les facteurs suivants :

-   Modèle d’application. Pour la haute disponibilité, assurez-vous que la logique d’application critique est effectuée à l’aide du service de [transactions com+](com--transactions.md) . En outre, l’utilisation d’un mécanisme de compensation peut être efficace pour s’assurer que les ressources restent dans un état sain après des échecs.
-   Modèle client. Intégrer la logique « réessayer en cas d’échec » à l’application cliente et s’efforcer de dégrader normalement l’application si les ressources ou les services ne sont pas disponibles. Comprenez ce que le client attend de l’application, et créez une conception qui permet d’autres solutions en cas de défaillance.
-   Disponibilité des données/États. Pour un accès cohérent aux données persistantes, utilisez le clustering Windows pour assurer la prise en charge du basculement.
-   Disponibilité du service. Vous pouvez utiliser l’équilibrage de la charge réseau pour équilibrer la charge des demandes IP entrantes sur un cluster de serveurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception pour le déploiement](designing-for-deployment.md)
</dt> <dt>

[Conception pour l’évolutivité](designing-for-scalability.md)
</dt> <dt>

[Conception pour la sécurité](designing-for-security.md)
</dt> </dl>

 

 



