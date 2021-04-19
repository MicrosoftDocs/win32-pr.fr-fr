---
description: Un objet SWbemNamedValueSet est une collection d’objets SWbemNamedValue.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Objet SWbemNamedValueSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541195"
---
# <a name="swbemnamedvalueset-object"></a><span data-ttu-id="c0f89-103">Objet SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="c0f89-103">SWbemNamedValueSet object</span></span>

<span data-ttu-id="c0f89-104">Un objet **SWbemNamedValueSet** est une collection d’objets [**SWbemNamedValue**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="c0f89-104">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) objects.</span></span> <span data-ttu-id="c0f89-105">Les méthodes et les propriétés de **SWbemNamedValueSet** sont principalement utilisées pour envoyer des informations supplémentaires aux fournisseurs lors de l’envoi de certains appels à WMI.</span><span class="sxs-lookup"><span data-stu-id="c0f89-105">The methods and properties of **SWbemNamedValueSet** are used principally to send more information to providers when submitting certain calls to WMI.</span></span> <span data-ttu-id="c0f89-106">Tous les appels dans [**SWbemServices**](swbemservices.md)et certains appels dans [**SWbemObject**](swbemobject.md)prennent un paramètre facultatif qui est un objet de ce type.</span><span class="sxs-lookup"><span data-stu-id="c0f89-106">All calls in [**SWbemServices**](swbemservices.md), and some calls in [**SWbemObject**](swbemobject.md), take an optional parameter that is an object of this type.</span></span> <span data-ttu-id="c0f89-107">Un client peut ajouter des informations à un objet **SWbemNamedValueSet** et envoyer l’objet **SWbemNamedValueSet** avec l’appel comme l’un des paramètres.</span><span class="sxs-lookup"><span data-stu-id="c0f89-107">A client can add information to an **SWbemNamedValueSet** object, and send the **SWbemNamedValueSet** object with the call as one of the parameters.</span></span> <span data-ttu-id="c0f89-108">Cet objet peut être créé par l’appel VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="c0f89-108">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="c0f89-109">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="c0f89-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

> [!Note]  
> <span data-ttu-id="c0f89-110">Important-si possible, n’utilisez pas ce mécanisme, car il peut rompre le modèle d’accès uniforme qui est la base de WMI.</span><span class="sxs-lookup"><span data-stu-id="c0f89-110">Important - If possible, do not use this mechanism because it can break the uniform access model that is the basis of WMI.</span></span> <span data-ttu-id="c0f89-111">Si un fournisseur utilise ce mécanisme, il est important que ce mécanisme soit utilisé aussi avec modération que possible.</span><span class="sxs-lookup"><span data-stu-id="c0f89-111">If a provider does use this mechanism, it is important that this mechanism is used as sparingly as possible.</span></span> <span data-ttu-id="c0f89-112">Si un fournisseur a besoin d’une grande quantité d’informations de contexte hautement spécifiques pour répondre à une demande, tous les clients doivent être codés pour fournir ces informations.</span><span class="sxs-lookup"><span data-stu-id="c0f89-112">If a provider requires a large amount of highly specific context information to respond to a request, all clients must be coded to provide this information.</span></span> <span data-ttu-id="c0f89-113">Ce mécanisme vous permet d’accéder à de tels fournisseurs, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c0f89-113">This mechanism allows you to access such providers, if necessary.</span></span>

 

<span data-ttu-id="c0f89-114">Un objet **SWbemNamedValueSet** est une collection d’éléments [**SWbemNamedValue**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="c0f89-114">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) elements.</span></span> <span data-ttu-id="c0f89-115">Ces éléments sont ajoutés à la collection à l’aide de la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .</span><span class="sxs-lookup"><span data-stu-id="c0f89-115">These items are added to the collection using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span> <span data-ttu-id="c0f89-116">Elles sont supprimées à l’aide de la méthode [**SWbemNamedValueSet. Remove**](swbemnamedvalueset-remove.md) et récupérées à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="c0f89-116">They are removed using the [**SWbemNamedValueSet.Remove**](swbemnamedvalueset-remove.md) method and retrieved using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="c0f89-117">Vous pouvez accéder aux méthodes pour remplir toutes les informations de contexte requises par un fournisseur dynamique.</span><span class="sxs-lookup"><span data-stu-id="c0f89-117">You can access the methods to fill in any context information that is required by a dynamic provider.</span></span> <span data-ttu-id="c0f89-118">Après avoir appelé l’une des méthodes [**SWbemServices**](swbemservices.md) , vous pouvez réutiliser l’objet **SWbemNamedValueSet** pour un autre appel.</span><span class="sxs-lookup"><span data-stu-id="c0f89-118">After you call one of the [**SWbemServices**](swbemservices.md) methods, you can reuse the **SWbemNamedValueSet** object for another call.</span></span>

<span data-ttu-id="c0f89-119">Le fournisseur sous-jacent détermine les informations contenues dans un objet **SWbemNamedValueSet** .</span><span class="sxs-lookup"><span data-stu-id="c0f89-119">The underlying provider determines the information that is contained in an **SWbemNamedValueSet** object.</span></span> <span data-ttu-id="c0f89-120">WMI n’utilise pas les informations, mais les transfère simplement au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c0f89-120">WMI makes no use of the information, but simply forwards it to the provider.</span></span> <span data-ttu-id="c0f89-121">Les fournisseurs doivent publier les informations de contexte dont ils ont besoin pour traiter les demandes.</span><span class="sxs-lookup"><span data-stu-id="c0f89-121">Providers must publish the context information they require to service requests.</span></span>

