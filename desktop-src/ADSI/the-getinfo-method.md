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
ms.openlocfilehash: 534de8bd667ed33d562ac55b6a70452b6496d0a3d708c55a2cb0fee1a86a8a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838453"
---
# <a name="the-getinfo-method"></a>La méthode GetInfo

La méthode [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) charge toutes les valeurs d’attribut pour un objet ADSI dans le cache local à partir du service d’annuaire sous-jacent. La méthode [**IADs :: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) est utilisée pour charger des valeurs d’attribut spécifiques dans le cache local. Pour plus d’informations sur l’utilisation de la méthode **IADs :: GetInfoEx** , consultez [optimisation à l’aide de GetInfoEx](optimization-using-getinfoex.md).

ADSI crée un appel de [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implicite quand la méthode [**IADs :: obtenir**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs :: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) est appelée pour un attribut spécifique et qu’aucune valeur n’est trouvée dans le cache local. Quand **IADs :: GetInfo** a été appelé, un appel implicite n’est pas répété. Toutefois, si une valeur existe déjà dans le cache de propriétés, l’appel de la méthode **IADs :: obtenir** ou **IADs :: GETEX** sans appeler d’abord les **IAD :: GetInfo** récupère la valeur mise en cache plutôt que la valeur la plus récente dans le répertoire sous-jacent. Cela peut entraîner le remplacement des valeurs d’attribut mises à jour si le cache local a été modifié, mais que les valeurs n’ont pas été validées dans le service d’annuaire sous-jacent avec un appel à la méthode [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Pour éviter les problèmes de mise en cache, validez les modifications de valeur d’attribut en appelant **IADs :: setinfo** avant d’appeler **IADs :: GetInfo**.


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



Certains services d’annuaire ne retournent pas toutes les valeurs d’attribut d’un objet en réponse à un appel [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) . Dans ces cas, utilisez la méthode [**IADs :: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) pour charger ces valeurs dans le cache local.

 

 




