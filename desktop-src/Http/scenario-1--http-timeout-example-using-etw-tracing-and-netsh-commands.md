---
title: Exemple de délai d’expiration HTTP du scénario 1 utilisant le suivi ETW et les commandes netsh
description: Grâce au suivi ETW, le workflow des données via le composant API du serveur HTTP peut être inspecté pour diagnostiquer les problèmes.
ms.assetid: b6b24161-c3da-4972-b49f-c545da2fc81e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bcb9ea328a77641e551f192b7aa89a56dd983251ade8aab45e68251a82458d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870457"
---
# <a name="scenario-1-http-timeout-example-using-etw-tracing-and-netsh-commands"></a>Scénario 1 : exemple de délai d’expiration HTTP utilisant le suivi ETW et les commandes netsh

Grâce au suivi ETW, le workflow des données via le composant API du serveur HTTP peut être inspecté pour diagnostiquer les problèmes. Par exemple, les utilisateurs d’une application Web peuvent voir les messages d’erreur dans leur navigateur qu’une page Web ne peut pas s’afficher. Sur le serveur hébergeant l’application Web, le professionnel de l’informatique voit également une entrée de délai de connexion dans le journal des erreurs HTTP, comme illustré à la figure 1 ci-dessous. Le journal des erreurs HTTP se trouve dans le répertoire suivant :% windir% \\ system32 \\ LogFiles \\ HTTPERR \\ .

![Capture d’écran montrant la fenêtre de commande netsh H T T P affichant un journal des erreurs H T t P pour le délai d’expiration.](images/httperrorlog.png)

Figure 1 : journal des erreurs HTTP pour le délai d’expiration

## <a name="generating-an-etw-trace-report"></a>Génération d’un rapport de suivi ETW

Pour générer un rapport de suivi ETW pour le composant API du serveur HTTP, exécutez les étapes ci-dessous à partir de l’invite de commandes. Dans cet exemple, la trace est exécutée sur le serveur, car elle héberge l’application Web.

Les étapes ci-dessous génèrent une trace appelée Httptrace. etl, puis convertissent la trace en un fichier CSV appelé httptrace.csv. comme indiqué ci-dessous, le fournisseur ETW pour l’API du serveur HTTP est appelé Microsoft-Windows-HttpService. L’option de ligne de commande 0xFFF indique que tous les événements ETW pour ce fournisseur doivent être capturés.

**Générer un rapport de suivi ETW**

1.  démarrer la trace ETW pour le composant de l’API serveur HTTP : l **ogman.exe start httptrace-p Microsoft-Windows-HttpService 0xffff-o httptrace. etl – ets**
2.  Reproduisez le problème afin qu’il puisse être capturé dans la trace. Dans cet exemple, accédez à l’application Web à partir d’un ordinateur client, ce qui entraîne l’affichage du message «**Impossible d’afficher la page**» sur le client.
3.  Maintenant que le problème a été reproduit, arrêtez la trace : **logman.exe Stop Httptrace – ETS**
4.  Convertissez le rapport au format CSV : **tracerpt.exe Httptrace. etl-of CSV-o httptrace.csv**
5.  Affichez le rapport de suivi. Un extrait d’une trace de volume partagé de cluster est présenté ci-dessous dans le tableau 1.

## <a name="viewing-the-trace-and-diagnosing"></a>Affichage du suivi et du diagnostic

