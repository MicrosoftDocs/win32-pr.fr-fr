---
title: Annulation d’un appel asynchrone
description: Un client peut annuler un appel asynchrone en cours si l’objet d’appel implémente l’interface ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102424"
---
# <a name="canceling-an-asynchronous-call"></a>Annulation d’un appel asynchrone

Un client peut annuler un appel asynchrone en cours si l’objet d’appel implémente l’interface [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) . Pour les objets qui utilisent le marshaling standard, **ICancelMethodCalls** est toujours disponible pour les appels marshalés. Pour les objets qui utilisent le marshaling personnalisé ou pour les appels aux objets serveur au sein du même cloisonnement, cette fonctionnalité est disponible uniquement si l’objet d’appel implémente **ICancelMethodCalls**.

Le client peut annuler l’appel à tout moment, à partir de lorsque la méthode Begin \_ est appelée jusqu’à ce que la méthode Finish soit \_ retournée. Si le client annule l’appel avant d’appeler la \_ méthode Finish, il doit appeler la \_ méthode Finish pour nettoyer l’état de l’objet d’appel. Tant que le client n’a pas effectué cette opération, tous les appels à toute \_ méthode Begin sur l’objet Call renverront l' \_ appel E RPC E \_ \_ en attente.

**Pour annuler un appel asynchrone**

1.  Interrogez l’objet d’appel pour [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).

2.  Appelez [**ICancelMethodCalls :: Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), puis appelez [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour libérer le pointeur obtenu par l’appel [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) à l’étape 1.

3.  Si le client n’a pas encore appelé la \_ méthode Finish, appelez-le maintenant.

Il n’y a aucune garantie que le serveur n’a pas réellement arrêté l’exécution de l’appel. Si le travail supplémentaire du client dépend de l’état du serveur dont l’appel peut ou non avoir changé, le client doit déterminer cet état avant de continuer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exécution d’un appel asynchrone](making-an-asynchronous-call.md)
</dt> </dl>

 

 