---
title: Réplication et intégrité des données
description: Active Directory Domain Services fournir une mise à jour multimaître.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation, réplication et intégrité des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ec62ec3e44b9252d2d186b690105623b338bdaedf6ed15e4a253bfc2f06927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184454"
---
# <a name="replication-and-data-integrity"></a>Réplication et intégrité des données

Active Directory Domain Services fournir *une mise à jour multimaître*. La mise à jour à plusieurs maîtres signifie que tous les réplicas complets d’une partition donnée sont accessibles en écriture (les réplicas partiels sur les serveurs de catalogue global ne sont pas accessibles en écriture). Une mise à jour multimaître signifie que les mises à jour ne sont pas bloquées, même lorsque certains réplicas sont inutilisables. Le serveur Active Directory propage les modifications à partir du réplica mis à jour vers tous les autres réplicas. La réplication est automatique et transparente.

Pour plus d’informations, voir les rubriques suivantes :

-   [Le modèle de réplication dans Active Directory Domain Services](replication-model-in-active-directory-domain-services.md)
-   [Comportement de réplication dans Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md)
-   [Détection et prévention de la latence de réplication](detecting-and-avoiding-replication-latency.md)

 

 




