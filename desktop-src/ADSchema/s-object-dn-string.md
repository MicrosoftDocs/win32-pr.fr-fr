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
ms.openlocfilehash: 18222343a5c10b7231d174021c8d4238ba075b66b648d99a704f4e1d1d651e2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580249"
---
# <a name="objectdn-string-syntax"></a>Syntaxe Object (DN-String)

Chaîne d’octets qui contient une valeur de chaîne et un DN.



| Entrée | Valeur |
|--------------|------------------------------------------------------------------------------------|
| Name         | Object(DN-String)                                                                  |
| ID de syntaxe    | 2.5.5.14                                                                           |
| ID OM        | 127                                                                                |
| Type MAPI    | \-                                                                                 |
| Type ADS     | ADSTYPE \_ DN \_ avec \_ chaîne                                                          |
| Type de variante | \_distribution vt                                                                       |
| SDS, type     | Objet COM pouvant être casté en [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring). |



## <a name="remarks"></a>Remarques

Une valeur avec cette syntaxe a le format suivant :

``` syntax
S:<char count>:<string value>:<object DN>
```

où « &lt; nombre &gt; de caractères » est le nombre de caractères dans la &lt; chaîne « valeur de chaîne &gt; », et « &lt; objet DN &gt; » est un nom unique d’un objet dans Active Directory. Active Directory met à jour le DN si l’objet auquel il fait référence est déplacé ou renommé.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
