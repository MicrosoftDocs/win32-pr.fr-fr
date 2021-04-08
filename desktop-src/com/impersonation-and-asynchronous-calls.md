---
title: Emprunt d’identité et appels asynchrones
description: Emprunt d’identité et appels asynchrones
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730677"
---
# <a name="impersonation-and-asynchronous-calls"></a><span data-ttu-id="49d1e-103">Emprunt d’identité et appels asynchrones</span><span class="sxs-lookup"><span data-stu-id="49d1e-103">Impersonation and Asynchronous Calls</span></span>

<span data-ttu-id="49d1e-104">Le serveur ne peut pas emprunter l’identité du client après l’appel du serveur à [**ISynchronize :: signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) , même si la méthode Begin n' \_ est pas encore terminée.</span><span class="sxs-lookup"><span data-stu-id="49d1e-104">The server cannot impersonate the client after the server's call to [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) completes, even if the Begin\_ method has not yet completed.</span></span> <span data-ttu-id="49d1e-105">Par exemple, supposons qu’un client appelle la méthode Begin, que le \_ serveur traite l’appel immédiatement et que le serveur appelle **signal** pour indiquer qu’il a terminé le traitement.</span><span class="sxs-lookup"><span data-stu-id="49d1e-105">For example, suppose a client calls the Begin\_ method, the server processes the call immediately, and the server calls **Signal** to indicate it is finished processing.</span></span> <span data-ttu-id="49d1e-106">Même si le travail reste à effectuer dans la \_ méthode Begin, le serveur ne peut pas emprunter l’identité du client une fois l’appel à **signal** terminé.</span><span class="sxs-lookup"><span data-stu-id="49d1e-106">Even if work remains to be done in the Begin\_ method, the server cannot impersonate the client after the call to **Signal** completes.</span></span>

<span data-ttu-id="49d1e-107">Si le serveur emprunte l’identité du client avant d’appeler [**signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), le jeton d’emprunt d’identité n’est pas supprimé du thread tant que le serveur n’a pas appelé [**IServerSecurity :: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) ou jusqu’à ce que l’appel du serveur de commence, selon ce qui se produit en \_ premier.</span><span class="sxs-lookup"><span data-stu-id="49d1e-107">If the server impersonates the client before it calls [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), the impersonation token will not be removed from the thread until the server calls [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) or until the server's call to Begin\_ returns, whichever comes first.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49d1e-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49d1e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49d1e-109">Délégation et emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="49d1e-109">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> <dt>

[<span data-ttu-id="49d1e-110">Exécution d’un appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="49d1e-110">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 