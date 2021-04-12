---
title: Exemple de résolution des conflits de noms de fonctions
description: Cette rubrique explique comment résoudre les conflits de nom de fonction lors de la création d’une extension pour ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, exemple de code Visual Basic, résolution des conflits de noms de fonctions
- résolution des conflits de noms de fonction ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049f9ce6447bf6d6ead783db3e34f74374333f10
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316464"
---
# <a name="example-for-resolving-function-name-conflicts"></a><span data-ttu-id="1491a-105">Exemple de résolution des conflits de noms de fonctions</span><span class="sxs-lookup"><span data-stu-id="1491a-105">Example for Resolving Function Name Conflicts</span></span>

<span data-ttu-id="1491a-106">Tenez compte des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1491a-106">Consider the following:</span></span>

-   <span data-ttu-id="1491a-107">IADs0 ne prend pas en charge Func0.</span><span class="sxs-lookup"><span data-stu-id="1491a-107">IADs0 does not support Func0.</span></span>
-   <span data-ttu-id="1491a-108">IADs1 prend en charge func1 et Func0.</span><span class="sxs-lookup"><span data-stu-id="1491a-108">IADs1 supports Func1 and Func0.</span></span>
-   <span data-ttu-id="1491a-109">IADs2 prend en charge Func2 et Func0.</span><span class="sxs-lookup"><span data-stu-id="1491a-109">IADs2 supports Func2 and Func0.</span></span>

<span data-ttu-id="1491a-110">Les trois interfaces sont des interfaces doubles.</span><span class="sxs-lookup"><span data-stu-id="1491a-110">All three interfaces are dual interfaces.</span></span>


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



