---
description: La nature interactive de la téléphonie nécessite l’utilisation de l’interface TAPI en temps réel.
ms.assetid: b8512588-ec28-4fbe-b47f-b900e2dba1f2
title: Modèle synchrone/asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b3d3b58e9704719e502fa3efc11bc4dc216479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517067"
---
# <a name="synchronousasynchronous-model"></a>Modèle synchrone/asynchrone

La nature interactive de la téléphonie nécessite l’utilisation de l’interface TAPI en temps réel. La plupart des fonctions TAPI sont nécessaires pour se terminer rapidement et retourner leurs résultats à l’application de façon synchrone. D’autres fonctions (telles que la numérotation) peuvent ne pas pouvoir se terminer aussi rapidement et s’exécuter de façon asynchrone.

Les opérations de téléphonie s’effectuent de façon synchrone ou asynchrone. Ces deux modèles diffèrent comme suit. Les *fonctions synchrones* exécutent la requête entière avant que le thread de l’appelant ne soit autorisé à retourner à partir de l’appel de fonction. Les *fonctions asynchrones* retournent avant l’exécution de la requête dans son intégralité. Lorsque la requête asynchrone se termine par la suite, le fournisseur de services signale la fin de l’opération en appelant une procédure de rappel que TAPI a initialement fournie au début de la séquence d’initialisation.

-   Les opérations asynchrones ont un paramètre nommé *dwRequestID* du type défini [DRV \_ REQUESTID](./drv-requestid.md) comme premier paramètre. Une telle opération effectue une partie de son traitement dans l’appel de fonction et le reste de son traitement dans un thread d’exécution indépendant après le retour de l’appel de fonction. Quand la fonction retourne, elle retourne soit un résultat d’erreur négatif, soit le *dwRequestID* (positif) qui a été passé dans l’appel de fonction. Le résultat d’erreur négatif indique que l’opération est terminée (et a échoué). Le *dwRequestID* positif retourné indique que l’opération continue dans le thread indépendant. Dans ce cas, le fournisseur de services appelle finalement la procédure d' [**\_ achèvement asynchrone**](/windows/win32/api/tspi/nc-tspi-async_completion) , en transmettant le *dwRequestID* et un code de résultat pour indiquer le résultat de l’opération. Le code de résultat est zéro en cas de réussite ou un des mêmes jeux de résultats d’erreur (négatifs). Dans tous les cas, le fournisseur de services ne doit jamais retourner zéro ou une valeur positive autre que *dwRequestID* à partir d’une fonction désignée comme asynchrone, car cela peut produire des résultats inattendus. Les fournisseurs de services doivent toujours copier les données d’entrée de la mémoire de l’application dans la mémoire du fournisseur de services avant de retourner une fonction asynchrone.
-   Les opérations synchrones n’ont pas *dwRequestID* comme premier paramètre. Une telle opération effectue tout son traitement dans le thread d’exécution de l’appelant, en retournant le résultat final lorsqu’elle retourne. Le résultat est zéro en cas de réussite ou un code d’erreur négatif pour l’échec. Le fournisseur de services n’appelle pas la [**\_ saisie semi-automatique asynchrone**](/windows/win32/api/tspi/nc-tspi-async_completion) pour les opérations synchrones.

Il est intéressant de prendre en compte la synchronisation d’un rappel « d’achèvement » par rapport au moment où la demande d’origine est retournée. Une requête asynchrone classique serait implémentée par le fournisseur de services, comme dans le pseudocode suivant :

``` syntax
Some_request(Request_ID, ...) {
  check parameters for validity
  check device state for validity
  store Request_ID for Completion Interrupt Handler's use
  manipulate device registers to start physical operation
  return Request_ID  // to indicate asynch operation
}
Operation Completion Interrupt Handler: {
  if operation was successful then
    call "completion" callback passing Request_ID and "success"
  else
    call "completion" callback passing Request_ID and "error num"
  endif
}
```

Si l’opération se termine très rapidement (ou si la demande d’origine retourne très lentement), il est possible que le gestionnaire d’interruptions qui s’exécute lorsqu’une opération physique se termine peut être déclenché avant que la demande d’origine ne retourne à l’application ou même à l’interface TAPI. Ce comportement est autorisé. L’interface TAPI garantit que la notification d’achèvement à l’application est remise après le retour de la requête d’origine.

**TAPI 2. x :** Répertorie l’État selon lequel chaque fonction se termine de façon synchrone ou asynchrone dans une [référence de fonction rapide TAPI](./tapi-quick-function-reference.md).

 

 
