---
description: Modification des valeurs de retour par COM+
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Modification des valeurs de retour par COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110918"
---
# <a name="how-com-modifies-return-values"></a><span data-ttu-id="14973-103">Modification des valeurs de retour par COM+</span><span class="sxs-lookup"><span data-stu-id="14973-103">How COM+ Modifies Return Values</span></span>

<span data-ttu-id="14973-104">COM+ ne modifie jamais la valeur de retour d’un **HRESULT** qui indique un échec, par exemple e \_ inattendu ou e \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="14973-104">COM+ never changes the return value of an **HRESULT** that indicates failure, such as E\_UNEXPECTED or E\_FAIL.</span></span> <span data-ttu-id="14973-105">Toutefois, lorsqu’un objet utilisant la fonctionnalité COM+ retourne une valeur **HRESULT** indiquant une réussite (telle que s \_ OK, s \_ false ou NOerror), com+ convertit parfois le **HRESULT** en code d’erreur com+ avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="14973-105">However, when an object using COM+ functionality returns an **HRESULT** value indicating success (such as S\_OK, S\_FALSE, or NOERROR), COM+ sometimes converts the **HRESULT** into a COM+ error code before it returns to the caller.</span></span>

<span data-ttu-id="14973-106">Par exemple, lorsqu’une application retourne un \_ OK après avoir appelé [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), si l’objet est la racine d’une transaction dont la validation échoue, la valeur **HRESULT** est convertie en contexte \_ E \_ abandonné.</span><span class="sxs-lookup"><span data-stu-id="14973-106">For example, when an application returns S\_OK after calling [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), if the object is the root of a transaction that fails to commit, the **HRESULT** is converted to CONTEXT\_E\_ABORTED.</span></span>

<span data-ttu-id="14973-107">Lorsque COM+ convertit une valeur **HRESULT** , il efface tous les paramètres de sortie de la méthode.</span><span class="sxs-lookup"><span data-stu-id="14973-107">When COM+ converts an **HRESULT** value, it clears all of the method's output parameters.</span></span> <span data-ttu-id="14973-108">Les références retournées sont libérées et les valeurs des pointeurs d’objets retournés ont la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="14973-108">Returned references are released, and the values of the returned object pointers are set to **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14973-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14973-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14973-110">Isolation des erreurs et stratégie FailFast</span><span class="sxs-lookup"><span data-stu-id="14973-110">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="14973-111">Recherche de la source d’une erreur</span><span class="sxs-lookup"><span data-stu-id="14973-111">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="14973-112">Interprétation des codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="14973-112">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="14973-113">Stratégies de gestion des erreurs dans COM+</span><span class="sxs-lookup"><span data-stu-id="14973-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="14973-114">Dépannage</span><span class="sxs-lookup"><span data-stu-id="14973-114">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



