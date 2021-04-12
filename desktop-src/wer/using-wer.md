---
title: Utilisation de WER
description: À compter de Windows Vista, Windows fournit des rapports d’erreurs de panne, de non-réponse et de défaillance du noyau par défaut, sans nécessiter de modifications de votre application.
ms.assetid: c096cd89-e3a7-4959-a35f-40e6168f277e
keywords:
- Rapport d’erreurs Windows Rapport d’erreurs Windows, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655bed6d11757d7d4e08cd00ac47479e1246f96b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104381773"
---
# <a name="using-wer"></a>Utilisation de WER

À compter de Windows Vista, Windows fournit des rapports d’erreurs de panne, de non-réponse et de défaillance du noyau par défaut, sans nécessiter de modifications de votre application. Le rapport inclut des informations sur le Minidump et le vidage du tas, si nécessaire. Les applications utilisent à la place l’API WER pour envoyer des rapports de problèmes spécifiques à l’application à Microsoft.

Étant donné que Windows signale automatiquement les exceptions non gérées, l’application ne doit pas gérer les exceptions irrécupérables. Si le processus de défaillance ou de non-réponse est interactif, WER affiche une interface utilisateur qui informe l’utilisateur du problème. Une application est considérée comme ne répondant pas si elle ne répond pas aux messages Windows pendant cinq secondes alors que l’utilisateur tente d’interagir avec l’application.

## <a name="windows-error-reporting-flow-for-crashes-non-response-and-kernel-faults"></a>Rapport d’erreurs Windows le workflow pour les pannes, les non-réponses et les défaillances du noyau

L’exemple suivant montre les étapes qui se produisent pour un incident d’application, une non-réponse ou une erreur de noyau.

1.  L’événement problème se produit.
2.  Le système d’exploitation appelle le WER.
3.  WER collecte les données, génère un rapport et invite l’utilisateur à donner son consentement (si nécessaire).
4.  WER envoie le rapport à Microsoft (serveur Watson) si l’utilisateur l’a accepté.
5.  Si le serveur Watson demande des données supplémentaires, WER collecte les données et invite l’utilisateur à donner son consentement (si nécessaire).
6.  Si l’application s’est inscrite pour la récupération et le redémarrage, WER exécute les fonctions de rappel enregistrées pendant que les données sont compressées et envoyées à Microsoft (si l’utilisateur l’a accepté).
7.  Si une réponse au problème est disponible auprès de Microsoft, l’utilisateur est averti.

Les applications peuvent utiliser les fonctions suivantes pour personnaliser le contenu du rapport envoyé à Microsoft. Les fonctions d’inscription indiquent à WER d’inclure les fichiers et blocs de mémoire spécifiques dans le rapport d’erreurs qu’il crée.

-   [**WerRegisterFile**](/windows/desktop/api/Werapi/nf-werapi-werregisterfile)
-   [**WerRegisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werregistermemoryblock)
-   [**WerSetFlags**](/windows/desktop/api/Werapi/nf-werapi-wersetflags)
-   [**WerUnregisterFile**](/windows/desktop/api/Werapi/nf-werapi-werunregisterfile)
-   [**WerUnregisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werunregistermemoryblock)
-   [**WerGetFlags**](/windows/desktop/api/Werapi/nf-werapi-wergetflags)

## <a name="windows-error-reporting-flow-for-generic-event-reporting"></a>Rapport d’erreurs Windows le Flow pour les rapports d’événements génériques

Les étapes suivantes montrent comment les applications peuvent obtenir un rapport d’erreurs pour une condition d’erreur récupérable.

1.  L’événement problème non récupérable se produit.
2.  L’application reconnaît l’événement et utilise la séquence suivante d’appels de fonction pour générer le rapport.
    1.  Appelez la fonction [**WerReportCreate**](/windows/desktop/api/Werapi/nf-werapi-werreportcreate) pour créer le rapport.
    2.  Appelez la fonction [**WerReportSetParameter**](/windows/desktop/api/Werapi/nf-werapi-werreportsetparameter) pour définir les paramètres du rapport.
    3.  Appelez la fonction [**WerReportAddFile**](/windows/desktop/api/Werapi/nf-werapi-werreportaddfile) pour ajouter des fichiers au rapport.
    4.  Appelez la fonction [**WerReportAddDump**](/windows/desktop/api/Werapi/nf-werapi-werreportadddump) pour ajouter un minidump au rapport (si nécessaire).
    5.  Appelez la fonction [**WerReportSubmit**](/windows/desktop/api/Werapi/nf-werapi-werreportsubmit) pour envoyer le rapport.
    6.  Appelez [**WerReportCloseHandle**](/windows/desktop/api/Werapi/nf-werapi-werreportclosehandle) pour libérer des ressources.
