---
title: Routines de saisie semi-automatique HTTP
description: Les applications disposent de plusieurs options pour recevoir des indications d’achèvement et offrir une certaine flexibilité aux développeurs.
ms.assetid: c48a64d2-b6c8-4694-8600-f84751954bad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd80259d806d81153a649ad606e40c10986090442e3cab5e04bd864367441871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981669"
---
# <a name="http-completion-routines"></a>Routines de saisie semi-automatique HTTP

Les applications disposent de plusieurs options pour recevoir des indications d’achèvement et offrir une certaine flexibilité aux développeurs. Les options doivent être bloquées en attendant la fin d’un appel d’API ou l’utilisation de routines de saisie semi-automatique pour les opérations asynchrones. L’avantage de l’utilisation des opérations asynchrones est l’augmentation de la réactivité de l’application.

## <a name="blocked-io"></a>E/s bloquées

Les applications peuvent se bloquer en attendant la fin de l’appel d’API en affectant à la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) la **valeur null**. Cela bloque véritablement toutes les opérations sur le thread. Par exemple, dans les appels à [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect), l’appel est bloqué jusqu’à ce que la connexion soit interrompue.

## <a name="asynchronous-io"></a>E/s asynchrones

Les applications qui préfèrent ne pas bloquer peuvent utiliser la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) pour obtenir les résultats de la saisie semi-automatique. L’application fournit un pointeur vers une structure **OVERLAPPED** , qui est utilisée avec un objet d’événement ou un port de terminaison. Avec un port de terminaison d’e/s, un descripteur HTTP est utilisé comme handle de fichier dans une opération d’e/s de fichier asynchrone. Le tableau suivant récapitule les options de saisie semi-automatique disponibles pour les applications.



| Structure OVERLAPPED | Objet d’événement   | Port de terminaison | Completion                                                                                                   |
|----------------------|----------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| **NULL**             | Non applicable | Ignoré         | L’opération se termine de façon synchrone.                                                                           |
| Non **null**         | Non **null**   | **NULL**        | L’opération se termine de façon asynchrone. Une notification Overlapped est effectuée en signalant un objet d’événement.       |
| Non **null**         | Ignoré        | Non **null**    | L’opération se termine de façon asynchrone. Une notification Overlapped est effectuée en planifiant une routine de saisie semi-automatique. |



 

## <a name="returning-the-number-of-bytes-read"></a>Retour du nombre d’octets lus

Certaines des fonctions qui utilisent la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) pour la saisie semi-automatique asynchrone retournent un paramètre *PBytesReceived* (ou *pBytesSent* ou *pBytesRead*) qui indique le nombre d’octets transférés de façon synchrone. Pour les appels asynchrones, ce paramètre doit avoir la valeur **null**. Pour les appels synchrones, le paramètre *pBytesReceived* est facultatif et peut avoir la **valeur null** ou non **null**.

Si l’objet d’événement est utilisé pour la saisie semi-automatique asynchrone, la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) est appelée pour déterminer le nombre d’octets lus. Si le port de terminaison est utilisé (le paramètre *hFile* est associé à un port de terminaison d’e/s), l’application appelle la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) pour déterminer le nombre d’octets lus. Si les opérations asynchrones ne sont pas terminées, les applications peuvent appeler la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir des informations d’erreur étendues.

Le tableau suivant résume le comportement de la saisie semi-automatique synchrone et asynchrone dans des fonctions telles que [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) qui utilisent le paramètre *pBytesReceived* .



| pBytesReceived\* | pOverlapped  | Description                                                                             |
|------------------|--------------|-----------------------------------------------------------------------------------------|
| **NULL**         | **NULL**     | L’application ne reçoit pas d’informations sur le nombre d’octets retournés.           |
| **NULL**         | Non **null** | Opération asynchrone, *pBytesReceived* est inutile.                                |
| Non **null**     | **NULL**     | Opération synchrone, nombre d’octets retournés dans *pBytesReceived*.                    |
| Non **null**     | Non **null** | Opération asynchrone, *pBytesReceived* est ignoré, même s’il n’est pas **null**.\*\* |



 

> [!Note]  
> \*Ce paramètre peut également être *pBytesSent* ou *pBytesRead*.

 

> [!Note]  
> \*\*Il est recommandé que les applications passent une **valeur null** dans *pBytesReceived* pour les opérations asynchrones et obtiennent le nombre d’octets reçus à partir de [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) ou [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

 

## <a name="return-codes"></a>Codes de retour

L’API du serveur HTTP retourne trois classes de codes pour les appels de fonction asynchrones.

-   AUCUNE \_ erreur
-   ERREUR d' \_ e/s \_ en attente
-   Tout autre [code d’erreur système](/windows/desktop/Debug/system-error-codes).

Quand les \_ e/s \_ d’erreur en attente ou aucune \_ erreur sont retournées par l’appel de fonction asynchrone, les utilisateurs doivent s’attendre à ce que l’événement ou la routine de saisie semi-automatique soit signalé. L’appel de la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) pour l’événement ou la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) pour le port de terminaison retourne l’état d’achèvement. En outre, si aucune \_ erreur n’est retournée, les applications peuvent effectuer un traitement postérieur sur le thread qui a effectué l’appel d’API.

Si l’API du serveur HTTP retourne autre chose que l’erreur \_ e/s \_ en attente ou aucune \_ erreur, à partir de l’appel de fonction asynchrone, la routine d’achèvement n’est pas signalée et l’erreur est retournée directement par l’API.

 

 