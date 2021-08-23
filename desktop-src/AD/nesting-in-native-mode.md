---
title: Imbrication en mode natif
description: La liste suivante décrit ce qui peut être contenu dans un groupe qui existe dans un domaine en mode natif.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Imbrication dans AD en mode natif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3fa2842981354738cd4ef112ef278fa33ca310adeedcd62fb245a2663cce07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025737"
---
# <a name="nesting-in-native-mode"></a>Imbrication en mode natif

La liste suivante décrit ce qui peut être contenu dans un groupe qui existe dans un domaine en mode natif. Cette même liste s’applique également aux groupes de distribution dans les domaines en mode mixte. L’étendue du groupe détermine ces règles de relation contenant-contenu.

-   Un groupe universel peut contenir d’autres groupes universels, groupes globaux et comptes issus de n’importe quel domaine de la forêt dans laquelle ce groupe universel réside.
-   Un groupe global peut contenir d’autres groupes globaux et comptes du même domaine auquel le groupe appartient. Un groupe global ne peut pas contenir de groupes universels, ni de groupe global ou de compte d’un autre domaine.
-   Un groupe de domaine local peut contenir des groupes universels, des groupes globaux et des comptes d’un domaine ou d’une forêt. Un groupe de domaine local peut également contenir d’autres groupes locaux de domaine du même domaine auquel le groupe appartient. Un groupe de domaine local ne peut pas contenir d’autres groupes locaux de domaine de n’importe quel autre domaine ou forêt.

 

 




