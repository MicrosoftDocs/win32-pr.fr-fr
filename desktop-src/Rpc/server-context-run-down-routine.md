---
title: Routine d’exécution du contexte de serveur
description: Si la communication s’arrête alors que le serveur gère le contexte pour le compte du client, une routine de nettoyage peut être nécessaire pour nettoyer l’état géré par le serveur pour le compte d’un client donné.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ad8afb7f698a258d7c4403143e74d566f813a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029655"
---
# <a name="server-context-run-down-routine"></a><span data-ttu-id="57b2d-103">Routine d’exécution du contexte de serveur</span><span class="sxs-lookup"><span data-stu-id="57b2d-103">Server Context Run-down Routine</span></span>

<span data-ttu-id="57b2d-104">Si la communication s’arrête alors que le serveur gère le contexte pour le compte du client, une routine de nettoyage peut être nécessaire pour nettoyer l’état géré par le serveur pour le compte d’un client donné.</span><span class="sxs-lookup"><span data-stu-id="57b2d-104">If communication breaks down while the server is maintaining context on behalf of the client, a cleanup routine may be needed to clean up the state maintained by the server on behalf of a given client.</span></span> <span data-ttu-id="57b2d-105">Cette routine de nettoyage est appelée « *routine d’exécution de contexte »*.</span><span class="sxs-lookup"><span data-stu-id="57b2d-105">This cleanup routine is called a *context run-down routine*.</span></span> <span data-ttu-id="57b2d-106">Lorsqu’une connexion est interrompue, le stub serveur et la bibliothèque Runtime appellent cette routine sur chaque handle de contexte ouvert par le client.</span><span class="sxs-lookup"><span data-stu-id="57b2d-106">When a connection breaks, the server stub and the run-time library will call this routine on every context handle opened by the client.</span></span>

<span data-ttu-id="57b2d-107">La routine d’exécution de contexte est obligatoire, et est déclarée implicitement et nommée, lorsque vous appliquez l' \[ attribut de **\_ handle de contexte** \] à une définition de type.</span><span class="sxs-lookup"><span data-stu-id="57b2d-107">The context run-down routine is required, and is implicitly declared and named, when you apply the \[**context\_handle**\] attribute to a type definition.</span></span> <span data-ttu-id="57b2d-108">Le serveur n’appellera pas la routine d’exécution de contexte si l' \[ attribut de **\_ handle de contexte** \] était appliqué directement à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="57b2d-108">The server will not call the context run-down routine if the \[**context\_handle**\] attribute was applied directly to a parameter.</span></span>

<span data-ttu-id="57b2d-109">La syntaxe de la routine d’exécution de contexte est la suivante :</span><span class="sxs-lookup"><span data-stu-id="57b2d-109">The context run-down routine syntax is:</span></span>

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

<span data-ttu-id="57b2d-110">Notez que le nom du type détermine le nom de la routine d’exécution du contexte.</span><span class="sxs-lookup"><span data-stu-id="57b2d-110">Note that the type name determines the name of the context run-down routine.</span></span>

<span data-ttu-id="57b2d-111">Le fragment de code qui suit présente un exemple de routine d’exécution de contexte.</span><span class="sxs-lookup"><span data-stu-id="57b2d-111">The code fragment that follows presents a sample context run-down routine.</span></span> <span data-ttu-id="57b2d-112">qui appelle la procédure RemoteClose utilisée dans l’exemple dans le [développement d’interface à l’aide de handles de contexte](interface-development-using-context-handles.md), le [développement serveur à l’aide de handles de contexte](server-development-using-context-handles.md)et le [développement client à l’aide de handles de contexte](client-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="57b2d-112">that calls the RemoteClose procedure used in the example in [Interface Development Using Context Handles](interface-development-using-context-handles.md), [Server Development Using Context Handles](server-development-using-context-handles.md), and [Client Development Using Context Handles](client-development-using-context-handles.md).</span></span> <span data-ttu-id="57b2d-113">Cette procédure ferme le descripteur de fichier, libère la mémoire associée au fichier et assigne la **valeur null** au handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="57b2d-113">This procedure closes the file handle, frees the memory associated with the file, and assigns **NULL** to the context handle.</span></span> <span data-ttu-id="57b2d-114">L’attribution de la **valeur null** est le résultat de l’appel de la fonction RemoteClose et n’est pas nécessaire dans un scénario d’exécution.</span><span class="sxs-lookup"><span data-stu-id="57b2d-114">Assigning **NULL** is a result of calling the RemoteClose function, and is not necessary in a run-down scenario.</span></span> <span data-ttu-id="57b2d-115">L’heure d’exécution RPC nettoie son état, que le handle de contexte ait la valeur **null** ou non.</span><span class="sxs-lookup"><span data-stu-id="57b2d-115">The RPC run time cleans up its state regardless of whether the context handle is set to **NULL**.</span></span>

``` syntax
//file: cxhndp.c (fragment of file containing remote procedures)
//The rundown routine is associated with the context handle type.  
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown(
    PCONTEXT_HANDLE_TYPE phContext)
{
    printf("Client died with an open file, closing it..\n");
    RemoteClose(&phContext);
    assert(phContext == 0);
}
```

 

 




