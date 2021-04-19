---
title: vararg (attribut)
description: L’attribut \ vararg \ spécifie que la fonction accepte un nombre variable de paramètres. Pour ce faire, le dernier paramètre doit être un tableau sécurisé de type VARIANT qui contient tous les paramètres restants.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- MIDL (MIDL), attribut vararg
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509031"
---
# <a name="vararg-attribute"></a>vararg (attribut)

L’attribut **\[ vararg \]** spécifie que la fonction accepte un nombre variable de paramètres. Pour ce faire, le dernier paramètre doit être un tableau sécurisé de type **Variant** qui contient tous les paramètres restants.

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*attributs facultatifs* 
</dt> <dd>

Spécifie zéro ou plusieurs attributs à appliquer à la fonction. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*type de retour* 
</dt> <dd>

Type des données retournées par la procédure distante à l’achèvement.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Nom de la procédure distante.

</dd> <dt>

*facultatif-param-Attributes* 
</dt> <dd>

Spécifie zéro ou plusieurs attributs à appliquer au paramètre de fonction immédiatement après la liste d’attributs.

</dd> <dt>

*Param-liste* 
</dt> <dd>

Spécifie tous les paramètres, enregistrez le paramètre final, variable.

</dd> <dt>

*Last-param-Name* 
</dt> <dd>

Nom du paramètre variable.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous ne pouvez pas appliquer les **\[** attributs [**facultatifs**](optional.md) **\]** ou **\[** [**DefaultValue**](defaultvalue.md) **\]** à des paramètres dans une fonction qui a l’attribut **\[ vararg \]** .

## <a name="examples"></a>Exemples

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DefaultValue**](defaultvalue.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**facultatif**](optional.md)
</dt> </dl>

 

 