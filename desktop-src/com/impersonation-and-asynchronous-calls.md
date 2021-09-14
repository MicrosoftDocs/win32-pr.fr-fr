---
title: Emprunt d’identité et appels asynchrones
description: Emprunt d’identité et appels asynchrones
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998912"
---
# <a name="impersonation-and-asynchronous-calls"></a>Emprunt d’identité et appels asynchrones

Le serveur ne peut pas emprunter l’identité du client après l’appel du serveur à [**ISynchronize :: signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) , même si la méthode Begin n' \_ est pas encore terminée. Par exemple, supposons qu’un client appelle la méthode Begin, que le \_ serveur traite l’appel immédiatement et que le serveur appelle **signal** pour indiquer qu’il a terminé le traitement. Même si le travail reste à effectuer dans la \_ méthode Begin, le serveur ne peut pas emprunter l’identité du client une fois l’appel à **signal** terminé.

Si le serveur emprunte l’identité du client avant d’appeler [**signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), le jeton d’emprunt d’identité n’est pas supprimé du thread tant que le serveur n’a pas appelé [**IServerSecurity :: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) ou jusqu’à ce que l’appel du serveur de commence, selon ce qui se produit en \_ premier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Délégation et emprunt d’identité](delegation-and-impersonation.md)
</dt> <dt>

[Exécution d’un appel asynchrone](making-an-asynchronous-call.md)
</dt> </dl>

 

 