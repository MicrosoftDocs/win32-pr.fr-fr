---
title: Génération des informations d’erreur
description: Si un serveur ou une application rencontre une erreur irrécupérable lors de son appel via RPC, elle doit indiquer à l’exécution RPC qu’elle a rencontré un échec, et idéalement, doit ajouter des informations sur l’échec pour faciliter le dépannage.
ms.assetid: 6658c387-94df-4d85-9749-53858f9e0f5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b06a13e932034e6840479443e0b78f4c322c0b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229163"
---
# <a name="generating-error-information"></a>Génération des informations d’erreur

Si un serveur ou une application rencontre une erreur irrécupérable lors de son appel via RPC, elle doit indiquer à l’exécution RPC qu’elle a rencontré un échec, et idéalement, doit ajouter des informations sur l’échec pour faciliter le dépannage.

## <a name="indicating-fatal-errors-to-the-rpc-run-time"></a>Indication des erreurs irrécupérables au moment de l’exécution RPC

Pour indiquer un échec au moment de l’exécution RPC, appelez la fonction [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) sur le thread RPC sur lequel l’exception a été appelée, ou [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) si le traitement de l’appel est asynchrone sur un autre thread. Le renvoi d’un code d’erreur à partir de la routine du serveur, tel que la routine du gestionnaire, n’est pas suffisant, conformément à la spécification RPC, la valeur de retour de la fonction n’a aucune sémantique d’erreur sur le serveur, quels que soient les paramètres de fichier IDL/ACF.

Lorsqu’une erreur irrécupérable se produit dans votre composant, effectuez tout nettoyage jugé nécessaire, puis appelez la fonction [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) avec le code d’erreur. La seule différence entre **RpcRaiseException** et le renvoi d’un code d’erreur est lorsque le **RpcRaiseException** est appelé, les paramètres out ne sont pas marshalés. C’est généralement un avantage, puisque l’évitement des paramètres non initialisés n’est pas nécessaire.

## <a name="generating-additional-extended-error-information"></a>Génération d’informations d’erreur étendues supplémentaires

Tout comme l’exécution RPC génère une chaîne d’enregistrements d’erreur, votre serveur ou votre application peut ajouter ses propres enregistrements à la chaîne. Cette approche est souvent utile dans le processus de résolution des problèmes. Par exemple, un serveur peut tenter d’ouvrir un fichier donné et de recevoir une erreur fichier introuvable. Il n’est pas utile de renvoyer simplement l’erreur 2 pour déterminer quel fichier est manquant.

Au lieu de cela, votre serveur peut appeler la fonction [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) et fournir un paramètre de chaîne, ANSI ou Unicode, dans l’enregistrement d’erreur indiquant le chemin d’accès complet au fichier qu’il recherchait. Lorsque toutes ces informations s’affichent sur l’écran de l’utilisateur sur un ordinateur distant, le dépannage devient trivial. une vérification simple de l’existence du fichier peut être effectuée, en particulier dans la mesure où le nom de l’ordinateur en question est déjà fourni par l’exécution RPC.

L’appel de fonction [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) peut échouer si la mémoire disponible n’est pas suffisante, même s’il ne nécessite que quelques octets d’espace de tas. En outre, les enregistrements ajoutés par **RpcErrorAddRecord** s’accumulent dans un thread donné. Le runtime nettoie normalement ces enregistrements avant d’appeler votre routine de serveur. Toutefois, si des informations d’erreur étendues sont utilisées en dehors de RPC, effectuez le nettoyage de l’erreur étendue accumulée dans le thread en appelant [**RpcErrorClearInformation**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation).

 

 




