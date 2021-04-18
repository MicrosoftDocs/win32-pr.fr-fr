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
# <a name="reference-counting-activation-contexts"></a>Contextes d’activation de comptage de références

Les contextes d’activation sont des objets comptés par référence. Votre application doit avoir une référence sur un contexte d’activation pour pouvoir l’utiliser. Les fonctions de l’API de contexte d’activation qui prennent un contexte d’activation peuvent effectuer leur propre comptage de références. Par exemple, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) augmente et [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) diminue le nombre de références. Si, toutefois, votre application passe un contexte d’activation sans utiliser ces fonctions, l’application doit fournir sa propre méthode de décompte de références.

Quand une application appelle [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), le handle retourné aura un décompte de références d’un. Une fois l’application terminée avec le contexte d’activation, le handle doit être libéré et le nombre de références diminué en appelant [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx). N’essayez pas d’utiliser [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)ou toute autre fonction de gestion de la mémoire sur le handle de contexte d’activation.

L’exemple suivant montre une méthode pour gérer le décompte de références sur la durée de vie d’un contexte d’activation. La fonction FUNCT crée un contexte d’activation, qu’elle transmet ensuite à la cible de l’objet, ce qui incrémente le décompte de références à 2. FUNCT libère ensuite sa référence sur le contexte d’activation et diminue le nombre de références à 1. La cible est ensuite propriétaire de la libération de sa propre référence quand SetActCtx est à nouveau appelé ou lorsque l’objet est détruit.


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



 

 
