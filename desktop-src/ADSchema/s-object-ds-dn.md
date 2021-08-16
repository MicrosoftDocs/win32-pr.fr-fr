---
title: Syntaxe de l’objet (DS-DN)
description: Chaîne qui contient un nom unique (DN).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Syntaxe d’objet (DS-DN) schéma Active Directory
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0c9adf4138de56d90ac89743c3b428a1f25b45027bc19f0b5dccc2e005b143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835682"
---
# <a name="objectds-dn-syntax"></a>Syntaxe de l’objet (DS-DN)

Chaîne qui contient un nom unique (DN). Pour les attributs avec cette syntaxe, Active Directory gère les valeurs d’attribut en tant que références à l’objet identifié par le DN et met automatiquement à jour la valeur si l’objet est déplacé ou renommé. Pour les requêtes qui incluent des attributs de syntaxe DN dans un filtre, spécifiez des noms uniques complets. Les caractères génériques (par exemple, CN = John \* ) ne sont pas pris en charge.



| Entrée | Valeur |
|--------------|------------------------------------------------------------------------|
| Nom         | Object(DS-DN)                                                          |
| ID de syntaxe    | 2.5.5.1                                                                |
| ID OM        | 127                                                                    |
| Type MAPI    | OBJECT                                                                 |
| Type ADS     | \_chaîne DN \_ ADSTYPE                                                    |
| Type de variante | VT \_ BSTR                                                               |
| SDS, type     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
