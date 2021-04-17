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
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519353"
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

 

 
