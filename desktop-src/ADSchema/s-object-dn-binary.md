---
title: Syntaxe Object (DN-Binary)
description: Chaîne d’octets qui contient une valeur binaire et un nom unique (DN).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Syntaxe de l’objet (DN-Binary) AD Schema
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106702"
---
# <a name="objectdn-binary-syntax"></a>Syntaxe Object (DN-Binary)

Chaîne d’octets qui contient une valeur binaire et un nom unique (DN).



| Entrée | Valeur |
|--------------|------------------------------------------------------------------------------------|
| Nom         | Object(DN-Binary)                                                                  |
| ID de syntaxe    | 2.5.5.7                                                                            |
| ID OM        | 127                                                                                |
| Type MAPI    | TSTRING                                                                            |
| Type ADS     | ADSTYPE \_ DN \_ avec \_ binaire                                                          |
| Type de variante | \_distribution vt                                                                       |
| SDS, type     | Objet COM pouvant être casté en [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary). |



## <a name="remarks"></a>Notes

Une valeur avec cette syntaxe a le format suivant :

``` syntax
B:<char count>:<binary value>:<object DN>
```

où « &lt; nombre &gt; de caractères » est le nombre de chiffres hexadécimaux dans « &lt; valeur binaire &gt; », « &lt; valeur binaire &gt; » est la représentation hexadécimale de la valeur binaire, et « &lt; objet DN &gt; » est un nom unique. Active Directory met automatiquement à jour le DN si l’objet auquel il fait référence est déplacé ou renommé. Pour plus d’informations et pour obtenir un exemple de code qui utilise cette syntaxe, consultez [activation de la liaison avec renommage sécurisé avec la propriété otherWellKnownObjects](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