le fichier csv résultant pour les traces peut être affiché dans Excel ou tout outil qui prend en charge le format CSV. Le tableau 1 ci-dessous présente des extraits d’un exemple de fichier de trace (httptrace.csv). Dans le rapport de suivi, la colonne « Level » affiche une entrée avec une valeur de « 3 », qui correspond à un avertissement dans ETW. Le composant de l’API du serveur HTTP suit les niveaux ETW définis dans l’article suivant : ( https://msdn2.microsoft.com/library/aa382793.aspx) . Les niveaux ETW sont les suivants :



| Niveau | Signification      |
|-------|--------------|
| 1     | Critique     |
| 2     | Erreur        |
| 3     | Avertissement      |
| 4     | Infomational |
| 5     | Commentaires      |



 

Avec cet avertissement, le type d’événement (colonne de type) indique « ConnTimedOut ». Dans les colonnes suivantes de l’événement ConnTimeOut, le minuteur spécifique qui a expiré est signalé comme « minuteur \_ ConnectionIdle ». Notez que la colonne avec l’entrée « Timer \_ ConnectionIdle » n’est pas incluse dans le tableau pour des raisons de concision et pour éviter l’extrait de colonnes non contiguës.



| Nom d'événement                    | Type            | ID de l’événement | Version | Canal | Niveau |
|-------------------------------|-----------------|----------|---------|---------|-------|
| EventTrace                    | En-tête          | 0        | 2       | 0       | 0     |
| HttpService Microsoft-Windows | ChgUrlGrpProp   | 28       | 0       | 16      | 4     |
| HttpService Microsoft-Windows | AddUrl          | 31       | 0       | 16      | 4     |
| HttpService Microsoft-Windows | ChgReqQueueProp | 30       | 0       | 16      | 4     |
| HttpService Microsoft-Windows | ChgUrlGrpProp   | 28       | 0       | 16      | 4     |
| HttpService Microsoft-Windows | ChgSrvSesProp   | 29       | 0       | 16      | 4     |
| HttpService Microsoft-Windows | ChgSrvSesProp   | 29       | 0       | 16      | 4     |
| HttpService Microsoft-Windows | ConnConnect     | 21       | 0       | 16      | 4     |
| HttpService Microsoft-Windows | ConnIdAssgn     | 22       | 0       | 16      | 4     |
| HttpService Microsoft-Windows | RecvReq         | 1        | 0       | 16      | 4     |
| HttpService Microsoft-Windows | Analyser           | 2        | 0       | 16      | 4     |
| HttpService Microsoft-Windows | LogFileWrite    | 51       | 0       | 16      | 4     |
| HttpService Microsoft-Windows | ConnCleanup     | 24       | 0       | 16      | 4     |
| HttpService Microsoft-Windows | ConnTimedOut    | 53       | 0       | 16      | 3     |



 

Tableau 1 : extraits d’un exemple de rapport de suivi pour un problème de minuteur

Dans cet exemple, l’expiration (événement ConnTimeOut) du minuteur d’en-tête (Timer \_ ConnectionIdle) est la raison pour laquelle les utilisateurs finaux voient le message « Impossible d’afficher la page » dans leurs clients Web. Une raison possible du délai d’attente peut être que les clients Web s’envoient lentement en raison de connexions lentes. Pour résoudre ce problème, la valeur du délai d’attente peut être ajustée par le biais des commandes netsh.

## <a name="adjusting-timeout-through-netsh-and-verifying-the-solution"></a>Ajustement du délai d’expiration via netsh et vérification de la solution

Les commandes netsh pour HTTP listées ci-dessous permettent à un professionnel de l’informatique d’afficher et de configurer des valeurs de paramètres sur le composant de l’API du serveur HTTP. Les modifications effectuées via les commandes netsh HTTP affectent toutes les applications serveur hébergées par le composant API du serveur HTTP pour cet ordinateur. Ces modifications sont conservées entre les redémarrages du composant et les redémarrages de la machine. les commandes Netsh HTTP sont disponibles dans Windows vista et Windows Server 2008 et remplacent le HttpCfg.exe outil du Kit de ressources de Windows Server 2003 lorsqu’ils sont exécutés sur Windows Vista et Windows Server 2008. Dans ce scénario, nous allons ajuster une valeur de délai d’attente, puis vérifier la solution. Les minuteurs existent dans le composant de l’API du serveur HTTP pour garantir la disponibilité et la protection contre la surconsommation par un utilisateur mal configuré ou malveillant. L’ajustement des minuteurs à partir des valeurs par défaut doit être soigneusement évalué par rapport à une attaque par déni de refus.

Dans cet exemple, les clients Web se trouvent derrière une connexion réseau lente, entraînant l' \_ événement ETW ConnectionIdle du minuteur. Après avoir pris en compte la cause des délais d’attente et l’équilibrage avec l’impact sur la charge du serveur, il est décidé d’augmenter les valeurs de délai d’attente à une valeur de 240 secondes. Vous pouvez afficher et configurer le minuteur à l’aide de la procédure suivante.

**Configurer le minuteur de connexion inactive (minuteur \_ ConnectionIdle) avec netsh**

1.  Sur le serveur, ouvrez une fenêtre de commande avec élévation de privilèges et exécutez les étapes ci-dessous pour afficher et configurer la valeur du délai d’attente. Une capture d’écran de la commande netsh HTTP est illustrée dans la figure 2 ci-dessous.
2.  Afficher les valeurs de délai d’attente actuelles : **netsh http show Timeout**
3.  Configurez la \_ valeur du délai d’attente ConnectionIdle du minuteur. Dans cet exemple, la valeur est remplacée par 240 secondes : **netsh http Add Timeout timeouttype = idleconnectiontimeout, value = 240**

![fenêtre commande netsh http](images/netshhttpcommand.png)

Figure 2 : fenêtre de commande netsh HTTP

Après avoir configuré la valeur du délai d’attente, réexécutez les étapes de diagnostic ETW. Si la condition d’erreur est corrigée, la trace ETW ne doit plus afficher de délai d’expiration avec un niveau ETW de « 3 » pour le minuteur d’inactivité de la connexion.

 

 




