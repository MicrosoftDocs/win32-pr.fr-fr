---
description: Quand un opertion retourne SUCCESS, la fonction a réussi à atteindre un point défini par l’API sur une fonction par fonction.
ms.assetid: e4077d77-dee1-4f1a-a6ee-20ca2f92a1ec
title: Signification du succès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d183695e9dce9df88dea5fe9464f16163130cd0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544992"
---
# <a name="the-meaning-of-success"></a>Signification du succès

## <a name="tapi-2x"></a>TAPI 2. x

Lorsqu’une opération retourne un indicateur de réussite (soit de façon synchrone au retour de la fonction pour les opérations synchrones, soit de manière asynchrone via un message de [**\_ réponse de ligne**](./line-reply.md) ou de [**\_ réponse téléphonique**](./phone-reply.md) pour les opérations asynchrones), le code suivant est supposé être vrai :

-   La fonction a bien progressé jusqu’à un point défini par l’API sur une base fonction par fonction. Une fois ce point atteint, l’opération est complètement terminée, ou elle est dans un état tel que les messages d’État indépendants informent l’application de la progression suivante.

    Par exemple, l’implémentation d’un fournisseur de services de [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) doit retourner Success au plus tard lorsque l’appel passe à l’état d’appel de procédure. Dans l’idéal, le fournisseur doit indiquer la réussite dès que possible, par exemple lorsque l’appel passe à l’état d’appel de tonalité (le cas échéant). Une fois la réussite renvoyée à l’application, les \_ messages CALLSTATE de ligne informent l’application de la progression de l’appel. Les fournisseurs de services qui retardent le renvoi de l’indication de réussite **lineMakeCall** , par exemple, jusqu’à la fin de la numérotation, doivent savoir que ce fournisseur a un inconvénient, car la facilité d’utilisation au niveau de l’application peut être sévèrement limitée. Par exemple, il n’est pas possible pour un utilisateur d’annuler la demande d’appel en cours tant que la numérotation n’est pas terminée et que tous les chiffres n’ont pas été envoyés au commutateur.

-   Les fonctions qui retournent des informations (comme [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)) retournent Success uniquement lorsque les informations demandées sont disponibles pour l’application. Les fonctions qui retournent des handles (vers des lignes ou des appels) peuvent retourner SUCCESS uniquement une fois que le handle est valide. Aucun message ne doit être envoyé à propos de cette ligne ou appel avant la réussite de l’indication de la fonction qui a provoqué sa création. Le fournisseur de services est responsable de la suppression de ces messages.
-   Les fonctions qui activent certaines conditions permanentes (telles que [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)) retournent Success uniquement une fois la condition activée, et non lorsque la condition est de nouveau supprimée (par exemple, pas lorsque l’analyse de tous les chiffres est terminée).
-   Les fonctions de contrôle d’appel (telles que [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold) ou [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), mais pas [**LINEMAKECALL**](/windows/win32/api/tapi/nf-tapi-linemakecall)) retournent Success lorsque l’opération est terminée. Certains réseaux téléphoniques ne fournissent pas d’accusé de réception (positif ou négatif) sur l’achèvement de certaines demandes effectuées par les fournisseurs de services. Dans ce cas, le fournisseur de services doit décider de la réussite ou de l’échec de la demande. Par conséquent, la réussite peut indiquer que le fournisseur de services a initié des actions pour satisfaire la demande, mais pas nécessairement quelque chose de plus. Par exemple, le fournisseur peut recevoir des accusés de réception affirmatives à sa demande du commutateur, bien qu’il ait déjà envoyé un message de réussite à l’application.

## <a name="tapi-3x"></a>TAPI 3. x

Lorsqu’une opération retourne un indicateur de réussite (soit de façon synchrone au retour de la fonction pour les opérations synchrones, soit de manière asynchrone avec un appel à la procédure de rappel d' [**\_ achèvement Async**](/windows/win32/api/tspi/nc-tspi-async_completion) pour les opérations asynchrones), les éléments suivants sont supposés être vrais :

-   La fonction a progressé avec succès jusqu’à un point défini par le fournisseur de services. Le fournisseur de services définit le point sur une base fonction par fonction. Après avoir atteint ce point, l’opération est complètement terminée ou est dans un état tel que les messages d’État indépendants suivants informent l’application de la progression.
-   Les fonctions qui retournent des informations (telles que [**TSPI \_ LinePark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark) ou [**TSPI \_ LINEDEVSPECIFIC**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)) retournent Success uniquement lorsque les informations demandées sont disponibles pour l’appelant. Les fonctions qui retournent des handles (vers des lignes ouvertes, des téléphones ouverts ou des appels) retournent immédiatement les handles lors du retour de la fonction. Le fournisseur de services et l’appelant doivent traiter les handles comme « non encore valides » jusqu’à l’indication de réussite. Il incombe au fournisseur de services d’empêcher tout message de rappel de la procédure [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) ou [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) sur la ligne ouverte, le téléphone ouvert ou d’appeler jusqu’à la fin de l’indication de réussite. Si le résultat final est une erreur, tous les descripteurs retournés immédiatement deviennent non valides sans action supplémentaire.
-   Les fonctions qui activent certaines conditions permanentes (comme [**TSPI \_ lineMonitorDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)) retournent Success uniquement une fois que la condition est activée, et non lorsque la condition est de nouveau supprimée (par exemple, pas lorsque la surveillance digit est terminée).
-   Les fonctions de contrôle d’appel (telles que [**TSPI \_ LineHold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold) et [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer), mais pas [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)) retournent Success lorsque l’opération est terminée. Dans les environnements de téléphonie qui ne fournissent pas d’accusé de réception positif de ces fonctions, le fournisseur de services est contraint de prendre une décision au mieux en ce qui concerne la réussite ou l’échec de la fonction.
-   L’implémentation d’un fournisseur de services de [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) doit retourner Success au plus tard lorsque l’appel passe à l’état d’appel de *procédure* . Dans l’idéal, le fournisseur indique la réussite dès que possible, par exemple lorsque l’appel passe à l’état de l’appel de *tonalité* (le cas échéant). Lorsque la réussite est retournée à l’application, les messages [**\_ CALLSTATE de ligne**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) informent l’appelant sur la progression de l’appel. Les fournisseurs de services qui retardent le renvoi de l’indication de réussite **TSPI \_ lineMakeCall** , par exemple, jusqu’à la fin de la numérotation, limitent sérieusement la flexibilité au niveau de l’application. Un délai de renvoi de la réussite dans **TSPI \_ lineMakeCall** empêche un utilisateur d’annuler la demande d’appel en cours jusqu’à ce que la numérotation soit terminée et que tous les chiffres soient envoyés au commutateur.

 

 
