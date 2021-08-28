---
title: Allocation et désallocation de nœud par nœud
description: L’allocation nœud par nœud et la désallocation des structures de données par les stubs sont la méthode par défaut de gestion de la mémoire pour tous les paramètres sur le client et le serveur.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52aea7c2e95615af8549c1f66476e1a105b91abd68dd31089db9cf23d8ec2af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927838"
---
# <a name="node-by-node-allocation-and-deallocation"></a>Allocation et désallocation de nœud par nœud

L’allocation nœud par nœud et la désallocation des structures de données par les stubs sont la méthode par défaut de gestion de la mémoire pour tous les paramètres sur le client et le serveur. Côté client, le stub alloue chaque nœud avec un appel distinct à l' [ \_ \_ allocation d’utilisateur MIDL](/windows/desktop/Midl/midl-user-allocate-1). Côté serveur, au lieu d’appeler l' **\_ \_ allocation d’utilisateur MIDL**, la mémoire privée est utilisée chaque fois que cela est possible. Si **l' \_ \_ allocation d’utilisateur MIDL** est appelée, les stubs de serveur appellent **MIDL \_ User \_ Free** pour libérer les données. Dans la plupart des cas, l’utilisation de l’allocation et de la désallocation nœud par nœud au lieu d’utiliser **\[ allocate (tous les \_ nœuds) \]** entraîne une augmentation des performances des stubs côté serveur.

 

 