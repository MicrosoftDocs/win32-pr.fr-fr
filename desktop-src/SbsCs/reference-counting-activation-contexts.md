---
description: Les contextes d’activation sont des objets comptés par référence. Votre application doit avoir une référence sur un contexte d’activation pour pouvoir l’utiliser.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Contextes d’activation de comptage de références
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff00afa0dd3a347e14ff9723c06d54af4520ce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536595"
---
# <a name="reference-counting-activation-contexts"></a><span data-ttu-id="93918-104">Contextes d’activation de comptage de références</span><span class="sxs-lookup"><span data-stu-id="93918-104">Reference Counting Activation Contexts</span></span>

<span data-ttu-id="93918-105">Les contextes d’activation sont des objets comptés par référence.</span><span class="sxs-lookup"><span data-stu-id="93918-105">Activation contexts are reference-counted objects.</span></span> <span data-ttu-id="93918-106">Votre application doit avoir une référence sur un contexte d’activation pour pouvoir l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="93918-106">Your application must have a reference on an activation context in order to use it.</span></span> <span data-ttu-id="93918-107">Les fonctions de l’API de contexte d’activation qui prennent un contexte d’activation peuvent effectuer leur propre comptage de références.</span><span class="sxs-lookup"><span data-stu-id="93918-107">The functions of the Activation Context API that take an activation context can perform their own reference counting.</span></span> <span data-ttu-id="93918-108">Par exemple, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) augmente et [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) diminue le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="93918-108">For example, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) increases and [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) decreases the reference count.</span></span> <span data-ttu-id="93918-109">Si, toutefois, votre application passe un contexte d’activation sans utiliser ces fonctions, l’application doit fournir sa propre méthode de décompte de références.</span><span class="sxs-lookup"><span data-stu-id="93918-109">If however your application passes an activation context without using these functions, the application should provide its own method of reference counting.</span></span>

<span data-ttu-id="93918-110">Quand une application appelle [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), le handle retourné aura un décompte de références d’un.</span><span class="sxs-lookup"><span data-stu-id="93918-110">When an application calls [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), the handle returned will have a reference count of one.</span></span> <span data-ttu-id="93918-111">Une fois l’application terminée avec le contexte d’activation, le handle doit être libéré et le nombre de références diminué en appelant [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span><span class="sxs-lookup"><span data-stu-id="93918-111">After the application finishes with the activation context, the handle should be released and the reference count decreased by calling [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span></span> <span data-ttu-id="93918-112">N’essayez pas d’utiliser [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)ou toute autre fonction de gestion de la mémoire sur le handle de contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="93918-112">Do not attempt to use [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree), or any other memory-management functions on the activation context handle.</span></span>

<span data-ttu-id="93918-113">L’exemple suivant montre une méthode pour gérer le décompte de références sur la durée de vie d’un contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="93918-113">The following example shows a method for handling reference counting over the lifetime of an activation context.</span></span> <span data-ttu-id="93918-114">La fonction FUNCT crée un contexte d’activation, qu’elle transmet ensuite à la cible de l’objet, ce qui incrémente le décompte de références à 2.</span><span class="sxs-lookup"><span data-stu-id="93918-114">The function Funct creates an activation context, which it then passes to the object Target, which increments the reference count to 2.</span></span> <span data-ttu-id="93918-115">FUNCT libère ensuite sa référence sur le contexte d’activation et diminue le nombre de références à 1.</span><span class="sxs-lookup"><span data-stu-id="93918-115">Funct then releases its reference on the activation context and decreases the reference count back to 1.</span></span> <span data-ttu-id="93918-116">La cible est ensuite propriétaire de la libération de sa propre référence quand SetActCtx est à nouveau appelé ou lorsque l’objet est détruit.</span><span class="sxs-lookup"><span data-stu-id="93918-116">Target then owns releasing its own reference when SetActCtx is called again or when the object is destroyed.</span></span>


```C++
#include <windows.h>

class CMyObject 
{
private:
    HANDLE m_hActCtx;
public:
    CMyObject() : m_hActCtx(INVALID_HANDLE_VALUE) { }
    ~CMyObject() 
    { 
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
            m_hActCtx = INVALID_HANDLE_VALUE;
        }
    }
    void SetActCtx(HANDLE hActCtx) 
    {
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
        }
        m_hActCtx = hActCtx;
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            AddRefActCtx(m_hActCtx);
        }
    }
    void DoWorkWithActCtx();
};

void Funct(CMyObject &Target) 
{
    HANDLE hActCtx;
    ACTCTX actctx = { sizeof(ACTCTX) };
    hActCtx = CreateActCtx(&actctx);  //create activation context  
    Target.SetActCtx(hActCtx);    //pass activation context to Target; 
    // actctx now has 1 more reference
    ReleaseActCtx(hActCtx);
}
```



 

 
