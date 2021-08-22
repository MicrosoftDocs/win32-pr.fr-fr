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
ms.openlocfilehash: 9f8e4944404bccc734594f3847c0ff9de17e54d0b5bcc444a56abe9b8f1e0eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328719"
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

## <a name="remarks"></a>Remarques

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

 

 