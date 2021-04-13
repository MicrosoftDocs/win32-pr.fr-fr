---
title: Problèmes multithread
description: Problèmes multithread
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380454"
---
# <a name="multi-threaded-issues"></a>Problèmes multithread

OLE assure la prise en charge des applications multithread, ce qui permet aux applications d’effectuer des appels OLE à partir de plusieurs threads. Cette prise en charge multithread est appelée modèle cloisonné. il est important que tous les composants OLE qui utilisent plusieurs threads suivent ce modèle. Le modèle cloisonné requiert que les pointeurs d’interface soient marshalés (à l’aide de [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)et [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) lorsqu’ils sont transmis entre les threads.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Processus, threads et Apartments](processes--threads--and-apartments.md)
</dt> </dl>

 

 




