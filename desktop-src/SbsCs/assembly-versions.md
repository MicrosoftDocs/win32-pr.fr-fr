---
description: Chaque assembly côte à côte doit avoir une version.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versions d’assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238116"
---
# <a name="assembly-versions"></a>Versions d’assembly

Chaque assembly côte à côte doit avoir une version. Chaque version d’assembly est associée à un numéro de version comportant quatre parties séparées par des points : *major. minor. Build. Revision*. Si une modification est apportée à un assembly qui le rend incompatible avec les versions existantes, les parties *majeures* ou *secondaires* du numéro de version doivent être modifiées. Un numéro de version qui change uniquement dans les parties de *Build* ou de *révision* indique que l’assembly est à compatibilité descendante avec les versions antérieures.

La version doit être spécifiée dans les éléments **assemblyIdentity** des [manifestes](manifests.md). Utilisez le format de version en quatre parties : MMMM. nnnnn. ooooo. ppppp. Chacun des composants séparés par des points peut être de 0-65535 inclus.

 

 



