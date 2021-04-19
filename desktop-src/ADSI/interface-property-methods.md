---
title: Méthodes de propriété d’interface
description: De nombreuses interfaces ADSI sont conçues pour prendre en charge l’automatisation et sont donc des interfaces doubles en ce sens qu’elles prennent en charge l’accès client via les interfaces IUnknown et IDispatch.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété d’interface
- ADSI ADSI, référence, méthodes de propriété expliquées
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510281"
---
# <a name="interface-property-methods"></a><span data-ttu-id="0da89-105">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="0da89-105">Interface Property Methods</span></span>

<span data-ttu-id="0da89-106">De nombreuses interfaces ADSI sont conçues pour prendre en charge l’automatisation et sont donc des interfaces doubles en ce sens qu’elles prennent en charge l’accès client via les interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="0da89-106">Many ADSI interfaces are designed to support Automation and thus are dual interfaces in that they support client access through both [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span> <span data-ttu-id="0da89-107">Les clients non-Automation, tels que ceux écrits en C/C++, résolvent directement l’appel de méthode, à l’aide de la méthode [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , et appellent la méthode directement.</span><span class="sxs-lookup"><span data-stu-id="0da89-107">Non-Automation clients, such as those written in C/C++, resolve method invocation directly, using the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, and call the method directly.</span></span> <span data-ttu-id="0da89-108">Les clients Automation, également appelés clients liés au nom, tels que ceux écrits en Visual Basic ou Visual Basic Scripting Edition (VBScript), doivent résoudre indirectement l’appel de méthode à l’aide de la méthode [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) .</span><span class="sxs-lookup"><span data-stu-id="0da89-108">Automation clients, also known as name-bound clients, such as those written in Visual Basic, or Visual Basic Scripting Edition (VBScript), must resolve method invocation indirectly using the [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) method.</span></span>

<span data-ttu-id="0da89-109">Une interface ADSI prenant en charge Automation définit des méthodes de propriété pour récupérer et modifier les propriétés d’un objet qui implémente l’interface.</span><span class="sxs-lookup"><span data-stu-id="0da89-109">An ADSI interface supporting Automation defines property methods for retrieving and modifying properties of an object implementing the interface.</span></span> <span data-ttu-id="0da89-110">Les méthodes de propriété ont des noms qui ont des noms d' **extraction** \_ et de **mise** \_ en avant des noms de propriété appropriés, par exemple, **obtenir un \_ utilisateur** et un **\_ nom de placement**.</span><span class="sxs-lookup"><span data-stu-id="0da89-110">The property methods have names that have **get**\_ and **put**\_ prepended to the appropriate property names, for example, **get\_User** and **put\_Name**.</span></span>

<span data-ttu-id="0da89-111">Chaque méthode d' **extraction \_** utilise un seul paramètre comme sortie.</span><span class="sxs-lookup"><span data-stu-id="0da89-111">Each **get\_** method takes a single parameter as output.</span></span> <span data-ttu-id="0da89-112">Ce paramètre est une adresse allouée par méthode d’une variable du type de données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0da89-112">This parameter is a method-allocated address of a variable of the property data type.</span></span> <span data-ttu-id="0da89-113">Lors du retour, cette variable utilise la valeur actuelle de la propriété demandée.</span><span class="sxs-lookup"><span data-stu-id="0da89-113">On return, this variable assumes the current value of the requested property.</span></span> <span data-ttu-id="0da89-114">L’appelant doit libérer la mémoire allouée de la variable lorsque la propriété n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0da89-114">The caller must release the allocated memory of the variable when the property is no longer required.</span></span>

<span data-ttu-id="0da89-115">Chaque **méthode \_ put** prend un paramètre unique comme entrée pour le type de données de la propriété correspondante.</span><span class="sxs-lookup"><span data-stu-id="0da89-115">Each **put\_** method takes a single parameter as input for the data type of the corresponding property.</span></span> <span data-ttu-id="0da89-116">Le paramètre contient une nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0da89-116">The parameter holds a new value of the property.</span></span>

<span data-ttu-id="0da89-117">L’exemple de code suivant montre l’appel des méthodes de propriété qui suivent la procédure habituelle pour appeler la fonction membre d’un objet.</span><span class="sxs-lookup"><span data-stu-id="0da89-117">The following code example shows the invocation of the property methods that follow the usual procedure to call the member function of an object.</span></span>


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



<span data-ttu-id="0da89-118">L’exemple de code suivant montre l’appel des méthodes de propriété dans les clients Automation, qui peuvent être légèrement différents.</span><span class="sxs-lookup"><span data-stu-id="0da89-118">The following code example shows the invocation of the property methods in automation clients, which can be somewhat different.</span></span> <span data-ttu-id="0da89-119">Par exemple, Visual Basic utilise la notation par points.</span><span class="sxs-lookup"><span data-stu-id="0da89-119">For example, Visual Basic uses dot notation.</span></span>


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



<span data-ttu-id="0da89-120">Tous les paramètres et types de retour doivent être de ceux définis par le type de données VARIANT.</span><span class="sxs-lookup"><span data-stu-id="0da89-120">All parameters and return types must be of those that the VARIANT data type defines.</span></span> <span data-ttu-id="0da89-121">Toutes les méthodes d’une interface double retournent une valeur HRESULT pour indiquer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="0da89-121">All methods on a dual interface return an HRESULT value to indicate success or failure.</span></span>

<span data-ttu-id="0da89-122">Pour plus d’informations sur l’obtention et la définition des propriétés sur les objets ADSI, consultez [cache des propriétés](property-cache-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0da89-122">For more information about getting and setting properties on ADSI objects, see [Property Cache](property-cache-interfaces.md).</span></span>

 

 