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
# <a name="accessing-attributes-with-adsi"></a>Accès aux attributs avec ADSI

Les méthodes [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) sont utilisées pour récupérer des valeurs d’attribut nommées. Les deux méthodes retournent une valeur de [**type Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . Ces méthodes ne sont disponibles que pour les répertoires qui prennent en charge un schéma. Lors de l’accès aux objets d’un répertoire sans schéma, les interfaces [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) et [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) doivent être utilisées pour manipuler des valeurs d’attribut.

Les méthodes [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) retournent un [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) qui peut être ou non un tableau **Variant** en fonction du nombre de valeurs retournées par le serveur. Par exemple, si une seule valeur est retournée par le serveur, qu’il s’agisse d’un attribut à valeur unique ou à valeurs multiples, la méthode retourne un **Variant** unique. À l’inverse, si plusieurs valeurs sont retournées, un tableau **Variant** est retourné. Si un **tableau variant** est retourné, le **membre VT** de la structure **Variant** contient les indicateurs **VT \_ Variant/vbVariant** et **VT \_ Array/VBArray** .

Les méthodes [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) peuvent également retourner un objet com à l’aide de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Dans ce cas, le membre **VT** de la structure [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contient l’indicateur **VT \_ Dispatch/vbObject** . Pour accéder à l’objet COM, appelez la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’interface **IDispatch** pour obtenir l’interface souhaitée.

Un autre type de données retourné par les méthodes [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) est données binaires. Dans ce cas, les données sont fournies sous la forme d’un tableau d’octets contigu et le membre **VT** de la structure [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contient les indicateurs **VT \_ UI1/vbByte** et **VT \_ Array/VBArray** .

> [!Note]  
> Microsoft Visual Basic, l’édition de script ne prend en charge que les tableaux [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) et **Variant** . Pour cette raison, VBScript ne peut pas être utilisé pour lire les valeurs de propriété binaires.

 

De nombreuses interfaces ADSI définissent des propriétés spécifiques à l’interface. Par exemple, l’interface [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) définit la propriété [**location**](iadscomputer-property-methods.md) . Ces propriétés définies par l’interface peuvent contenir des données qui sont identiques à l’un des attributs nommés, mais les propriétés sont spécifiques au type d’objet auquel l’interface fait référence. Dans les langages qui prennent en charge l’automatisation, ces propriétés définies par l’interface sont accessibles à l’aide de la notation par points, comme indiqué dans l’exemple de code suivant.

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment accéder à la propriété ADsPath de l’interface IADs.


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



Dans les langages non-Automation, les méthodes d’accès à la propriété doivent être utilisées pour accéder aux propriétés définies par l’interface. Par exemple, la méthode [**IADsComputer :: obtenir l' \_ emplacement**](iadscomputer-property-methods.md) est utilisée pour récupérer la propriété **IADsComputer. Location** .

L’exemple de code C++ suivant montre comment utiliser la méthode d’accès à la propriété en C++ pour récupérer l’ADsPath d’un utilisateur.


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



Pour plus d’informations sur l’accès aux attributs avec ADSI, consultez :

-   [Méthode d’extraction](the-get-method.md)
-   [Méthode GetEx](the-getex-method.md)
-   [La méthode GetInfo](the-getinfo-method.md)
-   [Optimisation à l’aide de GetInfoEx](optimization-using-getinfoex.md)
-   [Accès aux attributs avec l’interface IDirectoryObject](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [Exemple de code pour la lecture d’attributs](example-code-for-reading-attributes.md)

 

 