---
title: Fonctionnalités du modèle de réplication pour Active Directory Domain Services
description: Le modèle de réplication utilisé dans Active Directory Domain Services est appelé cohérence non-maître avec convergence.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, modèle de réplication
- Fonctionnalités du modèle de réplication Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd113ffe4182be47c9e8c84404fc748e417e78c866e41298ad19d8e7a0dec555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189530"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a>Fonctionnalités du modèle de réplication pour Active Directory Domain Services

Le modèle de réplication utilisé dans Active Directory Domain Services est appelé *cohérence non-maître avec convergence*. Dans ce modèle, le répertoire peut avoir de nombreux réplicas ; un système de réplication propage les modifications apportées à un réplica donné vers tous les autres réplicas. Il n’est pas garanti que les réplicas soient cohérents entre eux à un moment donné (« faible cohérence »), car les modifications peuvent être appliquées à n’importe quel réplica à tout moment (« multi-maître »). Si le système est autorisé à atteindre un état stable et qu’aucune nouvelle mise à jour n’est en cours et que toutes les mises à jour précédentes ont été complètement répliquées, tous les réplicas sont assurés de converger sur le même ensemble de valeurs (« convergence »).

 

 




