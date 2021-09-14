---
title: Gestion des transactions (Exchange de données)
description: Cette rubrique explique comment un client peut envoyer des transactions pour obtenir des données et des services à partir du serveur.
ms.assetid: 2d08ffa3-cbd7-4806-b94f-979938322c38
keywords:
- Windows Interface utilisateur, échange dynamique de données (DDE)
- échange dynamique de données (DDE), transactions
- DDE (échange dynamique de données), transactions
- échange de données, échange dynamique de données (DDE)
- Windows Interface utilisateur, échange dynamique de données Management Library (DDEML)
- bibliothèque de gestion des échange dynamique de données (DDEML), transactions
- DDEML (bibliothèque de gestion échange dynamique de données), transactions
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
- échange dynamique de données (DDE), demandes de transactions
- DDE (échange dynamique de données), demandes de transactions
- bibliothèque de gestion des échange dynamique de données (DDEML), demandes de transactions
- DDEML (bibliothèque de gestion échange dynamique de données), demandes de transactions
- échange dynamique de données (DDE), écritures en avant
- DDE (échange dynamique de données), écritures en avant
- bibliothèque de gestion des échange dynamique de données (DDEML), transactions d’en-in
- DDEML (bibliothèque de gestion échange dynamique de données), écritures de l’en-in
- échange dynamique de données (DDE), notification des transactions
- DDE (échange dynamique de données), notification des transactions
- bibliothèque de gestion des échange dynamique de données (DDEML), notification des transactions
- DDEML (bibliothèque de gestion échange dynamique de données), notification des transactions
- échange dynamique de données (DDE), exécuter des transactions
- DDE (échange dynamique de données), exécuter des transactions
- bibliothèque de gestion des échange dynamique de données (DDEML), exécution des transactions
- DDEML (bibliothèque de gestion échange dynamique de données), exécuter des transactions
- échange dynamique de données (DDE), transactions synchrones
- DDE (échange dynamique de données), transactions synchrones
- bibliothèque de gestion des échange dynamique de données (DDEML), transactions synchrones
- DDEML (bibliothèque de gestion échange dynamique de données), transactions synchrones
- échange dynamique de données (DDE), transactions asynchrones
- échanges de transactions asynchrones (échange dynamique de données)
- bibliothèque de gestion des échange dynamique de données (DDEML), transactions asynchrones
- DDEML (bibliothèque de gestion échange dynamique de données), transactions asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570aa48b4dcdbb31855b3e1b15a091908feb2ba4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008170"
---
# <a name="transaction-management-data-exchange"></a>Gestion des transactions (Exchange de données)

Après avoir établi une conversation avec un serveur, un client peut envoyer des transactions pour obtenir des données et des services à partir du serveur.

Les rubriques suivantes décrivent les types de transactions que les clients peuvent utiliser pour interagir avec un serveur.

