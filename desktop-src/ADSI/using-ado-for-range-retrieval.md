---
title: Utilisation d’ADO pour la récupération de plages
description: Si un langage Automation est utilisé, les objets d’annuaire ActiveX (ADO) doivent être utilisés pour récupérer une plage de valeurs de propriété. Lorsque vous utilisez ADO pour la récupération de plages, il existe un problème qui doit être traité spécifiquement.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Utilisation d’ADO pour l’ADSI de récupération de plages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671110"
---
# <a name="using-ado-for-range-retrieval"></a>Utilisation d’ADO pour la récupération de plages

Si un langage Automation est utilisé, les objets d’annuaire ActiveX (ADO) doivent être utilisés pour récupérer une plage de valeurs de propriété.

Lorsque vous utilisez ADO pour la récupération de plages, il existe un problème qui doit être traité spécifiquement. Lors de l’interrogation du groupe final de valeurs de propriété, l’objet ADO récupère zéro objet, même s’il en reste. Pour récupérer les valeurs restantes, utilisez le caractère générique de plage « \* ». Par exemple, si un groupe contient 150 membres, les valeurs de membre 0-100 peuvent être récupérées normalement à l’aide d’une récupération étendue. Si la plage 101-200 est ensuite demandée, l’objet ADO ne retourne aucun objet. À ce stade, il est nécessaire de modifier la requête pour demander la plage 101- \* . Cela permet de récupérer des valeurs comprises entre 101 et 150. Pour plus d’informations et pour obtenir un exemple de code, consultez [exemple de code pour l’utilisation de pour récupérer des membres d’un groupe](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).

Pour plus d’informations sur l’utilisation d’ADO pour la récupération de plages, consultez :

-   [Dialecte LDAP ADO](ado-ldap-ranging-dialect.md)
-   [Dialecte SQL ADO](ado-sql-ranging-dialect.md)
-   [Exemple de code pour l’utilisation de permettant de récupérer des membres d’un groupe](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




