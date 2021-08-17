---
title: Problèmes multithread
description: Problèmes multithread
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ffd1dc3f73c33ca30ebee0072f1c5059c73f25e9e2318d384cd0c3d0dc7bc94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918529"
---
# <a name="multi-threaded-issues"></a>Problèmes multithread

OLE assure la prise en charge des applications multithread, ce qui permet aux applications d’effectuer des appels OLE à partir de plusieurs threads. Cette prise en charge multithread est appelée modèle cloisonné. il est important que tous les composants OLE qui utilisent plusieurs threads suivent ce modèle. Le modèle cloisonné requiert que les pointeurs d’interface soient marshalés (à l’aide de [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)et [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) lorsqu’ils sont transmis entre les threads.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Processus, threads et Apartments](processes--threads--and-apartments.md)
</dt> </dl>

 

 




