---
title: Unions encapsulées
description: Une Union qui est contenue avec son discriminante dans une structure dans est une Union encapsulée.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- types de données MIDL, unions encapsulées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4489a043ff3690ddb31a8acccf359dcd76940aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512690"
---
# <a name="encapsulated-unions"></a><span data-ttu-id="fce90-104">Unions encapsulées</span><span class="sxs-lookup"><span data-stu-id="fce90-104">Encapsulated Unions</span></span>

<span data-ttu-id="fce90-105">Une Union qui est contenue avec son discriminante dans une structure dans est une Union encapsulée.</span><span class="sxs-lookup"><span data-stu-id="fce90-105">A union that is contained with its discriminant in a structure within is an encapsulated union.</span></span> <span data-ttu-id="fce90-106">L’Union encapsulée est indiquée par la présence du mot clé [**switch**](switch.md) .</span><span class="sxs-lookup"><span data-stu-id="fce90-106">The encapsulated union is indicated by the presence of the [**switch**](switch.md) keyword.</span></span> <span data-ttu-id="fce90-107">Ce type d’Union est donc nommé, car le compilateur MIDL encapsule automatiquement l’Union et son discriminante dans une structure de transmission pendant un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="fce90-107">This type of union is so named because the MIDL compiler automatically encapsulates the union and its discriminant in a structure for transmission during a remote procedure call.</span></span>

<span data-ttu-id="fce90-108">Si la balise Union est manquante ( \_ type U1 dans l’exemple ci-dessus), le compilateur génère la structure avec le champ d’Union nommé *\_ Union avec balises*.</span><span class="sxs-lookup"><span data-stu-id="fce90-108">If the union tag is missing (U1\_TYPE in the example above), the compiler will generate the structure with the union field named *tagged\_union*.</span></span>

<span data-ttu-id="fce90-109">La forme des unions doit être la même sur toutes les plateformes pour garantir l’interconnexion.</span><span class="sxs-lookup"><span data-stu-id="fce90-109">The shape of unions must be the same across platforms to ensure interconnectivity.</span></span>

<span data-ttu-id="fce90-110">Pour obtenir une description de la forme d’une Union encapsulée, consultez [**Union**](union.md).</span><span class="sxs-lookup"><span data-stu-id="fce90-110">For a description of the form of an encapsulated union, see [**union**](union.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fce90-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="fce90-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

<span data-ttu-id="fce90-112">Pour obtenir des informations connexes, consultez [types de base MIDL](midl-base-types.md), [**char**](char-idl.md), **\[** [**\_ descripteur de contexte**](context-handle.md) **\]** , [**enum**](enum.md), **\[** [**First \_ is**](first-is.md) **\]** , **\[** [**handle**](handle.md) **\]** , **\[** [**ignore**](ignore.md) **\]** [**int**](int.md), **\[** [**ignore**](ignore.md), **\]** **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md), **\]** **\[** [**MS \_ Union**](ms-union-attrib.md) **\]** , [unencapsulated unions](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md) **\]** , **\[** [**ref**](ref.md) **\]** , **\[** [**size \_ is**](size-is.md), **\]** **\[** [**String**](string.md) **\]** , [**struct**](struct.md), [**switch**](switch.md), **\[** [**Switch \_ is**](switch-is.md) **\]** , **\[** [**Switch \_ type**](switch-type.md) **\]** , **\[** [**transmit \_ As**](transmit-as.md) **\]** , [**Union**](union.md)et **\[** [**unique**](unique.md)**\]**</span><span class="sxs-lookup"><span data-stu-id="fce90-112">For related information, see [MIDL Base Types](midl-base-types.md), [**char**](char-idl.md), **\[**[**context\_handle**](context-handle.md)**\]**, [**enum**](enum.md), **\[**[**first\_is**](first-is.md)**\]**, **\[**[**handle**](handle.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, [**int**](int.md), **\[**[**ignore**](ignore.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**ms\_union**](ms-union-attrib.md)**\]**, [Nonencapsulated Unions](nonencapsulated-unions.md), **\[**[**ptr**](ptr.md)**\]**, **\[**[**ref**](ref.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, **\[**[**string**](string.md)**\]**, [**struct**](struct.md), [**switch**](switch.md), **\[**[**switch\_is**](switch-is.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**, [**union**](union.md), and **\[**[**unique**](unique.md)**\]**</span></span>

 

 




