---
description: DirectShow implémente IUnknown dans une classe de base appelée CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Utilisation de CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523289"
---
# <a name="using-cunknown"></a>Utilisation de CUnknown

DirectShow implémente [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dans une classe de base appelée [**CUnknown**](cunknown.md). Vous pouvez utiliser **CUnknown** pour dériver d’autres classes, en substituant uniquement les méthodes qui changent d’un composant à l’autre. La plupart des autres classes de base de DirectShow dérivant de **CUnknown**, votre composant peut hériter directement de **CUnknown** ou d’une autre classe de base.

## <a name="inondelegatingunknown"></a>INonDelegatingUnknown

[**CUnknown**](cunknown.md) implémente [**INonDelegatingUnknown**](inondelegatingunknown.md). Il gère les nombres de références en interne et, dans la plupart des cas, votre classe dérivée peut hériter des deux méthodes de décompte de références sans modification. Sachez que **CUnknown** se supprime lui-même lorsque le nombre de références est atteint de zéro. En revanche, vous devez substituer [**CUnknown :: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), car la méthode dans la classe de base retourne E \_ nointerface si elle reçoit un IID autre que IID \_ IUnknown. Dans votre classe dérivée, testez les IID d’interfaces que vous prenez en charge, comme indiqué dans l’exemple suivant :


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



La fonction utilitaire [**GetInterface**](getinterface.md) (voir [**fonctions d’assistance com**](com-helper-functions.md)) définit le pointeur, incrémente le décompte de références de manière thread-safe et retourne S \_ OK. Dans le cas par défaut, appelez la méthode de la classe de base et retournez le résultat. Si vous dérivez à partir d’une autre classe de base, appelez sa méthode [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) à la place. Cela vous permet de prendre en charge toutes les interfaces prises en charge par la classe parente.

## <a name="iunknown"></a>IUnknown

Comme indiqué précédemment, la version de la délégation de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) est la même pour chaque composant, car elle ne fait rien d’autre que d’appeler l’instance correcte de la version de nondelegating. Pour plus de commodité, le fichier d’en-tête ComBase. h contient une macro, [**déclarez \_ IUnknown**](declare-iunknown.md), qui déclare les trois méthodes de délégation comme des méthodes Inline. Il se développe jusqu’au code suivant :


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



La fonction utilitaire [**CUnknown :: GetOwner**](cunknown-getowner.md) récupère un pointeur vers l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du composant qui possède ce composant. Pour un composant agrégé, le propriétaire est le composant externe. Dans le cas contraire, le composant se trouve lui-même. Incluez la \_ macro DECLARE IUnknown dans la section public de votre définition de classe.

## <a name="class-constructor"></a>Constructeur de classe

Votre constructeur de classe doit appeler la méthode de constructeur pour la classe parente, en plus de tout ce qu’il fait, qui est spécifique à votre classe. L’exemple suivant est une méthode de constructeur typique :


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



La méthode prend les paramètres suivants, qu’elle transmet directement à la méthode du constructeur [**CUnknown**](cunknown.md) .

-   *tszName* spécifie un nom pour le composant.
-   *punk* est un pointeur vers l’agrégation [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).
-   *pHr* est un pointeur vers une valeur HRESULT indiquant la réussite ou l’échec de la méthode.

## <a name="summary"></a>Résumé

L’exemple suivant montre une classe dérivée qui prend en charge [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et une interface hypothétique nommée ISomeInterface :


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



Cet exemple illustre les points suivants :

-   La classe [**CUnknown**](cunknown.md) implémente l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Le nouveau composant hérite de **CUnknown** et de toutes les interfaces que le composant prend en charge. Le composant peut dériver à la place d’une autre classe de base qui hérite de **CUnknown**.
-   La macro [**Declare \_ IUnknown**](declare-iunknown.md) déclare les méthodes [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de délégation comme des méthodes Inline.
-   La classe [**CUnknown**](cunknown.md) fournit l’implémentation pour [**INonDelegatingUnknown**](inondelegatingunknown.md).
-   Pour prendre en charge une interface autre que [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), la classe dérivée doit substituer la méthode [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) et tester l’IID de la nouvelle interface.
-   Le constructeur de classe appelle la méthode de constructeur pour [**CUnknown**](cunknown.md).

L’étape suivante de l’écriture d’un filtre consiste à permettre à une application de créer de nouvelles instances du composant. Cela nécessite une compréhension des dll et de leur relation avec les fabriques de classes et les méthodes de constructeur de classe. Pour plus d’informations, voir [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment implémenter IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 
