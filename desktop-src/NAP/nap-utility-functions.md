---
title: Fonctions de l’utilitaire NAP
description: Les fonctions utilitaires suivantes prennent en charge l’API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b421069804a4047b511b775c7ffafe5b4b987eb0b0ad5105f48df0ed990e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620780"
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

 

 




