---
title: Méthode GetEx
description: Certains attributs peuvent stocker une ou plusieurs valeurs.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI, utilisation de IADs GetEx
- ADSI ADSI, utilisation de, à l’aide de la méthode IADs GetEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508955"
---
# <a name="the-getex-method"></a><span data-ttu-id="6733a-105">Méthode GetEx</span><span class="sxs-lookup"><span data-stu-id="6733a-105">The GetEx Method</span></span>

<span data-ttu-id="6733a-106">Certains attributs peuvent stocker une ou plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="6733a-106">Some attributes can store one or more values.</span></span> <span data-ttu-id="6733a-107">Par exemple, l’attribut **OtherTelephone** d’un objet utilisateur dans Active Directory est une propriété qui peut avoir zéro, une ou plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="6733a-107">For example, the **otherTelephone** attribute of a user object in Active Directory is a property that can have zero, one, or many values.</span></span> <span data-ttu-id="6733a-108">Les attributs qui ont plusieurs valeurs sont appelés « attributs à valeurs multiples ».</span><span class="sxs-lookup"><span data-stu-id="6733a-108">Attributes that have multiple values are known as "multi-valued attributes".</span></span> <span data-ttu-id="6733a-109">Si la méthode [**IADs :: obten**](/windows/desktop/api/Iads/nf-iads-iads-get) est utilisée pour récupérer un attribut à valeurs multiples, les résultats doivent être traités différemment que si l’attribut a une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="6733a-109">If the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve a multi-valued attribute, the results must be processed differently than if the attribute has a single value.</span></span> <span data-ttu-id="6733a-110">Toutefois, les résultats fournis par la méthode [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) sont traités de la même manière, que l’attribut ait une ou plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="6733a-110">The results provided by the [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, however, are processed in the same manner, regardless if the attribute has a single or multiple values.</span></span> <span data-ttu-id="6733a-111">Dans les deux cas, la méthode **IADs :: GETEX** retourne les valeurs dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="6733a-111">In both cases, the **IADs::GetEx** method returns the values in an array.</span></span>

<span data-ttu-id="6733a-112">La méthode [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) récupère les propriétés du cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6733a-112">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method retrieves properties from the property cache.</span></span> <span data-ttu-id="6733a-113">Si la propriété spécifiée est introuvable dans le cache, **IADs :: GETEX** effectue un appel [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implicite.</span><span class="sxs-lookup"><span data-stu-id="6733a-113">If the specified property is not found in the cache, **IADs::GetEx** performs an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span>

<span data-ttu-id="6733a-114">La méthode [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) retourne un tableau de variants de variantes, quel que soit le nombre de valeurs retournées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="6733a-114">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method returns a variant array of variants regardless of the number of values returned from the server.</span></span> <span data-ttu-id="6733a-115">Cela est vrai même si l’attribut ne contient qu’une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="6733a-115">This is true even if the attribute only contains one value.</span></span>


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



<span data-ttu-id="6733a-116">La méthode [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) peut également être utilisée pour les attributs à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="6733a-116">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method can also be used for single-valued attributes.</span></span> <span data-ttu-id="6733a-117">Les résultats d’un attribut à valeur unique sont traités de la même façon que les résultats d’un attribut à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="6733a-117">The results of a single-valued attribute are processed the same as the results for a multi-valued attribute.</span></span>


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



<span data-ttu-id="6733a-118">Si aucune valeur n’est définie pour l’attribut, [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) retourne l’erreur « la propriété est introuvable dans le cache ».</span><span class="sxs-lookup"><span data-stu-id="6733a-118">If no value is set for the attribute, [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) returns the error "Property not found in cache".</span></span>

 

 




