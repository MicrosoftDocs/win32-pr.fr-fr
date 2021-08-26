---
description: Chaque assembly côte à côte doit avoir une version.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versions d’assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e555035bf7b43f53d3a68f249005928867f453b78522f70dd45f3b5379c75e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885569"
---
# <a name="assembly-versions"></a>Versions d’assembly

Chaque assembly côte à côte doit avoir une version. Chaque version d’assembly est associée à un numéro de version comportant quatre parties séparées par des points : *major. minor. Build. Revision*. Si une modification est apportée à un assembly qui le rend incompatible avec les versions existantes, les parties *majeures* ou *secondaires* du numéro de version doivent être modifiées. Un numéro de version qui change uniquement dans les parties de *Build* ou de *révision* indique que l’assembly est à compatibilité descendante avec les versions antérieures.

La version doit être spécifiée dans les éléments **assemblyIdentity** des [manifestes](manifests.md). Utilisez le format de version en quatre parties : MMMM. nnnnn. ooooo. ppppp. Chacun des composants séparés par des points peut être de 0-65535 inclus.

 

 