<span data-ttu-id="1491a-111">Sachez que même si IADs1 ne prend pas en charge Func2, un client ADSI reconnaît un [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui prend en charge toutes les interfaces doubles et de dispatch dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="1491a-111">Be aware that even though IADs1 does not support Func2, an ADSI client recognizes one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that supports all the dual and dispatch interfaces in the model.</span></span> <span data-ttu-id="1491a-112">Ainsi, le client ADSI peut appeler directement Func2 à l’aide de myInf1. Func2 sans résoudre l’interface qui prend en charge Func2.</span><span class="sxs-lookup"><span data-stu-id="1491a-112">Thus, the ADSI client can directly call Func2 using myInf1.Func2 without resolving which interface supports Func2.</span></span>


```VB
myInf1.Func2
```



<span data-ttu-id="1491a-113">IADs1 et IADs2 ont une fonction appelée Func0, mais IADs1 :: Func0 est appelé directement à l’aide de l’accès vtable, car les deux éléments suivants s’appliquent au client :</span><span class="sxs-lookup"><span data-stu-id="1491a-113">Both IADs1 and IADs2 have a function called Func0, but IADs1::Func0 is invoked directly using vtable access, because both of following apply to the client:</span></span>

-   <span data-ttu-id="1491a-114">Le client a un pointeur vers un objet IADs1 à deux interfaces, qui a une fonction appelée Func0.</span><span class="sxs-lookup"><span data-stu-id="1491a-114">The client has a pointer to dual interface IADs1 object, which has a function called Func0.</span></span>
-   <span data-ttu-id="1491a-115">Visual Basic prend en charge l’accès direct à la vtable, en supposant que ce type de données est disponible via la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="1491a-115">Visual Basic supports direct vtable access, assuming that type of data is available through the type library.</span></span>

<span data-ttu-id="1491a-116">Dans l’exemple de code suivant, le client a un pointeur d’interface double vers IADs2 au lieu de IADs1.</span><span class="sxs-lookup"><span data-stu-id="1491a-116">In the next code example, the client has a dual interface pointer to IADs2 instead of IADs1.</span></span> <span data-ttu-id="1491a-117">Par conséquent, IADs2 :: Func0 est appelé à l’aide d’un accès direct à la vtable.</span><span class="sxs-lookup"><span data-stu-id="1491a-117">Therefore, IADs2::Func0 is invoked using direct vtable access.</span></span>


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



<span data-ttu-id="1491a-118">Là encore, dans l’exemple de code suivant, IADs1 et IADs2 ont une fonction appelée Func0, mais ici, le client a un pointeur vers une interface double, IADs0, qui n’a pas de fonction appelée Func0.</span><span class="sxs-lookup"><span data-stu-id="1491a-118">Again, in the next code example, both IADs1 and IADs2 have a function called Func0, but, here, the client has a pointer to a dual interface, IADs0, which does not have a function called Func0.</span></span> <span data-ttu-id="1491a-119">Par conséquent, aucun accès direct à la vtable ne peut être effectué.</span><span class="sxs-lookup"><span data-stu-id="1491a-119">Therefore, no direct vtable access can be performed.</span></span> <span data-ttu-id="1491a-120">Au lieu de cela, [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) et [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) sont appelés pour appeler Func0.</span><span class="sxs-lookup"><span data-stu-id="1491a-120">Instead, [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) are called to invoke Func0.</span></span>


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



<span data-ttu-id="1491a-121">Considérons les deux cas suivants :</span><span class="sxs-lookup"><span data-stu-id="1491a-121">Consider these two cases:</span></span>

-   <span data-ttu-id="1491a-122">IADs1 et IADs2 sont implémentés par deux composants COM, EXT1 et ext2, respectivement.</span><span class="sxs-lookup"><span data-stu-id="1491a-122">IADs1 and IADs2 are implemented by two COM components, Ext1 and Ext2, respectively.</span></span> <span data-ttu-id="1491a-123">Si EXT1 vient avant ext2 dans le registre, IADs1 :: Func0 est appelé.</span><span class="sxs-lookup"><span data-stu-id="1491a-123">If Ext1 comes before Ext2 in the registry, IADs1::Func0 is invoked.</span></span> <span data-ttu-id="1491a-124">Toutefois, si ext2 est en premier dans le registre, IADs2 :: Func0 est appelé.</span><span class="sxs-lookup"><span data-stu-id="1491a-124">However, if Ext2 comes first in the registry, IADs2::Func0 is invoked.</span></span>
-   <span data-ttu-id="1491a-125">Si IADs1 et ADs2 sont implémentés par le même objet d’extension, Func0 est toujours appelé par les méthodes [**IADsExtension ::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) et [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) de l’extension.</span><span class="sxs-lookup"><span data-stu-id="1491a-125">If IADs1 and ADs2 are implemented by the same extension object, Func0 is always invoked by the extension's [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods.</span></span>

<span data-ttu-id="1491a-126">Le développeur de l’extension doit déterminer comment résoudre les conflits de fonctions ou de propriétés de différentes interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) doubles portant le même nom dans une extension.</span><span class="sxs-lookup"><span data-stu-id="1491a-126">The extension developer must determine how to resolve conflicts of functions, or properties, of different dual [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces that have the same name in an extension.</span></span> <span data-ttu-id="1491a-127">L’implémentation de [**IADsExtension ::P méthodes rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) et [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) doit résoudre ce conflit.</span><span class="sxs-lookup"><span data-stu-id="1491a-127">The implementation of [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods should resolve this conflict.</span></span> <span data-ttu-id="1491a-128">Par exemple, si vous utilisez IMyInterface1 :: func1 et IMyInterface2 :: func1, où IMyInterface1 et IMyInterface2 sont des interfaces **IDispatch** doubles prises en charge par le même objet d’extension.</span><span class="sxs-lookup"><span data-stu-id="1491a-128">For example, if you use IMyInterface1::Func1 and IMyInterface2::Func1, where IMyInterface1 and IMyInterface2 are dual **IDispatch** interfaces supported by the same extension object.</span></span> <span data-ttu-id="1491a-129">Les méthodes **PrivateGetIDsOfNames** et **PrivateInvoke** doivent déterminer le func1 à toujours appeler.</span><span class="sxs-lookup"><span data-stu-id="1491a-129">The **PrivateGetIDsOfNames** and **PrivateInvoke** methods must determine which Func1 should always be called.</span></span>

<span data-ttu-id="1491a-130">Il en va de même pour les DISPID conflictuels dans différentes interfaces Dual ou [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="1491a-130">The same applies to conflicting DISPIDs in different dual or [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span>

<span data-ttu-id="1491a-131">Par exemple, le DISPID de IMyInterface1 :: Y est 2 dans le fichier IMyInterface1. ODL ou IMyInterface1. idl.</span><span class="sxs-lookup"><span data-stu-id="1491a-131">For example, the DISPID of IMyInterface1::Y is 2 in the file imyinterface1.odl, or imyinterface1.idl.</span></span> <span data-ttu-id="1491a-132">Le DISPID de IMyInterface2 :: X est également 2 dans iMyInterface2. ODL.</span><span class="sxs-lookup"><span data-stu-id="1491a-132">The DISPID of IMyInterface2::X is also 2 in iMyInterface2.odl.</span></span> <span data-ttu-id="1491a-133">[**IADsExtension ::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) doit retourner un DISPID unique, au sein de l’extension elle-même, pour chaque, au lieu de retourner le même DISPID pour les deux.</span><span class="sxs-lookup"><span data-stu-id="1491a-133">[**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) must return a unique DISPID, within the extension itself, for each, instead of returning the same DISPID for both.</span></span>

<span data-ttu-id="1491a-134">ADSI résout le premier problème en ne prenant pas en charge plusieurs interfaces avec des noms de fonctions ou de propriétés conflictuels.</span><span class="sxs-lookup"><span data-stu-id="1491a-134">ADSI resolves the first problem by not supporting multiple interfaces with conflicting function or property names.</span></span> <span data-ttu-id="1491a-135">Il résout le deuxième problème en ajoutant un unique, qui se trouve dans le même objet d’extension, le numéro d’interface aux bits inutilisés du DISPID.</span><span class="sxs-lookup"><span data-stu-id="1491a-135">It resolves the second problem by adding a unique, that is within the same extension object, interface number to the unused bits of the DISPID.</span></span>

 

 