## <a name="members"></a><span data-ttu-id="c0f89-122">Membres</span><span class="sxs-lookup"><span data-stu-id="c0f89-122">Members</span></span>

<span data-ttu-id="c0f89-123">L’objet **SWbemNamedValueSet** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c0f89-123">The **SWbemNamedValueSet** object has these types of members:</span></span>

-   [<span data-ttu-id="c0f89-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c0f89-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="c0f89-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0f89-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c0f89-126">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c0f89-126">Methods</span></span>

<span data-ttu-id="c0f89-127">L’objet **SWbemNamedValueSet** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c0f89-127">The **SWbemNamedValueSet** object has these methods.</span></span>



| <span data-ttu-id="c0f89-128">Méthode</span><span class="sxs-lookup"><span data-stu-id="c0f89-128">Method</span></span>                                            | <span data-ttu-id="c0f89-129">Description</span><span class="sxs-lookup"><span data-stu-id="c0f89-129">Description</span></span>                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0f89-130">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="c0f89-130">**Add**</span></span>](swbemnamedvalueset-add.md)             | <span data-ttu-id="c0f89-131">Ajoute un objet [**SWbemNamedValue**](swbemnamedvalue.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="c0f89-131">Adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span><br/>                                                  |
| [<span data-ttu-id="c0f89-132">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="c0f89-132">**Clone**</span></span>](swbemnamedvalueset-clone.md)         | <span data-ttu-id="c0f89-133">Effectue une copie de cette collection **SWbemNamedValueSet** .</span><span class="sxs-lookup"><span data-stu-id="c0f89-133">Makes a copy of this **SWbemNamedValueSet** collection.</span></span><br/>                                                                       |
| [<span data-ttu-id="c0f89-134">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="c0f89-134">**DeleteAll**</span></span>](swbemnamedvalueset-deleteall.md) | <span data-ttu-id="c0f89-135">Supprime tous les éléments de la collection, ce qui rend l’objet **SWbemNamedValueSet** vide.</span><span class="sxs-lookup"><span data-stu-id="c0f89-135">Removes all items from the collection, making the **SWbemNamedValueSet** object empty.</span></span><br/>                                        |
| [<span data-ttu-id="c0f89-136">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c0f89-136">**Item**</span></span>](swbemnamedvalueset-item.md)           | <span data-ttu-id="c0f89-137">Récupère un objet [**SWbemNamedValue**](swbemnamedvalue.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="c0f89-137">Retrieves an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span> <span data-ttu-id="c0f89-138">Il s’agit de la méthode par défaut de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c0f89-138">This is the default method of the object.</span></span><br/> |
| [<span data-ttu-id="c0f89-139">**Installez**</span><span class="sxs-lookup"><span data-stu-id="c0f89-139">**Remove**</span></span>](swbemnamedvalueset-remove.md)       | <span data-ttu-id="c0f89-140">Supprime un objet [**SWbemNamedValue**](swbemnamedvalue.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="c0f89-140">Removes an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span><br/>                                             |



 

### <a name="properties"></a><span data-ttu-id="c0f89-141">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c0f89-141">Properties</span></span>

<span data-ttu-id="c0f89-142">L’objet **SWbemNamedValueSet** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c0f89-142">The **SWbemNamedValueSet** object has these properties.</span></span>



| <span data-ttu-id="c0f89-143">Propriété</span><span class="sxs-lookup"><span data-stu-id="c0f89-143">Property</span></span>                                             | <span data-ttu-id="c0f89-144">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c0f89-144">Access type</span></span>          | <span data-ttu-id="c0f89-145">Description</span><span class="sxs-lookup"><span data-stu-id="c0f89-145">Description</span></span>                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="c0f89-146">**Saut**</span><span class="sxs-lookup"><span data-stu-id="c0f89-146">**Count**</span></span>](swbemnamedvalueset-count.md)<br/> | <span data-ttu-id="c0f89-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c0f89-147">Read-only</span></span><br/> | <span data-ttu-id="c0f89-148">Nombre d’éléments dans la collection</span><span class="sxs-lookup"><span data-stu-id="c0f89-148">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="c0f89-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="c0f89-149">Examples</span></span>

<span data-ttu-id="c0f89-150">L’exemple VBScript suivant illustre la manipulation des jeux de valeurs nommées, dans le cas où la valeur nommée est un type tableau.</span><span class="sxs-lookup"><span data-stu-id="c0f89-150">The following VBScript sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="c0f89-151">L’exemple perl suivant illustre la manipulation des jeux de valeurs nommées, dans le cas où la valeur nommée est un type tableau.</span><span class="sxs-lookup"><span data-stu-id="c0f89-151">The following Perl sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="c0f89-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0f89-152">Requirements</span></span>



| <span data-ttu-id="c0f89-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0f89-153">Requirement</span></span> | <span data-ttu-id="c0f89-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0f89-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f89-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0f89-155">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f89-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0f89-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0f89-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0f89-157">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f89-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0f89-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0f89-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0f89-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0f89-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0f89-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0f89-161">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c0f89-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0f89-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0f89-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0f89-163">DLL</span><span class="sxs-lookup"><span data-stu-id="c0f89-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0f89-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0f89-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c0f89-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="c0f89-165">CLSID</span></span><br/>                    | <span data-ttu-id="c0f89-166">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="c0f89-166">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="c0f89-167">IID</span><span class="sxs-lookup"><span data-stu-id="c0f89-167">IID</span></span><br/>                      | <span data-ttu-id="c0f89-168">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="c0f89-168">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="c0f89-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0f89-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f89-170">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="c0f89-170">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