3.  Selon les options spécifiques utilisées lors de l’appel des fonctions à l’étape 2, WER termine le rapport d’erreurs. Le rapport d’erreurs Windows garantit que la création de rapports est effectuée conformément aux stratégies définies par l’utilisateur. Par exemple, WER envoie le rapport à Microsoft, met le rapport en file d’attente et affiche les interfaces utilisateur appropriées pour l’utilisateur.

## <a name="excluding-an-application-from-windows-error-reporting"></a>Exclusion d’une application de Rapport d’erreurs Windows

Pour exclure votre application du rapport d’erreurs Windows, utilisez la fonction [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication) . Pour restaurer les rapports d’erreurs de votre application, utilisez la fonction [**WerRemoveExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-werremoveexcludedapplication) .

## <a name="automatically-recovering-data-and-restarting-a-faulted-application"></a>Récupération automatique des données et redémarrage d’une application défaillante

Une application peut utiliser la récupération et le redémarrage de l’application pour enregistrer les données et les informations d’État avant la fermeture de l’application en raison d’une exception non gérée ou lorsque l’application cesse de répondre. L’application est également redémarrée, si nécessaire. Pour plus d’informations, consultez [récupération et redémarrage](/windows/desktop/Recovery/application-recovery-and-restart-portal)de l’application.

## <a name="legacy-api"></a>API héritée

Une application peut signaler une erreur en appelant la fonction [**ReportFault**](/windows/desktop/api/ErrorRep/nf-errorrep-reportfault) . Toutefois, vous ne devez pas utiliser la fonction **ReportFault** , sauf si vous avez une exigence très spécifique selon laquelle le comportement de rapport d’erreurs par défaut du système d’exploitation ne peut pas être respecté.

Si le rapport d’erreurs est activé, le système affiche une boîte de dialogue indiquant à l’utilisateur que l’application a rencontré un problème et se ferme. Si un débogueur est configuré dans la clé **HKEY \_ \_ \\ \\ AeDebug CurrentVersion Software Software Microsoft \\ Windows \\ NT \\ CurrentVersion** , l’utilisateur a la possibilité de lancer le débogueur. L’utilisateur a également la possibilité d’envoyer un rapport à Microsoft. Si l’utilisateur envoie le rapport, le système affiche une autre boîte de dialogue en remerciant l’utilisateur pour le rapport et en fournissant un lien vers des informations supplémentaires.

Le système de création de rapports d’erreurs prend en charge les modes d’opération suivants.



| Mode d’opération          | Description                                                                                                                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rapport de mémoire partagée | Si le contexte de sécurité de l’application est le même que le contexte de sécurité de l’utilisateur connecté, le système de création de rapports d’erreurs utilise un bloc de mémoire partagée pour la communication. Ce mode ne peut pas être utilisé avec le mode rapport de manifeste.<br/>                                                                                               |
| Création de rapports de manifeste      | Si le contexte de sécurité de l’application n’est pas le même que le contexte de sécurité de l’utilisateur connecté, le système de création de rapports d’erreurs utilise un fichier pour la communication. Ce mode est également utilisé pour signaler les erreurs de noyau et les applications qui ne répondent pas. Ce mode ne peut pas être utilisé avec le mode de création de rapports de la mémoire partagée.<br/>                      |
| Rapports Internet      | Le système de rapport d’erreurs envoie toutes les données à Microsoft via Internet. Ceci est le mode de fonctionnement par défaut. Elle ne peut pas être utilisée avec le mode de création de rapports d’entreprise. Ce mode est utilisé lorsqu’il n’existe aucun chemin de téléchargement d’entreprise spécifié par l’administrateur.<br/>                                                                     |
| Rapports d’entreprise     | Le système de rapport d’erreurs envoie toutes les données à un partage de fichiers au lieu de les télécharger directement vers Microsoft. Cela permet aux responsables informatiques d’entreprise d’examiner les données avant de les envoyer à Microsoft. Ce mode est utilisé lorsqu’un chemin de téléchargement d’entreprise est spécifié par l’administrateur. Elle ne peut pas être utilisée avec le mode de création de rapports Internet.<br/> |
| Rapports headless      | Le système de rapport d’erreurs n’affiche pas de boîtes de dialogue à l’utilisateur. Cela permet aux responsables informatiques d’entreprise de collecter des rapports d’erreurs à tout moment auprès de leurs employés. Ce mode est utilisé lorsque la création de rapports est activée par l’administrateur, mais la notification est désactivée. Il peut être utilisé uniquement avec le mode de création de rapports d’entreprise.<br/>        |



 

Pour exclure votre application du rapport d’erreurs, utilisez la fonction [**AddERExcludedApplication**](/windows/desktop/api/ErrorRep/nf-errorrep-adderexcludedapplicationa) .

 

