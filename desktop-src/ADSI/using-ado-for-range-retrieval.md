---
title: Utilisation d’ADO pour la récupération de plages
description: si un langage automation est utilisé, les objets d’annuaire d’ActiveX (ADO) doivent être utilisés pour récupérer une plage de valeurs de propriété. Lorsque vous utilisez ADO pour la récupération de plages, il existe un problème qui doit être traité spécifiquement.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Utilisation d’ADO pour l’ADSI de récupération de plages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523cd65e7d26a82b9b647913c919bef374b1c76ddf1a18fd9f99384b4ae6e483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023047"
---
# <a name="using-ado-for-range-retrieval"></a>Utilisation d’ADO pour la récupération de plages

si un langage automation est utilisé, les objets d’annuaire d’ActiveX (ADO) doivent être utilisés pour récupérer une plage de valeurs de propriété.

Lorsque vous utilisez ADO pour la récupération de plages, il existe un problème qui doit être traité spécifiquement. Lors de l’interrogation du groupe final de valeurs de propriété, l’objet ADO récupère zéro objet, même s’il en reste. Pour récupérer les valeurs restantes, utilisez le caractère générique de plage « \* ». Par exemple, si un groupe contient 150 membres, les valeurs de membre 0-100 peuvent être récupérées normalement à l’aide d’une récupération étendue. Si la plage 101-200 est ensuite demandée, l’objet ADO ne retourne aucun objet. À ce stade, il est nécessaire de modifier la requête pour demander la plage 101- \* . Cela permet de récupérer des valeurs comprises entre 101 et 150. Pour plus d’informations et pour obtenir un exemple de code, consultez [exemple de code pour l’utilisation de pour récupérer des membres d’un groupe](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).

Pour plus d’informations sur l’utilisation d’ADO pour la récupération de plages, consultez :

-   [Dialecte LDAP ADO](ado-ldap-ranging-dialect.md)
-   [dialecte SQL ADO](ado-sql-ranging-dialect.md)
-   [Exemple de code pour l’utilisation de permettant de récupérer des membres d’un groupe](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




