---
title: Accès aux attributs avec ADSI
description: Les méthodes IADs. obten et IADs. GetEx sont utilisées pour récupérer des valeurs d’attribut nommées.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Attributs, accès avec ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ee6990483b45e335bb6b830cef85e482f30e00
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510706"
---
# <a name="accessing-attributes-with-adsi"></a><span data-ttu-id="32ada-104">Accès aux attributs avec ADSI</span><span class="sxs-lookup"><span data-stu-id="32ada-104">Accessing Attributes with ADSI</span></span>

<span data-ttu-id="32ada-105">Les méthodes [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) sont utilisées pour récupérer des valeurs d’attribut nommées.</span><span class="sxs-lookup"><span data-stu-id="32ada-105">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods are used to retrieve named attribute values.</span></span> <span data-ttu-id="32ada-106">Les deux méthodes retournent une valeur de [**type Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="32ada-106">Both methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) value.</span></span> <span data-ttu-id="32ada-107">Ces méthodes ne sont disponibles que pour les répertoires qui prennent en charge un schéma.</span><span class="sxs-lookup"><span data-stu-id="32ada-107">These methods are available only for directories that support a schema.</span></span> <span data-ttu-id="32ada-108">Lors de l’accès aux objets d’un répertoire sans schéma, les interfaces [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) et [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) doivent être utilisées pour manipuler des valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="32ada-108">When accessing objects in a directory without a schema, the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interfaces must be used to manipulate attribute values.</span></span>

<span data-ttu-id="32ada-109">Les méthodes [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) retournent un [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) qui peut être ou non un tableau **Variant** en fonction du nombre de valeurs retournées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="32ada-109">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) which may, or may not, be a **VARIANT** array depending on the number of values returned by the server.</span></span> <span data-ttu-id="32ada-110">Par exemple, si une seule valeur est retournée par le serveur, qu’il s’agisse d’un attribut à valeur unique ou à valeurs multiples, la méthode retourne un **Variant** unique.</span><span class="sxs-lookup"><span data-stu-id="32ada-110">For example, if only one value is returned from the server, regardless of whether it is a single or multi-valued attribute, the method returns a single **VARIANT**.</span></span> <span data-ttu-id="32ada-111">À l’inverse, si plusieurs valeurs sont retournées, un tableau **Variant** est retourné.</span><span class="sxs-lookup"><span data-stu-id="32ada-111">Conversely, if multiple values are returned, a **VARIANT** array is returned.</span></span> <span data-ttu-id="32ada-112">Si un **tableau variant** est retourné, le **membre VT** de la structure **Variant** contient les indicateurs **VT \_ Variant/vbVariant** et **VT \_ Array/VBArray** .</span><span class="sxs-lookup"><span data-stu-id="32ada-112">If a **VARIANT** array is returned, the **vt** member of the **VARIANT** structure contains the **VT\_VARIANT/vbVariant** and **VT\_ARRAY/vbArray** flags.</span></span>

