---
title: La méthode GetInfo
description: La méthode IADs GetInfo charge toutes les valeurs d’attribut d’un objet ADSI dans le cache local à partir du service d’annuaire sous-jacent.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- GetInfo ADSI, à l’aide d’IADs GetInfo
- ADSI ADSI, utilisation de, à l’aide de la méthode IADs GetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b374791e7fd7ff787c1b825827f410a9c15b551b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671114"
---
# <a name="the-getinfo-method"></a><span data-ttu-id="0d44c-105">La méthode GetInfo</span><span class="sxs-lookup"><span data-stu-id="0d44c-105">The GetInfo Method</span></span>

<span data-ttu-id="0d44c-106">La méthode [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) charge toutes les valeurs d’attribut pour un objet ADSI dans le cache local à partir du service d’annuaire sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0d44c-106">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method loads all of the attribute values for an ADSI object into the local cache from the underlying directory service.</span></span> <span data-ttu-id="0d44c-107">La méthode [**IADs :: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) est utilisée pour charger des valeurs d’attribut spécifiques dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="0d44c-107">The [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache.</span></span> <span data-ttu-id="0d44c-108">Pour plus d’informations sur l’utilisation de la méthode **IADs :: GetInfoEx** , consultez [optimisation à l’aide de GetInfoEx](optimization-using-getinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="0d44c-108">For more information about using the **IADs::GetInfoEx** method, see [Optimization Using GetInfoEx](optimization-using-getinfoex.md).</span></span>

<span data-ttu-id="0d44c-109">ADSI crée un appel de [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implicite quand la méthode [**IADs :: obtenir**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) est appelée pour un attribut spécifique et qu’aucune valeur n’est trouvée dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="0d44c-109">ADSI will make an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call when the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method is called for a specific attribute and no value is found in the local cache.</span></span> <span data-ttu-id="0d44c-110">Quand **IADs :: GetInfo** a été appelé, un appel implicite n’est pas répété.</span><span class="sxs-lookup"><span data-stu-id="0d44c-110">When **IADs::GetInfo** has been called, an implicit call is not repeated.</span></span> <span data-ttu-id="0d44c-111">Toutefois, si une valeur existe déjà dans le cache de propriétés, l’appel de la méthode **IADs :: obtenir** ou **IADs :: GETEX** sans appeler d’abord les **IAD :: GetInfo** récupère la valeur mise en cache plutôt que la valeur la plus récente dans le répertoire sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0d44c-111">If a value already exists in the property cache, however, calling the **IADs::Get** or **IADs::GetEx** method without first calling **IADs::GetInfo** will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="0d44c-112">Cela peut entraîner le remplacement des valeurs d’attribut mises à jour si le cache local a été modifié, mais que les valeurs n’ont pas été validées dans le service d’annuaire sous-jacent avec un appel à la méthode [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="0d44c-112">This can cause updated attribute values to be overwritten if the local cache has been modified but the values have not been committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="0d44c-113">Pour éviter les problèmes de mise en cache, validez les modifications de valeur d’attribut en appelant **IADs :: setinfo** avant d’appeler **IADs :: GetInfo**.</span><span class="sxs-lookup"><span data-stu-id="0d44c-113">To avoid caching problems, commit attribute value changes by calling **IADs::SetInfo** before calling **IADs::GetInfo**.</span></span>


```VB
Dim usr As IADs

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' This code example assumes that the property description has a single value in the directory.
' Be aware that this will IMPLICITLY call GetInfo because at this point GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's title is " + usr.Get("title")

' Change the attribute value in the local cache.
usr.Put "title", "Vice President"
Debug.Print "User's title is " + usr.Get("title")

' Call GetInfo, which will overwrite the updated value because SetInfo has not 
' been called.
usr.GetInfo
Debug.Print "User's title is " + usr.Get("title")
```



<span data-ttu-id="0d44c-114">Certains services d’annuaire ne retournent pas toutes les valeurs d’attribut d’un objet en réponse à un appel [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="0d44c-114">Some directory services do not return all attribute values for an object in response to a [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span> <span data-ttu-id="0d44c-115">Dans ces cas, utilisez la méthode [**IADs :: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) pour charger ces valeurs dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="0d44c-115">In these cases, use the [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method to load these values into the local cache.</span></span>

 

 




