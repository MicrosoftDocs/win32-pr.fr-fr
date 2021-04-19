---
description: Bien que ce mécanisme soit suffisant pour les applications simples, il ne peut pas prendre en charge les exigences complexes de distribution des messages des applications plus avancées, telles que celles utilisant le modèle d’interface multidocument (MDI, multiple document interface).
ms.assetid: e4558e71-bbec-415a-a7c2-9025a4d6c474
title: Crochet bloquant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd098692784a662456c990a238bd309db0c321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513229"
---
# <a name="blocking-hook"></a>Crochet bloquant

Bien que ce mécanisme soit suffisant pour les applications simples, il ne peut pas prendre en charge les exigences complexes de distribution des messages des applications plus avancées, telles que celles utilisant le modèle d’interface multidocument (MDI, multiple document interface). Pour ces applications, un raccordement bloquant propre au thread peut être installé par l’application. Ce sera appelé par le fournisseur de services au lieu du hook de blocage par défaut décrit dans le précédent. Un fournisseur de services doit récupérer un pointeur vers le hook de blocage par thread à partir de la \_32.dll Ws2 en appelant [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback). Si l’application n’a pas installé son propre raccordement de blocage, un pointeur vers la fonction de raccordement de blocage par défaut sera retourné.

Un fournisseur de services Windows Sockets ne peut pas supposer qu’un raccordement bloquant fourni par l’application permet au traitement des messages de continuer comme le hook de blocage par défaut. Certaines applications ne peuvent pas tolérer la possibilité de réentrant des messages pendant qu’une opération de blocage est en attente. Une telle fonction de raccordement de blocage de l’application retourne simplement la **valeur false**. Si un fournisseur de services dépend des messages pour son fonctionnement interne, il peut exécuter **PeekMessage**(hMyWnd...) avant d’exécuter le hook de blocage de l’application afin qu’il puisse obtenir ses propres messages sans affecter le reste du système.

Aucun hook de blocage par défaut n’est installé dans les versions préemptif multithread de Windows. En effet, les autres processus ne sont pas bloqués si une seule application attend la fin d’une opération (et n’appelle donc pas **PeekMessage** ou **GetMessage** , ce qui amène l’application à générer le processeur dans Windows non préemptif). Lorsque le fournisseur de services appelle [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback) , un pointeur null est retourné, indiquant que le fournisseur doit utiliser des fonctions de blocage du système d’exploitation natives. Toutefois, pour préserver la compatibilité descendante, un raccordement de blocage fourni par l’application peut toujours être installé sur une base par thread dans Windows.

Le fournisseur de services Winsock appelle le hook de blocage uniquement si tous les éléments suivants sont vrais : la routine est définie comme étant capable de bloquer, le socket spécifié est un socket bloquant et la demande ne peut pas être effectuée immédiatement. Si seuls les sockets non bloquants et [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) / [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) au lieu de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) sont utilisés, le hook de blocage ne sera jamais appelé.

> [!Note]  
> Si, pendant l’utilisation de pseudoblocking pour bloquer un thread, un message Windows est reçu pour le thread, il existe un risque que le thread tente d’émettre un autre appel Winsock. En raison de la difficulté de gérer cette condition de manière sécurisée, la spécification de Windows Sockets 1,1 n’autorise pas ce comportement. Il n’est pas possible pour un thread donné d’effectuer plusieurs appels de fonction Winsock imbriqués. Un seul appel de fonction en suspens est autorisé pour un thread particulier. Les appels de fonction Winsock imbriqués échouent avec l’erreur WSAEINPROGRESS. Il convient de souligner que cette restriction s’applique aux opérations de blocage et de non-blocage, mais uniquement dans les environnements Windows Sockets 1,1. Il existe quelques exceptions à cette règle, y compris deux fonctions qui permettent à une application de déterminer si une opération de pseudoblocking est en cours, et d’annuler une telle opération si nécessaire. Celles-ci sont décrites dans les rubriques suivantes.

 

 

 