<span data-ttu-id="32ada-113">Les méthodes [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) peuvent également retourner un objet com à l’aide de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="32ada-113">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods can also return a COM object using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="32ada-114">Dans ce cas, le membre **VT** de la structure [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contient l’indicateur **VT \_ Dispatch/vbObject** .</span><span class="sxs-lookup"><span data-stu-id="32ada-114">In this case, the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure contains the **VT\_DISPATCH/vbObject** flag.</span></span> <span data-ttu-id="32ada-115">Pour accéder à l’objet COM, appelez la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’interface **IDispatch** pour obtenir l’interface souhaitée.</span><span class="sxs-lookup"><span data-stu-id="32ada-115">To access the COM object, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the **IDispatch** interface to obtain the desired interface.</span></span>

<span data-ttu-id="32ada-116">Un autre type de données retourné par les méthodes [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) est données binaires.</span><span class="sxs-lookup"><span data-stu-id="32ada-116">Another data type returned by the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods is binary data.</span></span> <span data-ttu-id="32ada-117">Dans ce cas, les données sont fournies sous la forme d’un tableau d’octets contigu et le membre **VT** de la structure [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contient les indicateurs **VT \_ UI1/vbByte** et **VT \_ Array/VBArray** .</span><span class="sxs-lookup"><span data-stu-id="32ada-117">In this case, the data is supplied as a contiguous array of bytes and the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure will contain the **VT\_UI1/vbByte** and **VT\_ARRAY/vbArray** flags.</span></span>

> [!Note]  
> <span data-ttu-id="32ada-118">Microsoft Visual Basic, l’édition de script ne prend en charge que les tableaux [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) et **Variant** .</span><span class="sxs-lookup"><span data-stu-id="32ada-118">Microsoft Visual Basic, Scripting Edition only supports [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) and **VARIANT** arrays.</span></span> <span data-ttu-id="32ada-119">Pour cette raison, VBScript ne peut pas être utilisé pour lire les valeurs de propriété binaires.</span><span class="sxs-lookup"><span data-stu-id="32ada-119">Because of this, VBScript cannot be used to read binary property values.</span></span>

 

<span data-ttu-id="32ada-120">De nombreuses interfaces ADSI définissent des propriétés spécifiques à l’interface.</span><span class="sxs-lookup"><span data-stu-id="32ada-120">Many ADSI interfaces define interface-specific properties.</span></span> <span data-ttu-id="32ada-121">Par exemple, l’interface [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) définit la propriété [**location**](iadscomputer-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="32ada-121">For example, the [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface defines the [**Location**](iadscomputer-property-methods.md) property.</span></span> <span data-ttu-id="32ada-122">Ces propriétés définies par l’interface peuvent contenir des données qui sont identiques à l’un des attributs nommés, mais les propriétés sont spécifiques au type d’objet auquel l’interface fait référence.</span><span class="sxs-lookup"><span data-stu-id="32ada-122">These interface-defined properties may contain data that is identical to one of the named attributes, but the properties are specific to the type of object the interface refers to.</span></span> <span data-ttu-id="32ada-123">Dans les langages qui prennent en charge l’automatisation, ces propriétés définies par l’interface sont accessibles à l’aide de la notation par points, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="32ada-123">In languages that support automation, these interface-defined properties can be accessed using the dot notation as shown in the following code example.</span></span>

## <a name="examples"></a><span data-ttu-id="32ada-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="32ada-124">Examples</span></span>

<span data-ttu-id="32ada-125">L’exemple de code suivant montre comment accéder à la propriété ADsPath de l’interface IADs.</span><span class="sxs-lookup"><span data-stu-id="32ada-125">The following code example shows how to access the ADsPath property on the IADs interface.</span></span>


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



<span data-ttu-id="32ada-126">Dans les langages non-Automation, les méthodes d’accès à la propriété doivent être utilisées pour accéder aux propriétés définies par l’interface.</span><span class="sxs-lookup"><span data-stu-id="32ada-126">In non-automation languages, the property access methods must be used to access the interface-defined properties.</span></span> <span data-ttu-id="32ada-127">Par exemple, la méthode [**IADsComputer :: obtenir l' \_ emplacement**](iadscomputer-property-methods.md) est utilisée pour récupérer la propriété **IADsComputer. Location** .</span><span class="sxs-lookup"><span data-stu-id="32ada-127">For example, the [**IADsComputer::get\_Location**](iadscomputer-property-methods.md) method is used to retrieve the **IADsComputer.Location** property.</span></span>

<span data-ttu-id="32ada-128">L’exemple de code C++ suivant montre comment utiliser la méthode d’accès à la propriété en C++ pour récupérer l’ADsPath d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32ada-128">The following C++ code example demonstrates how to use the property access method in C++ to retrieve the ADsPath of a user.</span></span>


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



<span data-ttu-id="32ada-129">Pour plus d’informations sur l’accès aux attributs avec ADSI, consultez :</span><span class="sxs-lookup"><span data-stu-id="32ada-129">For more information about accessing attributes with ADSI, see:</span></span>

-   [<span data-ttu-id="32ada-130">Méthode d’extraction</span><span class="sxs-lookup"><span data-stu-id="32ada-130">The Get Method</span></span>](the-get-method.md)
-   [<span data-ttu-id="32ada-131">Méthode GetEx</span><span class="sxs-lookup"><span data-stu-id="32ada-131">The GetEx Method</span></span>](the-getex-method.md)
-   [<span data-ttu-id="32ada-132">La méthode GetInfo</span><span class="sxs-lookup"><span data-stu-id="32ada-132">The GetInfo Method</span></span>](the-getinfo-method.md)
-   [<span data-ttu-id="32ada-133">Optimisation à l’aide de GetInfoEx</span><span class="sxs-lookup"><span data-stu-id="32ada-133">Optimization Using GetInfoEx</span></span>](optimization-using-getinfoex.md)
-   [<span data-ttu-id="32ada-134">Accès aux attributs avec l’interface IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="32ada-134">Accessing Attributes with the IDirectoryObject Interface</span></span>](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [<span data-ttu-id="32ada-135">Exemple de code pour la lecture d’attributs</span><span class="sxs-lookup"><span data-stu-id="32ada-135">Example Code for Reading Attributes</span></span>](example-code-for-reading-attributes.md)

 

 