---
title: attribut public
description: L’attribut \ public \ comprend un alias déclaré avec le mot clé typedef dans la bibliothèque de types.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- MIDL (attribut public)
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093230"
---
# <a name="public-attribute"></a>attribut public

L’attribut **\[ \] public** comprend un alias déclaré avec le mot clé [**typedef**](typedef.md) dans la bibliothèque de types.

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type de données* 
</dt> <dd>

Type de données pour lequel l’identificateur sera un alias.

</dd> <dt>

*identifier* 
</dt> <dd>

Autre nom par lequel le *type de données* sera connu dans le logiciel.

</dd> </dl>

## <a name="remarks"></a>Notes

Par défaut, un alias qui est déclaré avec [**typedef**](typedef.md) et n’a pas d’autres attributs est traité comme une **\# définition** et n’est pas inclus dans la bibliothèque de types. L’utilisation de l’attribut **\[ public \]** garantit que l’alias devient partie intégrante de la bibliothèque de types.

> [!Note]  
> Le compilateur MIDL requiert que vous appliquiez explicitement l’attribut **\[ public \]** à chaque typedef que vous souhaitez public.

 

## <a name="examples"></a>Exemples

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 