---
title: Réplication et intégrité des données
description: Active Directory Domain Services fournir une mise à jour multimaître.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation, réplication et intégrité des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512227"
---
# <a name="replication-and-data-integrity"></a>Réplication et intégrité des données

Active Directory Domain Services fournir *une mise à jour multimaître*. La mise à jour à plusieurs maîtres signifie que tous les réplicas complets d’une partition donnée sont accessibles en écriture (les réplicas partiels sur les serveurs de catalogue global ne sont pas accessibles en écriture). Une mise à jour multimaître signifie que les mises à jour ne sont pas bloquées, même lorsque certains réplicas sont inutilisables. Le serveur Active Directory propage les modifications à partir du réplica mis à jour vers tous les autres réplicas. La réplication est automatique et transparente.

Pour plus d'informations, consultez les rubriques ci-dessous.

-   [Le modèle de réplication dans Active Directory Domain Services](replication-model-in-active-directory-domain-services.md)
-   [Comportement de réplication dans Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md)
-   [Détection et prévention de la latence de réplication](detecting-and-avoiding-replication-latency.md)

 

 




