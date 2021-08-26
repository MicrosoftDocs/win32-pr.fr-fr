---
description: cette rubrique explique comment implémenter la journalisation des erreurs dans DirectShow Services d’édition.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Création d’une classe de journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 194d927b2e4eae73f75a326ed03363d96f6121634e46b606ba87409e3bf07f9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108199"
---
# <a name="creating-an-error-logging-class"></a>Création d’une classe de journalisation des erreurs

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

cette rubrique explique comment implémenter la journalisation des erreurs dans [DirectShow Services d’édition](directshow-editing-services.md).

Tout d’abord, déclarez une classe qui implémente la journalisation des erreurs. La classe hérite de l’interface [**IAMErrorLog**](iamerrorlog.md) . Elle contient des déclarations pour les trois méthodes **IUnknown** et pour la méthode unique dans [IAMErrorLog](implementing-iamerrorlog.md). La déclaration de classe se présente comme suit :


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



La seule variable membre de la classe est m \_ lRef, qui contient le nombre de références de l’objet.

Ensuite, définissez les méthodes dans **IUnknown**. L’exemple suivant illustre une implémentation standard de ces méthodes :


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



Avec l’infrastructure COM en place, vous pouvez désormais implémenter l’interface **IAMErrorLog** . La section suivante décrit la procédure à suivre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Journalisation des erreurs](logging-errors.md)
</dt> </dl>

 

 



