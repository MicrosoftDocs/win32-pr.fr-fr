---
title: Fonctions de l’utilitaire NAP
description: Les fonctions utilitaires suivantes prennent en charge l’API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672733"
---
# <a name="nap-utility-functions"></a>Fonctions de l’utilitaire NAP

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

Les fonctions utilitaires suivantes prennent en charge l’API NAP.

Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et l’allocateur de mémoire COM (CoTaskMemAlloc et CoTaskMemFree).

-   DANS les paramètres, alloué et libéré par l’appelant.
-   Paramètres OUT — alloués par l’appelé, libérés par l’appelant à l’aide de CoTaskMem \* ()
-   Paramètres IN/OUT — alloués par l’appelant, libérés et réalloués par l’appelé, libérés en fin de terme par l’appelant, à l’aide de CoTaskMem \* ()

Dans les fonctions FreeXxx (), tous les pointeurs incorporés sont également libérés.

-   [**AllocConnections**](allocconnections-func.md)
-   [**AllocCountedString**](alloccountedstring-func.md)
-   [**AllocFixupInfo**](allocfixupinfo-func.md)
-   [**FreeConnections**](freeconnections-func.md)
-   [**FreeCountedString**](freecountedstring-func.md)
-   [**FreeFixupInfo**](freefixupinfo-func.md)
-   [**FreeIsolationInfo**](freeisolationinfo-func.md)
-   [**FreeIsolationInfoEx**](freeisolationinfoex.md)
-   [**FreeNapComponentRegistrationInfoArray**](freenapcomponentregistrationinfoarray-func.md)
-   [**FreeNetworkSoH**](freenetworksoh-func.md)
-   [**FreePrivateData**](freeprivatedata-func.md)
-   [**FreeSoH**](freesoh-func.md)
-   [**FreeSoHAttributeValue**](freesohattributevalue-func.md)
-   [**FreeSystemHealthAgentState**](freesystemhealthagentstate-func.md)
-   [**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
-   [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)

 

 




