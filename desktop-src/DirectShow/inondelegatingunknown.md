---
description: L’interface INonDelegatingUnknown est une version de IUnknown qui est renommée pour permettre la prise en charge de nondelegating et de la délégation d’interfaces IUnknown dans le même objet COM.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: INonDelegatingUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543898"
---
# <a name="inondelegatingunknown"></a><span data-ttu-id="1eb72-103">INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="1eb72-103">INonDelegatingUnknown</span></span>

<span data-ttu-id="1eb72-104">L' `INonDelegatingUnknown` interface est une version de **IUnknown** qui est renommée pour permettre la prise en charge de la nondelegating et de la délégation des interfaces **IUnknown** dans le même objet com.</span><span class="sxs-lookup"><span data-stu-id="1eb72-104">The `INonDelegatingUnknown` interface is a version of **IUnknown** that is renamed to enable support for both nondelegating and delegating **IUnknown** interfaces in the same COM object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb72-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eb72-105">Syntax</span></span>


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a><span data-ttu-id="1eb72-106">Notes</span><span class="sxs-lookup"><span data-stu-id="1eb72-106">Remarks</span></span>

<span data-ttu-id="1eb72-107">Pour utiliser `INonDelegatingUnknown` pour l’héritage multiple, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="1eb72-107">To use `INonDelegatingUnknown` for multiple inheritance, perform the following steps.</span></span>

1.  <span data-ttu-id="1eb72-108">Dérivez votre classe d’une interface, par exemple IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="1eb72-108">Derive your class from an interface, for example, IMyInterface.</span></span>
2.  <span data-ttu-id="1eb72-109">Incluez [**Declare \_ IUnknown**](declare-iunknown.md) dans votre définition de classe pour déclarer des implémentations de **QueryInterface**, **AddRef** et **Release** qui appellent l’externe Unknown.</span><span class="sxs-lookup"><span data-stu-id="1eb72-109">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition to declare implementations of **QueryInterface**, **AddRef**, and **Release** that call the outer unknown.</span></span>
3.  <span data-ttu-id="1eb72-110">Remplacez **NonDelegatingQueryInterface** pour exposer IMyInterface à l’aide d’un code tel que le suivant :</span><span class="sxs-lookup"><span data-stu-id="1eb72-110">Override **NonDelegatingQueryInterface** to expose IMyInterface with code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="1eb72-111">Déclarez et implémentez les fonctions membres de IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="1eb72-111">Declare and implement the member functions of IMyInterface.</span></span>

<span data-ttu-id="1eb72-112">Pour utiliser `INonDelegatingUnknown` pour les interfaces imbriquées, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1eb72-112">To use `INonDelegatingUnknown` for nested interfaces, perform the following steps:</span></span>

1.  <span data-ttu-id="1eb72-113">Déclarez une classe dérivée de [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="1eb72-113">Declare a class derived from [**CUnknown**](cunknown.md).</span></span>
2.  <span data-ttu-id="1eb72-114">Incluez [**Declare \_ IUnknown**](declare-iunknown.md) dans votre définition de classe.</span><span class="sxs-lookup"><span data-stu-id="1eb72-114">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition.</span></span>
3.  <span data-ttu-id="1eb72-115">Remplacez **NonDelegatingQueryInterface** pour exposer IMyInterface avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="1eb72-115">Override **NonDelegatingQueryInterface** to expose IMyInterface with the code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="1eb72-116">Implémentez les fonctions membres de IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="1eb72-116">Implement the member functions of IMyInterface.</span></span> <span data-ttu-id="1eb72-117">Utilisez [**CUnknown :: GetOwner**](cunknown-getowner.md) pour accéder à la classe d’objets com.</span><span class="sxs-lookup"><span data-stu-id="1eb72-117">Use [**CUnknown::GetOwner**](cunknown-getowner.md) to access the COM object class.</span></span>
5.  <span data-ttu-id="1eb72-118">Dans votre classe d’objets COM, faites de la classe imbriquée un Friend de la classe d’objet COM, puis déclarez une instance de la classe imbriquée en tant que membre de la classe d’objets COM.</span><span class="sxs-lookup"><span data-stu-id="1eb72-118">In your COM object class, make the nested class a friend of the COM object class, and declare an instance of the nested class as a member of the COM object class.</span></span>

<span data-ttu-id="1eb72-119">Étant donné que vous devez toujours passer l’externe Unknown et un **HRESULT** au constructeur [**CUnknown**](cunknown.md) , vous ne pouvez pas utiliser un constructeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="1eb72-119">Because you must always pass the outer unknown and an **HRESULT** to the [**CUnknown**](cunknown.md) constructor, you can't use a default constructor.</span></span> <span data-ttu-id="1eb72-120">Vous devez transformer la variable membre en pointeur vers la classe et en faire un nouvel appel dans votre constructeur pour la créer réellement.</span><span class="sxs-lookup"><span data-stu-id="1eb72-120">You have to make the member variable a pointer to the class and make a new call in your constructor to actually create it.</span></span>

<span data-ttu-id="1eb72-121">Remplacez le **NonDelegatingQueryInterface** par un code tel que le suivant :</span><span class="sxs-lookup"><span data-stu-id="1eb72-121">Override the **NonDelegatingQueryInterface** with code such as the following:</span></span>


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



<span data-ttu-id="1eb72-122">Vous pouvez avoir des classes mixtes qui prennent en charge certaines interfaces via un héritage multiple et certaines interfaces via des classes imbriquées.</span><span class="sxs-lookup"><span data-stu-id="1eb72-122">You can have mixed classes that support some interfaces through multiple inheritance and some interfaces through nested classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb72-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1eb72-123">Requirements</span></span>



| <span data-ttu-id="1eb72-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eb72-124">Requirement</span></span> | <span data-ttu-id="1eb72-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eb72-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb72-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1eb72-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1eb72-127"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1eb72-127"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1eb72-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1eb72-128">Library</span></span><br/> | <dl> <span data-ttu-id="1eb72-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1eb72-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eb72-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eb72-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb72-131">**Fonctions d’assistance COM**</span><span class="sxs-lookup"><span data-stu-id="1eb72-131">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




