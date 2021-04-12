---
title: attribut nocode
description: L’attribut \ nocode \ est utilisé dans les en-têtes ACF ou avec des fonctions individuelles pour empêcher la génération de code stub client.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- attribut nocode MIDL
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312211"
---
# <a name="nocode-attribute"></a>attribut nocode

L’attribut **\[ nocode \]** est utilisé dans les en-têtes ACF ou avec des fonctions individuelles pour empêcher la génération de code stub client.

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*ACF-interface-attributs* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à l’ensemble de l’interface. Les attributs valides incluent **\[** [**\_ handle automatique**](auto-handle.md) **\]** ou **\[** [**\_ handle implicite**](implicit-handle.md) **\]** et **\[** [**code**](code.md) **\]** ou **\[ \] nocode**. Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface. Dans le mode de compatibilité DCE, le nom de l’interface doit correspondre au nom de l’interface spécifiée dans le fichier IDL. Quand vous utilisez le commutateur de compilateur MIDL [**/ACF**](-acf.md), le nom d’interface dans le CCP et le nom d’interface dans le fichier IDL peuvent être différents.

</dd> <dt>

*nom de fichier-liste* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs noms de fichiers d’en-tête en langage C, séparés par des virgules. Le nom de fichier complet, y compris l’extension, doit être fourni.

</dd> <dt>

*type-attribut-List* 
</dt> <dd>

Spécifie une liste d’un ou plusieurs attributs, séparés par des virgules, qui s’appliquent au type spécifié. Les attributs de type valides incluent **\[** [**allocate**](allocate.md) **\]** .

</dd> <dt>

*TypeName* 
</dt> <dd>

Spécifie un type défini dans le fichier IDL. Les attributs de type dans le ACF peuvent uniquement être appliqués aux types précédemment définis dans le fichier IDL.

</dd> <dt>

*ACF-Function-Attributes* 
</dt> <dd>

Spécifie les attributs qui s’appliquent à la fonction dans son ensemble, par exemple l' **\[** [**\_ État comm**](comm-status.md) **\]** . Les attributs de fonction sont placés entre crochets. Séparez plusieurs attributs de fonction par des virgules.

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

Spécifie un paramètre de la fonction tel qu’il est défini dans le fichier IDL. Chaque paramètre de la fonction doit être spécifié dans la même séquence et utiliser le même nom que celui défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ nocode \]** peut apparaître dans l’en-tête ACF, ou il peut être appliqué à une fonction individuelle.

Lorsque l’attribut **\[ \] nocode** apparaît dans l’en-tête ACF, le code stub du client n’est pas généré pour une fonction distante, sauf s’il a l’attribut de fonction de **\[** [**code**](code.md) **\]** . Vous pouvez remplacer l’attribut **\[ nocode \]** dans l’en-tête d’une fonction individuelle en spécifiant l’attribut de **\[ code \]** en tant qu’attribut de fonction.

Lorsque l’attribut **\[ nocode \]** apparaît dans la liste d’attributs de la fonction, aucun code stub client n’est généré pour la fonction.

Le code stub du client n’est pas généré dans les cas suivants :

-   L’en-tête ACF comprend l’attribut **\[ nocode \]** .
-   L’attribut **\[ nocode \]** est appliqué à la fonction.
-   L' **\[** attribut [**local**](local.md) **\]** s’applique à la fonction dans le fichier d’interface.

**\[** [**Code**](code.md) **\]** ou **\[ nocode \]** peut apparaître dans la liste des attributs d’une fonction, et celui que vous choisissez peut apparaître une seule fois.

L’attribut **\[ nocode \]** est ignoré lors de la génération de stubs de serveur. Vous ne pouvez pas l’appliquer lors de la génération de stubs de serveur dans le mode de compatibilité DCE.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**lui**](allocate.md)
</dt> <dt>

[**\_handle automatique**](auto-handle.md)
</dt> <dt>

[**code**](code.md)
</dt> <dt>

[**État comm. \_**](comm-status.md)
</dt> <dt>

[**handle implicite \_**](implicit-handle.md)
</dt> </dl>

 

 




