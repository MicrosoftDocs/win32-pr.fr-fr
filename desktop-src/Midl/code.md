---
title: attribut de code
description: L’attribut \ code \ ACF provoque la génération du code stub client pour les fonctions distantes.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- MIDL, attribut de code
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093729"
---
# <a name="code-attribute"></a>attribut de code

L’attribut **\[ code \]** ACF provoque la génération du code stub client pour les fonctions distantes.

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*ACF-interface-attributs* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à l’ensemble de l’interface. Les attributs valides incluent le descripteur [**\[ \_ \] automatique**](auto-handle.md) ou [**\[ implicite \_ \]**](implicit-handle.md) et le **\[ code \]**, [**\[ \] le code ou**](nocode.md)l' [**\[ optimisation \]**](optimize.md). Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*nom de fichier-liste* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs noms de fichiers d’en-tête C, séparés par des virgules. Vous devez fournir le nom de fichier complet, y compris l’extension.

</dd> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs attributs, séparés par des virgules, qui s’appliquent au type spécifié. Les attributs de type valides incluent [**\[ allocate \]**](allocate.md) et [**\[ représentent \_ comme \]**](represent-as.md).

</dd> <dt>

*TypeName* 
</dt> <dd>

Spécifie un type défini dans le fichier IDL. Les attributs de type dans le ACF peuvent être appliqués uniquement aux types précédemment définis dans le fichier IDL.

</dd> <dt>

*ACF-Function-Attributes* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction dans son ensemble, par exemple l' [**\[ \_ état \] comm**](comm-status.md). Les attributs de fonction sont placés entre crochets. Séparez plusieurs attributs de fonction par des virgules.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.

</dd> <dt>

*ACF-Parameter-Attributes* 
</dt> <dd>

Spécifie les attributs ACF qui s’appliquent à un paramètre. Notez que zéro, un ou plusieurs attributs peuvent être appliqués au paramètre. Séparez les attributs de plusieurs paramètres par des virgules. Les attributs de paramètres ACF sont placés entre crochets.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Spécifie un paramètre de la fonction tel qu’il est défini dans le fichier IDL. Chaque paramètre de la fonction doit être spécifié dans la même séquence et avec le même nom que celui défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ code \]** peut apparaître dans l’en-tête ACF ou être appliqué à une fonction individuelle.

Lorsque l’attribut **\[ code \]** apparaît dans l’en-tête ACF, le code stub du client est généré pour toutes les fonctions distantes qui n’ont pas l’attribut de fonction [**\[ nocode \]**](nocode.md) . Vous pouvez remplacer l’attribut **\[ code \]** dans l’en-tête d’une fonction individuelle en spécifiant l’attribut **\[ nocode \]** en tant qu’attribut de fonction.

Lorsque l’attribut **\[ code \]** apparaît dans la liste d’attributs de la fonction distante, le code stub du client est généré pour la fonction. Le code stub du client n’est pas généré dans les cas suivants :

-   L’en-tête ACF comprend l’attribut [**\[ nocode \]**](nocode.md) .
-   L’attribut [**\[ nocode \]**](nocode.md) est appliqué à la fonction.
-   L’attribut [**\[ local \]**](local.md) s’applique à la fonction dans le fichier d’interface.

Le **\[ code \]** ou le [**\[ nocode \]**](nocode.md) peut apparaître dans la liste des attributs de l’interface ou de la fonction, mais celui que vous choisissez ne peut apparaître qu’une seule fois dans la liste.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**lui**](allocate.md)
</dt> <dt>

[**\_handle automatique**](auto-handle.md)
</dt> <dt>

[**État comm. \_**](comm-status.md)
</dt> <dt>

[**handle implicite \_**](implicit-handle.md)
</dt> <dt>

[**localisé**](local.md)
</dt> <dt>

[**SansCode**](nocode.md)
</dt> <dt>

[**requêtes**](optimize.md)
</dt> <dt>

[**représenter \_ comme**](represent-as.md)
</dt> </dl>

 

 




