---
title: Prise en charge de la liaison tardive
description: Lorsque la prise en charge de la liaison tardive est en place, chaque appel de fonction doit traverser l’interface ADSI IDispatch, avant d’être redirigé vers l’extension appropriée.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- ADSI d’extensions, prise en charge de la liaison tardive
- ADSI ADSI, exemple de code Visual Basic, prise en charge de la liaison tardive
- liaison Active Directory, prise en charge de la liaison tardive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e4dd1de0000d9edbe3e73cbc47b81d094d48c2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730309"
---
# <a name="late-binding-support"></a><span data-ttu-id="68e90-106">Prise en charge de la liaison tardive</span><span class="sxs-lookup"><span data-stu-id="68e90-106">Late Binding Support</span></span>

<span data-ttu-id="68e90-107">Lorsque la prise en charge de la liaison tardive est en place, chaque appel de fonction doit traverser l’interface ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , avant d’être redirigé vers l’extension appropriée.</span><span class="sxs-lookup"><span data-stu-id="68e90-107">When late binding support is in place, each function call must go through the ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface, before it is rerouted to the appropriate extension.</span></span>

<span data-ttu-id="68e90-108">Considérez l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="68e90-108">Consider the following code example.</span></span>


```C++
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
 
x.MyNewMethod( "\\srv\public")
x.MyProperty = "Hello World"
 
x.OtherMethod()
x.OtherProperty = 4362
 
Debug.Print x.LastName
```



<span data-ttu-id="68e90-109">Il n’y a pas d’appels explicites à la méthode **QueryInterface** pour accéder aux extensions.</span><span class="sxs-lookup"><span data-stu-id="68e90-109">There are no explicit calls to the **QueryInterface** method to get to the extensions.</span></span> <span data-ttu-id="68e90-110">Les extensions doivent rediriger leurs appels [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) vers l’interface ADSI **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="68e90-110">The extensions must reroute their [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) calls to the ADSI **IDispatch** interface.</span></span> <span data-ttu-id="68e90-111">L’interface ADSI prend la décision et résout tous les conflits qui se produisent, puis elle réachemine vers l’extension appropriée à l’aide d’une interface appelée [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="68e90-111">ADSI makes the decision and resolves any conflicts that occur, then it re-routes back to the appropriate extension using an interface called [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span> <span data-ttu-id="68e90-112">Par conséquent, toute extension qui prend en charge la liaison tardive doit implémenter **IADsExtension**.</span><span class="sxs-lookup"><span data-stu-id="68e90-112">Therefore, any extension that supports late binding must implement **IADsExtension**.</span></span>

 

 