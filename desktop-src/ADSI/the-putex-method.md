---
title: La méthode le
description: La méthode IADs visés par utilise le nom d’une propriété pour enregistrer une propriété avec une ou plusieurs valeurs dans le cache de propriétés.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- Biais d’ADSI, à propos de
- ADSI ADSI, exemple de code Visual Basic, à l’aide de la méthode biaisée
- propriétés ADSI, enregistrement d’une propriété à valeur unique ou à valeurs multiples dans le cache de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea698c2dd14f3ddf8f3ad97459fad598006db22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839125"
---
# <a name="the-putex-method"></a><span data-ttu-id="0b29b-106">La méthode le</span><span class="sxs-lookup"><span data-stu-id="0b29b-106">The PutEx Method</span></span>

<span data-ttu-id="0b29b-107">La méthode [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) utilise le nom d’une propriété pour enregistrer une propriété avec une ou plusieurs valeurs dans le cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0b29b-107">The [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the name of a property to save a property with single or multiple values into the property cache.</span></span> <span data-ttu-id="0b29b-108">Cela remplace toute valeur actuellement dans le cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0b29b-108">This overwrites any value currently in the property cache.</span></span> <span data-ttu-id="0b29b-109">Les valeurs du cache ne sont pas écrites dans le service d’annuaire sous-jacent jusqu’à ce qu’un [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) se produise.</span><span class="sxs-lookup"><span data-stu-id="0b29b-109">The values in the cache are not written to the underlying directory service until an [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) occurs.</span></span> <span data-ttu-id="0b29b-110">Le premier argument de la valeur de la propriété d’un paramètre de la propriété indique si vous souhaitez remplacer ou **Ajouter des valeurs** existantes à la propriété.</span><span class="sxs-lookup"><span data-stu-id="0b29b-110">The first argument of **PutEx** indicates whether you want to replace or add to any existing values for the property.</span></span> <span data-ttu-id="0b29b-111">Dans l’exemple suivant, toutes les valeurs existantes de l’attribut **Description** sont effacées dans le cache **lorsque l'** appel de la méthode respectent la valeur et effacent le serveur lorsque **setinfo** est appelé.</span><span class="sxs-lookup"><span data-stu-id="0b29b-111">In the following example, any existing values of the **description** attribute are erased in the cache when **PutEx** is called, and erased on the server when **SetInfo** is called.</span></span>


```VB
Dim x As IADs
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'----------------------------------------------
' Assume the otherHomePhoneNumber has the following values:
' 111-1111, 222-2222
'----------------------------------------------
x.PutEx ADS_PROPERTY_APPEND, "OtherhomePhone", Array("333-3333" )  
x.SetInfo              'Now the values are 111-1111,222-222,333-3333.
 
x.PutEx ADS_PROPERTY_DELETE, "OtherHomePhone", Array("111-1111", "222-2222")
x.SetInfo              'Now the values are 333-3333.
x.PutEx ADS_PROPERTY_UPDATE, "OtherHomePhone", Array("888-8888", "999-9999")
x.SetInfo              'Now the values are 888-8888,999-9999.
x.PutEx ADS_PROPERTY_CLEAR, "OtherHomePhone",  vbNull
x.SetInfo              'Now the property has no value.
```



 

 




