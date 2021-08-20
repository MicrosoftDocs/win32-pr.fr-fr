---
title: Nouveautés du WER
description: cette page récapitule les nouvelles fonctionnalités de Rapport d’erreurs Windows (WER) pour chaque version.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Windows Rapport d’erreurs Windows des rapports d’erreurs, nouveautés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a15462b38c158dbe323fd355611640102cb1f11ea26e8fef80c593a00cc5152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670630"
---
# <a name="whats-new-in-wer"></a>Nouveautés du WER

cette page récapitule les nouvelles fonctionnalités de Rapport d’erreurs Windows (WER) pour chaque version.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 et Windows Server 2008 R2

la liste suivante récapitule les nouvelles fonctionnalités WER pour Windows 7 et Windows Server 2008 R2.

-   ajoute la possibilité de lever une exception qui ignore tous les gestionnaires d’exceptions, mettant ainsi fin à l’application immédiatement et appelant Rapport d’erreurs Windows. Pour plus d’informations, consultez la fonction [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) .
-   Ajoute la possibilité d’enregistrer un gestionnaire d’exceptions hors processus que le WER appelle lorsqu’un incident se produit pour collecter le nom de l’événement, les paramètres de création de rapports et les options de lancement du débogage. Pour plus d’informations, consultez la fonction [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) .

Fonctions qui ont été ajoutées :

-   [**OutOfProcessExceptionEventCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [**OutOfProcessExceptionEventSignatureCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [**OutOfProcessExceptionEventDebuggerLaunchCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))
-   [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [**WerUnregisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

Structures qui ont été ajoutées :

-   [**\_ \_ informations sur l’exception du runtime wer \_**](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 et Windows Vista SP1

la liste suivante récapitule les nouvelles fonctionnalités de WER pour Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).

-   Le rapport d’erreurs Windows peut être configuré de sorte que les vidages complets en mode utilisateur soient collectés et stockés localement après un incident d’application en mode utilisateur (les applications qui effectuent leurs propres rapports d’incident personnalisés, y compris les applications .NET ne sont pas prises en charge). Pour plus d’informations, consultez [collecte des vidages de User-Mode](collecting-user-mode-dumps.md).

## <a name="windows-vista"></a>Windows Vista

la liste suivante résume les nouvelles fonctionnalités de Rapport d’erreurs Windows (WER) pour Windows Vista :

-   WER a été étendu au-delà de la surveillance des incidents et des processus qui ne répondent pas. WER prend en charge de nombreux nouveaux types d’événements non critiques, tels que les problèmes de performances. Cela permet aux développeurs d’en savoir plus sur les expériences de leurs clients avec les applications qu’ils ont développées.
-   De nouvelles fonctions offrent aux développeurs la flexibilité nécessaire pour créer, personnaliser et soumettre des rapports de problèmes. Pour plus d’informations, consultez [fonctions wer](wer-functions.md).
-   l’amélioration des [Services en ligne de Windows qualité](https://www.microsoft.com/?ref=go) offre aux développeurs un accès aux informations sur les problèmes que les clients envoient pour leurs applications et un mécanisme permettant de fournir des solutions à ces clients.
-   Les fonctions introduites par la récupération de l' [application et](/windows/desktop/Recovery/application-recovery-and-restart-portal) le gestionnaire de redémarrage et de [redémarrage](/windows/desktop/RstMgr/restart-manager-portal) permettent aux applications de récupérer automatiquement les informations et de redémarrer en cas de défaillance critique. Les développeurs peuvent utiliser ces fonctionnalités dans leurs applications pour améliorer de manière significative leur expérience utilisateur.
-   les **rapports et Solutions aux problèmes sur Windows Vista ou le centre de maintenance sur Windows 7** constituent l’emplacement central où les utilisateurs peuvent interagir avec le rapport d’erreurs windows. Les utilisateurs peuvent rechercher de nouvelles solutions, gérer leur historique de création de rapports, afficher les détails d’un rapport de problème et gérer les paramètres de création de rapports, notamment activer le rapport d’erreurs Windows pour rechercher automatiquement des solutions sans interrompre l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rapport d’erreurs Windows](windows-error-reporting.md)
</dt> </dl>

 

 