---
title: Exemple de résolution des conflits de noms de fonctions
description: Cette rubrique explique comment résoudre les conflits de nom de fonction lors de la création d’une extension pour ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- adsi adsi, exemple de code Visual Basic, résolution des conflits de noms de fonctions
- résolution des conflits de noms de fonction ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6ce09251ba61b31768d973e258c568694067aff0420f0512a13913bb6fce90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179979"
---
# <a name="example-for-resolving-function-name-conflicts"></a>Exemple de résolution des conflits de noms de fonctions

Tenez compte des éléments suivants :

-   IADs0 ne prend pas en charge Func0.
-   IADs1 prend en charge func1 et Func0.
-   IADs2 prend en charge Func2 et Func0.

Les trois interfaces sont des interfaces doubles.


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



Sachez que même si IADs1 ne prend pas en charge Func2, un client ADSI reconnaît un [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui prend en charge toutes les interfaces doubles et de dispatch dans le modèle. Ainsi, le client ADSI peut appeler directement Func2 à l’aide de myInf1. Func2 sans résoudre l’interface qui prend en charge Func2.


```VB
myInf1.Func2
```



IADs1 et IADs2 ont une fonction appelée Func0, mais IADs1 :: Func0 est appelé directement à l’aide de l’accès vtable, car les deux éléments suivants s’appliquent au client :

-   Le client a un pointeur vers un objet IADs1 à deux interfaces, qui a une fonction appelée Func0.
-   Visual Basic prend en charge l’accès direct à la vtable, en supposant que ce type de données est disponible via la bibliothèque de types.

Dans l’exemple de code suivant, le client a un pointeur d’interface double vers IADs2 au lieu de IADs1. Par conséquent, IADs2 :: Func0 est appelé à l’aide d’un accès direct à la vtable.


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



Là encore, dans l’exemple de code suivant, IADs1 et IADs2 ont une fonction appelée Func0, mais ici, le client a un pointeur vers une interface double, IADs0, qui n’a pas de fonction appelée Func0. Par conséquent, aucun accès direct à la vtable ne peut être effectué. Au lieu de cela, [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) et [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) sont appelés pour appeler Func0.


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



Considérons les deux cas suivants :

-   IADs1 et IADs2 sont implémentés par deux composants COM, EXT1 et ext2, respectivement. Si EXT1 vient avant ext2 dans le registre, IADs1 :: Func0 est appelé. Toutefois, si ext2 est en premier dans le registre, IADs2 :: Func0 est appelé.
-   Si IADs1 et ADs2 sont implémentés par le même objet d’extension, Func0 est toujours appelé par les méthodes [**IADsExtension ::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) et [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) de l’extension.

Le développeur de l’extension doit déterminer comment résoudre les conflits de fonctions ou de propriétés de différentes interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) doubles portant le même nom dans une extension. L’implémentation de [**IADsExtension ::P méthodes rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) et [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) doit résoudre ce conflit. Par exemple, si vous utilisez IMyInterface1 :: func1 et IMyInterface2 :: func1, où IMyInterface1 et IMyInterface2 sont des interfaces **IDispatch** doubles prises en charge par le même objet d’extension. Les méthodes **PrivateGetIDsOfNames** et **PrivateInvoke** doivent déterminer le func1 à toujours appeler.

Il en va de même pour les DISPID conflictuels dans différentes interfaces Dual ou [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .

Par exemple, le DISPID de IMyInterface1 :: Y est 2 dans le fichier IMyInterface1. ODL ou IMyInterface1. idl. Le DISPID de IMyInterface2 :: X est également 2 dans iMyInterface2. ODL. [**IADsExtension ::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) doit retourner un DISPID unique, au sein de l’extension elle-même, pour chaque, au lieu de retourner le même DISPID pour les deux.

ADSI résout le premier problème en ne prenant pas en charge plusieurs interfaces avec des noms de fonctions ou de propriétés conflictuels. Il résout le deuxième problème en ajoutant un unique, qui se trouve dans le même objet d’extension, le numéro d’interface aux bits inutilisés du DISPID.

 

 