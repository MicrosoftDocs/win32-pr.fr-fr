---
description: L’interface TAPI fournit un certain nombre de fonctions pour manipuler les handles d’appel, en déterminant la relation entre les lignes, les appels et l’adresse, et ainsi de suite.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Appeler une manipulation de handle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519027"
---
# <a name="call-handle-manipulation"></a>Appeler une manipulation de handle

L’interface TAPI fournit un certain nombre de fonctions pour manipuler les handles d’appel, en déterminant la relation entre les lignes, les appels et l’adresse, et ainsi de suite. La plupart de ces fonctionnalités sont implémentées strictement dans TAPI sans référence au fournisseur de services, à l’exception de [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid). Cette fonction récupère l’identificateur d’adresse d’un appel existant au sein de sa ligne. Les fournisseurs de services qui modélisent une ligne en tant que groupe d’identificateurs d’adresses peuvent choisir une adresse imprévisible pour un nouvel appel entrant ou sortant. Cette fonction fournit à TAPI des informations suffisantes pour implémenter l’opération [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) lorsqu’elle est appelée avec l' \_ option d’adresse LINECALLSELECT.

 

 
