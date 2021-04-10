---
title: Optimisation à l’aide de GetInfoEx
description: Utilisé pour charger des valeurs d’attribut spécifiques dans le cache local à partir du service d’annuaire sous-jacent.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Optimisation à l’aide d’ADSI GetInfoEx
- GetInfoEx ADSI, optimisation à l’aide d’IADs GetInfoEx
- ADSI ADSI, utilisation, optimisation à l’aide de la méthode IADs GetInfoEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b522093fff00700cf35b864edde2a6ae7f8f9922
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316452"
---
# <a name="optimization-using-getinfoex"></a><span data-ttu-id="76f43-106">Optimisation à l’aide de GetInfoEx</span><span class="sxs-lookup"><span data-stu-id="76f43-106">Optimization Using GetInfoEx</span></span>

<span data-ttu-id="76f43-107">La méthode [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) est utilisée pour charger des valeurs d’attribut spécifiques dans le cache local à partir du service d’annuaire sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="76f43-107">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache from the underlying directory service.</span></span> <span data-ttu-id="76f43-108">Cette méthode charge uniquement les valeurs d’attribut spécifiées dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="76f43-108">This method only loads the specified attribute values into the local cache.</span></span> <span data-ttu-id="76f43-109">La méthode [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) permet de charger toutes les valeurs d’attribut dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="76f43-109">The [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is used to load all attribute values into the local cache.</span></span>

<span data-ttu-id="76f43-110">La méthode [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) obtient des valeurs actuelles spécifiques pour les propriétés d’un objet Active Directory à partir du magasin d’annuaires sous-jacent, en actualisant les valeurs mises en cache.</span><span class="sxs-lookup"><span data-stu-id="76f43-110">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method gets specific current values for the properties of an Active Directory object from the underlying directory store, refreshing the cached values.</span></span>

<span data-ttu-id="76f43-111">Toutefois, si une valeur existe déjà dans le cache de propriétés, l’appel de la méthode [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) sans appeler d’abord les [**IAD. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) pour cet attribut récupérera la valeur mise en cache plutôt que la valeur la plus récente de l’annuaire sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="76f43-111">If a value already exists in the property cache, however, calling the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method without first calling [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) for that attribute will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="76f43-112">Cela peut entraîner le remplacement des valeurs d’attribut mises à jour si le cache local a été modifié, mais que les valeurs n’ont pas été validées dans le service d’annuaire sous-jacent avec un appel à la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="76f43-112">This can cause updated attribute values to be overwritten if the local cache has been modified, but the values have not been committed to the underlying directory service with a call to the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="76f43-113">La méthode suggérée pour éviter les problèmes de mise en cache consiste à toujours valider les modifications de valeur d’attribut en appelant **IADs. setinfo** avant d’appeler [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span><span class="sxs-lookup"><span data-stu-id="76f43-113">The suggested method for avoiding caching problems is to always commit attribute value changes by calling **IADs.SetInfo** before calling [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span></span>


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a><span data-ttu-id="76f43-114">Récupération des attributs construits Active Directory</span><span class="sxs-lookup"><span data-stu-id="76f43-114">Retrieving Active Directory Constructed Attributes</span></span>

<span data-ttu-id="76f43-115">Dans Active Directory, la plupart des attributs construits sont récupérés et mis en cache quand la méthode [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) est appelée ([**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) effectue un appel de **IADs. GetInfo** implicite si le cache est vide).</span><span class="sxs-lookup"><span data-stu-id="76f43-115">In Active Directory, most of the constructed attributes are retrieved and cached when the [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called ([**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) performs an implicit **IADs.GetInfo** call if the cache is empty).</span></span> <span data-ttu-id="76f43-116">Certains attributs construits, toutefois, ne sont pas automatiquement récupérés et mis en cache et nécessitent donc que la méthode [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) soit appelée explicitement pour les récupérer.</span><span class="sxs-lookup"><span data-stu-id="76f43-116">Some constructed attributes, however, are not automatically retrieved and cached and, therefore, require that the [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method be called explicitly to retrieve them.</span></span> <span data-ttu-id="76f43-117">Par exemple, dans Active Directory, l’attribut [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) n’est pas récupéré lorsque la méthode **IADs. GetInfo** est appelée et les **IAD. obtenir** renvoient la **\_ propriété E ADS \_ \_ \_ introuvable**.</span><span class="sxs-lookup"><span data-stu-id="76f43-117">For example, in Active Directory, the [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) attribute is not retrieved when the **IADs.GetInfo** method is called and **IADs.Get** will return **E\_ADS\_PROPERTY\_NOT\_FOUND**.</span></span> <span data-ttu-id="76f43-118">La méthode **IADs. GetInfoEx** doit être appelée pour récupérer l’attribut **canonicalName** .</span><span class="sxs-lookup"><span data-stu-id="76f43-118">The **IADs.GetInfoEx** method must be called to retrieve the **canonicalName** attribute.</span></span> <span data-ttu-id="76f43-119">Ces mêmes attributs construits ne seront pas non plus extraits à l’aide de l’interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) pour énumérer les attributs.</span><span class="sxs-lookup"><span data-stu-id="76f43-119">These same constructed attributes will also not be retrieved using the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface to enumerate the attributes.</span></span>

<span data-ttu-id="76f43-120">Pour plus d’informations et pour obtenir un exemple de code qui montre comment récupérer toutes les valeurs d’attribut, consultez l' [exemple de code pour la lecture d’un attribut construit](example-code-for-reading-a-constructed-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="76f43-120">For more information and a code example that shows how to retrieve all attribute values, see [Example Code for Reading a Constructed Attribute](example-code-for-reading-a-constructed-attribute.md).</span></span>

 

 