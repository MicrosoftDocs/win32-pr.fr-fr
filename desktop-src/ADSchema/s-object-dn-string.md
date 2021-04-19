---
title: Syntaxe Object (DN-String)
description: Chaîne d’octets qui contient une valeur de chaîne et un DN.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Syntaxe d’objet (DN-String) schéma Active Directory
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514266"
---
# <a name="objectdn-string-syntax"></a>Syntaxe Object (DN-String)

Chaîne d’octets qui contient une valeur de chaîne et un DN.



| Entrée | Valeur |
|--------------|------------------------------------------------------------------------------------|
| Nom         | Object(DN-String)                                                                  |
| ID de syntaxe    | 2.5.5.14                                                                           |
| ID OM        | 127                                                                                |
| Type MAPI    | \-                                                                                 |
| Type ADS     | ADSTYPE \_ DN \_ avec \_ chaîne                                                          |
| Type de variante | \_distribution vt                                                                       |
| SDS, type     | Objet COM pouvant être casté en [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring). |



## <a name="remarks"></a>Notes

Une valeur avec cette syntaxe a le format suivant :

``` syntax
S:<char count>:<string value>:<object DN>
```

où « &lt; nombre &gt; de caractères » est le nombre de caractères dans la &lt; chaîne « valeur de chaîne &gt; », et « &lt; objet DN &gt; » est un nom unique d’un objet dans Active Directory. Active Directory met à jour le DN si l’objet auquel il fait référence est déplacé ou renommé.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
