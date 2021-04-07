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
# <a name="the-putex-method"></a>La méthode le

La méthode [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) utilise le nom d’une propriété pour enregistrer une propriété avec une ou plusieurs valeurs dans le cache de propriétés. Cela remplace toute valeur actuellement dans le cache de propriétés. Les valeurs du cache ne sont pas écrites dans le service d’annuaire sous-jacent jusqu’à ce qu’un [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) se produise. Le premier argument de la valeur de la propriété d’un paramètre de la propriété indique si vous souhaitez remplacer ou **Ajouter des valeurs** existantes à la propriété. Dans l’exemple suivant, toutes les valeurs existantes de l’attribut **Description** sont effacées dans le cache **lorsque l'** appel de la méthode respectent la valeur et effacent le serveur lorsque **setinfo** est appelé.


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



 

 