-   [Transaction de demande](#request-transaction)
-   [Transaction de journalisation](#poke-transaction)
-   [Transaction de notification](#advise-transaction)
-   [Exécuter la transaction](#execute-transaction)
-   [Transactions synchrones et asynchrones](#synchronous-and-asynchronous-transactions)
-   [Contrôle de transaction](#transaction-control)
-   [Classes de transaction](#transaction-classes)
-   [Types de transactions](#transaction-types)

## <a name="request-transaction"></a>Transaction de demande

Une application cliente peut utiliser la transaction de [**\_ demande XTYP**](xtyp-request.md) pour demander un élément de données à partir d’une application serveur. Le client appelle la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) , en spécifiant la **\_ demande XTYP** comme type de transaction et en spécifiant l’élément de données dont l’application a besoin.

la bibliothèque de gestion des échange dynamique de données (DDEML) transmet la transaction de [**\_ demande XTYP**](xtyp-request.md) au serveur, en spécifiant le nom de la rubrique, le nom de l’élément et le format de données demandés par le client. Si le serveur prend en charge la rubrique, l’élément et le format demandés, le serveur doit retourner un handle de données qui identifie la valeur actuelle de l’élément. Le DDEML transmet ce handle au client en tant que valeur de retour de [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Le serveur doit retourner la **valeur null** s’il ne prend pas en charge la rubrique, l’élément ou le format demandé.

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) utilise le paramètre *lpdwResult* pour retourner un indicateur d’état de transaction au client. Si le serveur ne traite pas la transaction de [**\_ demande XTYP**](xtyp-request.md) , **DdeClientTransaction** retourne la **valeur null** et *LPDWRESULT* pointe vers l' \_ indicateur DDE FNOTPROCESSED ou DDE \_ FBUSY. Si l' \_ indicateur DDE FNOTPROCESSED est retourné, le client ne peut pas déterminer la raison pour laquelle le serveur n’a pas traité la transaction.

Si un serveur ne prend pas en charge la transaction de [**\_ demande XTYP**](xtyp-request.md) , il doit spécifier l' \_ \_ indicateur de filtre de demandes CBF Fail dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Cet indicateur empêche DDEML d’envoyer la transaction au serveur.

## <a name="poke-transaction"></a>Transaction de journalisation

Un client peut envoyer des données non sollicitées à un serveur à l’aide de [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) pour envoyer une transaction d’ajout de [**XTYP \_**](xtyp-poke.md) à la fonction de rappel d’un serveur.

L’application cliente crée d’abord une mémoire tampon qui contient les données à envoyer au serveur, puis passe un pointeur vers la mémoire tampon en tant que paramètre de [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Le client peut également utiliser la fonction [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) pour obtenir un handle de données qui identifie les données, puis passer le descripteur à **DdeClientTransaction**. Dans les deux cas, le client spécifie également le nom de la rubrique, le nom de l’élément et le format de données lorsqu’il appelle **DdeClientTransaction**.

DDEML transmet la transaction d’extension [**XTYP \_**](xtyp-poke.md) au serveur, en spécifiant le nom de la rubrique, le nom de l’élément et le format de données que le client a demandé. Pour accepter l’élément et le format de données, le serveur doit retourner des \_ Fack DDE. Pour refuser les données, le serveur doit retourner des \_ FNOTPROCESSED DDE. Si le serveur est trop occupé pour accepter les données, le serveur doit renvoyer des \_ FBUSY DDE.

Quand [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) retourne, le client peut utiliser le paramètre *lpdwResult* pour accéder à l’indicateur d’état de transaction. Si l’indicateur est \_ FBUSY DDE, le client doit renvoyer la transaction ultérieurement.

Si un serveur ne prend pas en [**charge \_ la transaction XTYP**](xtyp-poke.md) , il doit spécifier l' \_ \_ indicateur de filtre d’échec de CBF dans [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Cet indicateur empêche DDEML d’envoyer cette transaction au serveur.

## <a name="advise-transaction"></a>Transaction de notification

Une application cliente peut utiliser DDEML pour établir un ou plusieurs liens vers les éléments d’une application serveur. Lorsqu’un tel lien a été établi, le serveur envoie des mises à jour périodiques sur l’élément lié au client (en général, chaque fois que la valeur de l’élément associé à l’application serveur est modifiée). La liaison établit une boucle de notification entre les deux applications qui reste en place jusqu’à ce que le client le termine.

Il existe deux types de boucles de notification : « chaude » et « chaude ». Dans une boucle de notification à chaud, le serveur envoie immédiatement un handle de données qui identifie la valeur modifiée. Dans une boucle de notification à chaud, le serveur notifie le client que la valeur de l’élément a changé, mais n’envoie pas le descripteur de données tant que le client ne l’a pas demandé.

Un client peut demander une boucle de notification à chaud avec un serveur en spécifiant le type de transaction [**XTYP \_ ADVSTART**](xtyp-advstart.md) dans un appel à [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Pour demander une boucle de notification à chaud, le client doit combiner l' \_ indicateur NoData XTYPF avec le type de transaction **XTYP \_ ADVSTART** . dans les deux cas, DDEML transmet la transaction **XTYP \_ ADVSTART** à la fonction de rappel échange dynamique de données (DDE) du serveur. La fonction de rappel DDE du serveur doit examiner les paramètres qui accompagnent la transaction **XTYP \_ ADVSTART** (y compris le format demandé, le nom de la rubrique et le nom de l’élément), puis retourne **true** pour autoriser la boucle Advise ou **false** à la refuser.

Après l’établissement d’une boucle de notification, l’application serveur doit appeler la fonction [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) chaque fois que la valeur de l’élément associé au nom de l’élément demandé change. Cet appel entraîne l’envoi d’une transaction [**XTYP \_ ADVREQ**](xtyp-advreq.md) à la fonction de rappel DDE du serveur. La fonction de rappel DDE du serveur doit retourner un handle de données qui identifie la nouvelle valeur de l’élément de données. Le DDEML informe ensuite le client que l’élément spécifié a changé en envoyant la transaction [**XTYP \_ ADVDATA**](xtyp-advdata.md) à la fonction de rappel DDE du client.

Si le client a demandé une boucle de notification à chaud, le DDEML transmet le descripteur de données à l’élément modifié au client au cours de la transaction [**\_ ADVDATA XTYP**](xtyp-advdata.md) . Dans le cas contraire, le client peut envoyer une transaction de [**\_ demande XTYP**](xtyp-request.md) pour obtenir le descripteur de données.

Il est possible pour un serveur d’envoyer des mises à jour plus rapidement qu’un client ne peut traiter les nouvelles données. La vitesse des mises à jour peut être un problème pour un client qui doit effectuer des opérations de traitement longues sur les données. Dans ce cas, le client doit spécifier l' \_ indicateur XTYPF ACKREQ lorsqu’il demande une boucle de notification. Cet indicateur force le serveur à attendre que le client confirme qu’il a reçu et traité un élément de données avant que le serveur n’envoie l’élément de données suivant. Les boucles de notification établies avec l' \_ indicateur XTYPF ACKREQ sont plus robustes avec les serveurs rapides, mais peuvent parfois manquer de mises à jour. Les boucles de notification établies sans l' \_ indicateur XTYPF ACKREQ sont assurées de ne pas manquer les mises à jour tant que le client continue de s’exécuter sur le serveur.

Un client peut terminer une boucle de notification en spécifiant le type de transaction [**XTYP \_ ADVSTOP**](xtyp-advstop.md) dans un appel à [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).

Si un serveur ne prend pas en charge les boucles de notification, il doit spécifier l' \_ \_ indicateur de filtre de notifications d’échec CBF dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Cet indicateur empêche DDEML d’envoyer les transactions [**XTYP \_ ADVSTART**](xtyp-advstart.md) et [**XTYP \_ ADVSTOP**](xtyp-advstop.md) au serveur.

## <a name="execute-transaction"></a>Exécuter la transaction

Un client peut utiliser la transaction d' [**\_ exécution XTYP**](xtyp-execute.md) pour faire en sorte qu’un serveur exécute une commande ou une série de commandes.

Pour exécuter une commande de serveur, le client crée d’abord une mémoire tampon qui contient une chaîne de commande que le serveur doit exécuter, puis passe un pointeur vers la mémoire tampon ou un handle de données qui identifie la mémoire tampon lorsqu’elle appelle [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Les autres paramètres requis incluent le descripteur de conversation, le descripteur de chaîne de nom d’élément, la spécification de format et le type de transaction d' [**\_ exécution XTYP**](xtyp-execute.md) . Une application qui crée un descripteur de données pour transmettre des données d’exécution doit spécifier **null** pour le paramètre *hszItem* de la fonction [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) et zéro pour le paramètre *uFmt* .

DDEML transmet la transaction [**d' \_ exécution XTYP**](xtyp-execute.md) à la fonction de rappel DDE du serveur et spécifie le nom de format, le descripteur de conversation, le nom de la rubrique et le descripteur de données identifiant la chaîne de commande. Si le serveur prend en charge la commande, il doit utiliser la fonction [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) pour obtenir un pointeur vers la chaîne de commande, exécuter la commande, puis retourner des \_ Fack DDE. Si le serveur ne prend pas en charge la commande ou ne peut pas exécuter la transaction, il doit renvoyer des \_ FNOTPROCESSED DDE. Le serveur doit retourner le \_ FBUSY DDE s’il est trop occupé pour terminer la transaction.

En général, la fonction de rappel d’un serveur doit traiter la transaction d' [**\_ exécution XTYP**](xtyp-execute.md) avant de retourner avec les exceptions suivantes :

1.  Lorsque la commande transmise avec [**XTYP \_ Execute**](xtyp-execute.md) transaction demande au serveur de se terminer, le serveur ne doit pas se terminer tant que sa fonction de rappel n’est pas retournée du traitement de l' **\_ exécution de XTYP**.
2.  Si le serveur doit effectuer une opération, telle que le traitement d’une boîte de dialogue ou d’une transaction DDE qui peut provoquer des problèmes de récurrence de DDEML, le serveur doit retourner le \_ Code de retour du bloc CBR pour bloquer l’exécution de la transaction, effectuer l’opération, puis reprendre le traitement de la transaction d’exécution.

Quand [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) retourne, le client peut utiliser le paramètre *lpdwResult* pour accéder à l’indicateur d’état de la transaction. Si l’indicateur est \_ FBUSY DDE, le client doit renvoyer la transaction ultérieurement.

Si un serveur ne prend pas en charge la transaction d' [**\_ exécution XTYP**](xtyp-execute.md) , il doit spécifier l' \_ \_ indicateur de filtre CBF Fail executes dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Cela empêche le DDEML d’envoyer la transaction au serveur.

## <a name="synchronous-and-asynchronous-transactions"></a>Transactions synchrones et asynchrones

Un client peut envoyer des transactions synchrones ou asynchrones. Dans une transaction synchrone, le client spécifie une valeur de délai d’attente qui indique la durée maximale pendant laquelle il attend que le serveur traite la transaction. [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) ne retourne pas de valeur tant que le serveur n’a pas traité la transaction, que la transaction échoue ou que la valeur de délai d’attente expire. Le client spécifie la valeur du délai d’attente lors de l’appel de **DdeClientTransaction**.

Pendant une transaction synchrone, le client entre une boucle modale en attendant que la transaction soit traitée. Le client peut toujours traiter l’entrée d’utilisateur, mais ne peut pas envoyer une autre transaction synchrone tant que [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) n’est pas retourné.

Un client envoie une transaction asynchrone en spécifiant l' \_ indicateur Async Timeout dans [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). La fonction retourne une fois que la transaction a commencé, en passant un identificateur de transaction au client. Une fois que le serveur a terminé le traitement de la transaction asynchrone, DDEML envoie une transaction [**XTYP \_ XACT \_ Complete**](xtyp-xact-complete.md) au client. L’un des paramètres que le DDEML transmet au client pendant la transaction **XTYP \_ XACT \_ Complete** est l’identificateur de la transaction. En comparant cet identificateur de transaction avec l’identificateur retourné par **DdeClientTransaction**, le client identifie la transaction asynchrone que le serveur a terminé de traiter.

Un client peut utiliser la fonction [**DdeSetUserHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle) comme aide pour le traitement d’une transaction asynchrone. Cette fonction permet à un client d’associer une valeur définie par l’application à un descripteur de conversation et à un identificateur de transaction. Le client peut utiliser la fonction [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) pendant la transaction [**XTYP \_ XACT \_ Complete**](xtyp-xact-complete.md) pour obtenir la valeur définie par l’application. En raison de cette fonction, une application n’a pas besoin de conserver une liste d’identificateurs de transaction actifs.

Lorsqu’un client effectue avec succès une demande de données à l’aide d’une transaction synchrone, le DDEML n’a aucun moyen de savoir à quel moment le client a terminé d’utiliser les données reçues. L’application cliente doit passer le descripteur de données reçu à la fonction [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) , en notifiant au Ddeml que le descripteur ne sera plus utilisé. Les handles de données retournés par les transactions synchrones sont détenus par le client.

Si un serveur ne traite pas une transaction asynchrone en temps opportun, le client peut abandonner la transaction en appelant la fonction [**DdeAbandonTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction) . Le DDEML libère toutes les ressources associées à la transaction et ignore les résultats de la transaction lorsque le serveur termine le traitement. Un délai d’attente pendant une transaction synchrone annule effectivement la transaction.

La méthode de transaction asynchrone est fournie pour les applications qui doivent envoyer un volume élevé de transactions DDE tout en effectuant simultanément une quantité importante de traitement, par exemple en effectuant des calculs. La méthode asynchrone est également utile dans les applications qui doivent cesser de traiter temporairement les transactions DDE afin de pouvoir effectuer d’autres tâches sans interruption. Dans la plupart des autres cas, une application doit utiliser la méthode synchrone.

Les transactions synchrones sont plus simples à gérer et sont plus rapides que les transactions asynchrones. Toutefois, une seule transaction synchrone peut être exécutée à la fois, tandis que de nombreuses transactions asynchrones peuvent être exécutées simultanément. Avec les transactions synchrones, un serveur lent peut faire en sorte qu’un client reste inactif pendant qu’il attend une réponse. En outre, les transactions synchrones font en sorte que le client entre dans une boucle modale qui peut contourner le filtrage des messages dans la propre boucle de message de l’application.

Si le client a installé une procédure de Hook pour filtrer les messages (c’est-à-dire, spécifié le \_ type de hook BL msgfilter dans un appel à la fonction [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) ), une transaction synchrone n’entraîne pas le contournement de la procédure de hook par le système. Lorsqu’un événement d’entrée se produit pendant que le client attend la fin d’une transaction synchrone, la procédure de raccordement reçoit un \_ Code de hook MSGF DDEMGR. Le danger principal de l’utilisation d’une boucle modale de transaction synchrone est qu’une boucle modale créée par une boîte de dialogue peut interférer avec son fonctionnement. Les transactions asynchrones doivent toujours être utilisées lorsque le DDEML est utilisé par une DLL.

## <a name="transaction-control"></a>Contrôle de transaction

Une application peut suspendre des transactions à sa fonction de rappel DDE soit ces transactions associées à un descripteur de conversation spécifique, soit toutes les transactions, quel que soit le descripteur de conversation. Cette fonctionnalité est utile quand une application reçoit une transaction qui nécessite un traitement long. Dans ce cas, l’application peut renvoyer le \_ Code de retour de bloc CBR pour suspendre les futures transactions associées au descripteur de conversation de la transaction, afin que l’application soit libre de traiter d’autres conversations.

Une fois le traitement terminé, l’application appelle la fonction [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) pour reprendre les transactions associées à la conversation suspendue. L’appel de **DdeEnableCallback** amène le Ddeml à renvoyer la transaction qui a entraîné la suspension de la conversation par l’application. Par conséquent, l’application doit stocker le résultat de la transaction de manière à ce qu’elle puisse obtenir et retourner le résultat sans retraiter la transaction.

Une application peut suspendre toutes les transactions associées à un handle de conversation spécifique en spécifiant le descripteur et l' \_ indicateur EC Disable dans un appel à [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback). En spécifiant un descripteur **null** , une application peut suspendre toutes les transactions pour toutes les conversations.

Lorsqu’une conversation a été interrompue, DDEML enregistre les transactions de la conversation dans une file d’attente de transactions. Lorsque l’application réactive la conversation, DDEML supprime les transactions enregistrées de la file d’attente et transmet chaque transaction à la fonction de rappel appropriée. La capacité de la file d’attente des transactions est importante, mais une application doit réactiver une conversation suspendue dès que possible pour éviter de perdre des transactions.

Une application peut reprendre le traitement de transactions habituel en spécifiant l' \_ indicateur EC ENABLEALL dans [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback). Pour une reprise plus contrôlée du traitement des transactions, l’application peut spécifier l' \_ indicateur EC ENABLEONE. Cet indicateur supprime une transaction de la file d’attente des transactions et la transmet à la fonction de rappel appropriée. une fois cette transaction traitée, toutes les conversations sont à nouveau désactivées.

Si l' \_ indicateur EC ENABLEONE et un descripteur de conversation sont spécifiés dans l’appel à [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback), seule cette conversation est bloquée après le traitement de la transaction. Si un descripteur de conversation **null** est spécifié, toutes les conversations sont bloquées après le traitement d’une transaction dans une conversation.

## <a name="transaction-classes"></a>Classes de transaction

DDEML possède quatre classes de transactions. Chaque classe est identifiée par une constante qui commence par le \_ préfixe XCLASS. Les classes sont définies dans le fichier d’en-tête DDEML. La valeur de classe est associée à la valeur de type de transaction et est transmise à la fonction de rappel DDE de l’application réceptrice.

La classe d’une transaction détermine la valeur de retour qu’une fonction de rappel est supposée retourner si elle traite la transaction. Les valeurs de retour et les types de transactions suivants sont associés à chacune des quatre classes de transaction.



| Classe                | Valeur de retour                                                     | Transaction                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| XCLASS \_ bool         | **True** ou **false**                                            | [**XTYP \_ ADVSTART**](xtyp-advstart.md)<br/> [**XTYP \_ Connect**](xtyp-connect.md)<br/>                                                                                                                                                                                                                                                                                            |
| \_données XCLASS         | Un descripteur de données, le \_ Code de retour de bloc CBR ou **null**           | [**XTYP \_ ADVREQ**](xtyp-advreq.md)<br/> [**\_demande XTYP**](xtyp-request.md)<br/> [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)<br/>                                                                                                                                                                                                                                       |
| \_indicateurs XCLASS        | Indicateur de transaction : DDE \_ Fack, DDE \_ FBUSY ou DDE \_ FNOTPROCESSED | [**XTYP \_ ADVDATA**](xtyp-advdata.md)<br/> [**exécution de XTYP \_**](xtyp-execute.md)<br/> [**XTYP \_**](xtyp-poke.md)<br/>                                                                                                                                                                                                                                                   |
| \_notification XCLASS | None                                                             | [**XTYP \_ ADVSTOP**](xtyp-advstop.md)<br/> [**confirmer la XTYP \_ Connect \_**](xtyp-connect-confirm.md)<br/> [**déconnexion XTYP \_**](xtyp-disconnect.md)<br/> [**\_erreur XTYP**](xtyp-error.md)<br/> [**\_Registre XTYP**](xtyp-register.md)<br/> [**\_désinscription XTYP**](xtyp-unregister.md)<br/> [**XTYP \_ XACT \_ terminé**](xtyp-xact-complete.md)<br/> |



 

## <a name="transaction-types"></a>Types de transactions

Chaque type de transaction DDE a un récepteur et une activité associée qui entraîne la génération par le DDEML de chaque type.



| Type de transaction                                       | Destinataire                   | Cause                                                                                                                                                                         |
|--------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XTYP \_ ADVDATA**](xtyp-advdata.md)                  | Client                     | Un serveur a répondu à une [**transaction \_ ADVREQ XTYP**](xtyp-advreq.md) en renvoyant un descripteur de données.                                                                          |
| [**XTYP \_ ADVREQ**](xtyp-advreq.md)                    | Serveur                     | Un serveur a appelé la fonction [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) , indiquant que la valeur d’un élément de données dans une boucle de notification a changé.                                  |
| [**XTYP \_ ADVSTART**](xtyp-advstart.md)                | Serveur                     | Un client a spécifié le type de transaction [**XTYP \_ ADVSTART**](xtyp-advstart.md) dans un appel à la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .               |
| [**XTYP \_ ADVSTOP**](xtyp-advstop.md)                  | Serveur                     | Un client a spécifié le type de transaction [**XTYP \_ ADVSTOP**](xtyp-advstop.md) dans un appel à [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**XTYP \_ Connect**](xtyp-connect.md)                  | Serveur                     | Un client a appelé la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) et a spécifié un nom de service et un nom de rubrique pris en charge par le serveur.                                            |
| [**confirmer la XTYP \_ Connect \_**](xtyp-connect-confirm.md) | Serveur                     | Le serveur a retourné la **valeur true** en réponse à une transaction [**XTYP \_ Connect**](xtyp-connect.md) ou [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) .                            |
| [**déconnexion XTYP \_**](xtyp-disconnect.md)            | Client/serveur              | Un partenaire dans une conversation a appelé la fonction [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) , ce qui A pour effet que les deux partenaires reçoivent cette transaction.                                    |
| [**\_erreur XTYP**](xtyp-error.md)                      | Client/serveur              | Une erreur critique s’est produite. Le DDEML peut ne pas disposer de ressources suffisantes pour continuer.                                                                                       |
| [**exécution de XTYP \_**](xtyp-execute.md)                  | Serveur                     | Un client a spécifié le type de transaction [**XTYP \_ Execute**](xtyp-execute.md) dans un appel à [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**\_moniteur XTYP**](xtyp-monitor.md)                  | Application de surveillance DDE | Un événement DDE s’est produit dans le système. Pour plus d’informations sur les applications d’analyse DDE, consultez [surveillance des applications](monitoring-applications.md).                       |
| [**XTYP \_**](xtyp-poke.md)                        | Serveur                     | Un client a spécifié le type de transaction [**XTYPs \_**](xtyp-poke.md) dans un appel à [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                                    |
| [**\_Registre XTYP**](xtyp-register.md)                | Client/serveur              | Une application serveur a utilisé la fonction [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour enregistrer un nom de service.                                                                   |
| [**\_demande XTYP**](xtyp-request.md)                  | Serveur                     | Un client a spécifié le type de transaction [**XTYP \_ Request**](xtyp-request.md) dans un appel à [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**\_désinscription XTYP**](xtyp-unregister.md)            | Client/serveur              | Une application serveur a utilisé [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour annuler l’inscription d’un nom de service.                                                                              |
| [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)          | Serveur                     | Un client A appelé la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) ou [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) , en spécifiant la **valeur null** pour le nom du service, le nom de la rubrique, ou les deux. |
| [**XTYP \_ XACT \_ terminé**](xtyp-xact-complete.md)     | Client                     | Une transaction asynchrone, envoyée lorsque le client a spécifié l' \_ indicateur Timeout Async dans un appel à [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction), s’est terminée.         |



 

 

