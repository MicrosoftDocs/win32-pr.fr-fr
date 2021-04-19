---
title: Espace de noms
description: Un espace de noms est un contexte dans lequel les noms de tous les objets doivent être résolus sans ambiguïté.
ms.assetid: 7731f6b5-1efa-43bc-bd31-9b5183ec90dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb79ba44bfaab1ea50dd89961503176dc8fbd1a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106539847"
---
# <a name="namespace"></a>Espace de noms

Un espace de noms est un contexte dans lequel les noms de tous les objets doivent être résolus sans ambiguïté. Par exemple, Internet est un espace de noms DNS unique, dans lequel tous les périphériques réseau ayant un nom DNS peuvent être résolus en une adresse particulière (par exemple, est résolu `www.microsoft.com` en 207.46.131.13).

## <a name="flat-namespace"></a>Espace de noms plat

Un espace de noms peut être plat ou hiérarchique. Un espace de noms plat n’est pas bien adapté, car il ne peut croître que jusqu’à ce que tous les noms disponibles soient utilisés. Une fois qu’un nom est utilisé plusieurs fois dans un espace de noms, l’espace de noms ne respecte pas l’exigence pouvant être résolue sans ambiguïté.

## <a name="hierarchical-namespace"></a>Espace de noms hiérarchique

Un espace de noms hiérarchique est divisé en différentes zones, qui peuvent être considérées comme des sous-espaces de noms. Chaque zone est son propre sous-espace de noms dans l’espace de noms global. Par conséquent, chaque objet doit avoir un nom unique dans son sous-espace de noms pour avoir un nom pouvant être résolu de façon univoque dans la hiérarchie d’espaces de noms. Les espaces de noms hiérarchiques, alors, peuvent être mis à l’échelle vers des réseaux extrêmement volumineux &mdash; lorsque vous ajoutez des objets à l’espace de noms global, vous devez rechercher des noms uniques pour eux dans le sous-espace de noms auquel ils appartiennent.

Tous les espaces de noms DNS sont hiérarchiques. Les sous-espaces de noms de l’espace de noms hiérarchique DNS sont appelés *domaines*. Le nom unique d’un ordinateur au sein d’un domaine est appelé un *nom unique relatif*. Les ordinateurs ayant le même nom unique relatif peuvent exister dans différents sous-espaces de noms (domaines) de la hiérarchie d’espaces de noms, car ils peuvent être entièrement résolus en un objet unique au sein de l’ensemble de la hiérarchie DNS, à l’aide d’un nom de domaine complet (FQDN). Par exemple, vous pouvez avoir un serveur nommé *Server1* dans le domaine *widgets.Microsoft.com* (l’espace de noms *widgets.Microsoft.com* ) et un *Serveur1* dans l’espace de noms *gadgets.widgets.Microsoft.com* . Dans la mesure où ils se trouvent dans des sous-espaces de noms différents dans l’espace de noms hiérarchique, ils peuvent être résolus en différents noms de domaine complets &mdash; *server1.widgets.microsoft.com* et *server1.gadgets.widgets.Microsoft.com*.
