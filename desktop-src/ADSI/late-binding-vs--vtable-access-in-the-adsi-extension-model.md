---
title: Liaison tardive et accès vtable dans le modèle d’extension ADSI
description: Une interface double permet l’accès direct à toutes ses fonctions par le biais d’une interface de dispatch.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- liaison tardive et accès vtable dans le modèle d’extension ADSI ADSI
- ADSI d’extensions, liaison tardive ou accès vtable dans le modèle d’extension ADSI
- ADSI ADSI, exemple de code Visual Basic à l’aide de IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106513555"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a><span data-ttu-id="3b1d8-106">Liaison tardive et accès vtable dans le modèle d’extension ADSI</span><span class="sxs-lookup"><span data-stu-id="3b1d8-106">Late Binding vs. Vtable Access in the ADSI Extension Model</span></span>

<span data-ttu-id="3b1d8-107">Une interface double permet l’accès direct à toutes ses fonctions par le biais d’une interface de dispatch.</span><span class="sxs-lookup"><span data-stu-id="3b1d8-107">A dual interface enables direct vtable access to all its functions while a dispatch interface does not.</span></span> <span data-ttu-id="3b1d8-108">Un client C/C++ peut interroger un pointeur d’interface double et utiliser l’accès direct à la vtable pour appeler ses fonctions.</span><span class="sxs-lookup"><span data-stu-id="3b1d8-108">A C/C++ client can query for a dual interface pointer and use direct vtable access to invoke its functions.</span></span> <span data-ttu-id="3b1d8-109">Cela permet un accès plus rapide que l’appel de la fonction à l’aide des fonctions [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) et [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="3b1d8-109">This provides faster access than invoking the function using the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions.</span></span> <span data-ttu-id="3b1d8-110">Cela est particulièrement vrai dans le modèle d’extension, car toutes les interfaces doubles dans un objet d’extension doivent d’abord déléguer leurs fonctions **GetIDsOfNames** et **Invoke** à l’agrégateur (ADSI).</span><span class="sxs-lookup"><span data-stu-id="3b1d8-110">This is especially true in the extension model, because all dual interfaces in an extension object must delegate their **GetIDsOfNames** and **Invoke** functions back to the aggregator (ADSI) first.</span></span> <span data-ttu-id="3b1d8-111">L’agrégation doit alors effectuer des étapes internes supplémentaires pour identifier l’objet d’extension, éventuellement inclure l’agrégateur lui-même, la prise en charge de la fonction appelée et rediriger l’appel vers l’objet approprié.</span><span class="sxs-lookup"><span data-stu-id="3b1d8-111">The aggregator then must perform extra internal steps to identify which extension object, possibly including the aggregator itself, provides support for the function called and redirect the call to the appropriate object.</span></span>

<span data-ttu-id="3b1d8-112">Visual Basic appelle également une fonction à interface double à l’aide d’un accès direct à un vtable, s’il a un pointeur vers l’interface et un accès aux données de type à partir de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="3b1d8-112">Visual Basic also invokes a dual-interface function using direct access to a vtable, if it has a pointer to the interface and access to type data from the type library.</span></span> <span data-ttu-id="3b1d8-113">Les clients ADSI écrits en Visual Basic peuvent spécifier un pointeur vers une interface double, par exemple [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitement, et ainsi activer l’accès vtable aux fonctions dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="3b1d8-113">ADSI clients written in Visual Basic can specify a pointer to a dual interface, for example, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitly, and thus enable vtable access to functions in the interface.</span></span>


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



<span data-ttu-id="3b1d8-114">Comme une interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ne prend pas en charge l’accès vtable, cet exemple ne s’applique pas.</span><span class="sxs-lookup"><span data-stu-id="3b1d8-114">Because an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface does not support vtable access, this example does not apply.</span></span> <span data-ttu-id="3b1d8-115">Autrement dit, une fonction de répartition est toujours appelée par le biais des fonctions [**IDispatch :: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) et [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) uniquement.</span><span class="sxs-lookup"><span data-stu-id="3b1d8-115">That is, a dispatch function is always invoked through the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions only.</span></span>

<span data-ttu-id="3b1d8-116">Les versions actuelles de VBScript et JScript ne prennent pas non plus en charge l’accès vtable.</span><span class="sxs-lookup"><span data-stu-id="3b1d8-116">Current releases of VBScript and JScript also do not support vtable access.</span></span> <span data-ttu-id="3b1d8-117">Par conséquent, une interface double dans un environnement VBScript ou JScript fonctionne comme une interface de dispatch.</span><span class="sxs-lookup"><span data-stu-id="3b1d8-117">Therefore, a dual interface in a VBScript or JScript environment performs like a dispatch interface.</span></span>

 

 