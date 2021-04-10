---
description: Le parcours de chaîne d’attente (WCT) permet aux débogueurs de diagnostiquer les blocages et les blocages d’application.
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: Wait Chain Traversal
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 842beb7d5470bc2b3e6e9c7c1150ff2aa1a4cf76
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/04/2021
ms.locfileid: "103845662"
---
# <a name="wait-chain-traversal"></a>Wait Chain Traversal

Le parcours de chaîne d’attente (WCT) permet aux débogueurs de diagnostiquer les blocages et les blocages d’application.

Une *chaîne d’attente* est une séquence alternative de threads et d’objets de synchronisation dans laquelle chaque thread attend l’objet qui suit. Chaque objet qui suit est, à son tour, détenu par le thread suivant dans la chaîne.

Un thread attend un objet de synchronisation à partir du moment où le thread demande l’objet jusqu’à ce que le thread l’ait obtenu. Ce « verrou » est détenu par un thread à partir du moment où le thread l’acquiert, jusqu’à ce que le thread le libère. En d’autres termes, lorsque le thread 1 attend un verrou détenu par le thread 2, le thread 1 est en attente de thread 2.

WCT prend en charge les primitives de synchronisation suivantes :

- [Appel de procédure locale avancée (ALPC)](../etw/alpc.md)
- [COM (Component Object Model)](../com/the-component-object-model.md)
- [Sections critiques](../sync/critical-section-objects.md)
- [Mutex](../sync/mutex-objects.md)
- [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage)
- Opérations d' [attente](../sync/wait-functions.md) sur [les processus et les threads](../procthread/processes-and-threads.md)

Pour récupérer la chaîne d’attente pour un ou plusieurs threads, créez une session WCT à l’aide des fonctions [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) et [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) . Les sessions WCT sont représentées par un handle de type **HWCT**.

## <a name="sessions-can-be-synchronous-or-asynchronous"></a>Les sessions peuvent être synchrones ou asynchrones.

Les sessions synchrones ne peuvent pas être annulées et bloquent le thread appelant, jusqu’à ce qu’une chaîne d’attente ait été récupérée.

Les sessions asynchrones ne bloquent pas le thread appelant et peuvent être annulées par l’application à l’aide de la fonction [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) . Les résultats des opérations asynchrones sont rendus disponibles par le biais d’une fonction de rappel [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) fournie par l’application.

Pour les sessions asynchrones, l’appelant peut spécifier un pointeur vers une structure de données de contexte via [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (ce même pointeur est passé à la fonction de rappel [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) ).

La structure des données de contexte est définie par l’utilisateur et opaque à WCT. Il peut être utilisé par l’application pour communiquer le contexte entre une requête WCT et une fonction de rappel. En général, vous transmettez un handle d’événement via cette structure et, lorsque le rappel est exécuté, cet événement est signalé et un thread d’analyse est informé que la requête a été effectuée.

Pour obtenir un exemple de parcours de chaîne d’attente, consultez [utilisation de WCT](using-wct.md) .

## <a name="related-topics"></a>Rubriques connexes

[Utilisation de WCT](using-wct.md), [référence WCT](wct-reference.md), [MSDN Magazine 2007 juillet-Bugslayer : wait chaîne Traversal](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)