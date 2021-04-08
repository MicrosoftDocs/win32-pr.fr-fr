---
title: attribut fault_status
description: L’attribut \ \_ CCP Status indique qu’un code d’erreur de type Error \_ Status indique qu’il s’agit \_ d’un échec de la procédure distante, plutôt que d’autres types de problèmes tels que des erreurs de communication.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status MIDL de l’attribut
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678250"
---
# <a name="fault_status-attribute"></a>\_attribut état d’erreur

L’attribut ACF de l' **\[ \_ état \]** d’erreur indique qu’un code d’erreur de type [**erreur \_ \_ t**](error-status-t.md) indique un échec de la procédure distante, plutôt que d’autres types de problèmes tels que des erreurs de communication.

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*ACF-Function-Attributes* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de fonction ACF tels que l' **\[ \_ état \] d’erreur** et le **\[** [**nocode**](nocode.md) **\]** . Les attributs de fonction sont placés entre crochets. Notez que zéro, un ou plusieurs attributs peuvent être appliqués à une fonction. Séparez plusieurs attributs de fonction par des virgules. Notez également que si l' **\[ \_ état \] d’erreur** apparaît en tant qu’attribut de fonction, il ne peut pas apparaître en tant qu’attribut de paramètre.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.

</dd> <dt>

*ACF-Parameter-Attributes* 
</dt> <dd>

Spécifie les attributs qui s’appliquent à un paramètre. Notez que zéro, un ou plusieurs attributs peuvent être appliqués au paramètre. Les attributs de paramètres sont placés entre crochets. Séparez les attributs de plusieurs paramètres par des virgules. Les attributs de paramètres IDL, tels que les attributs directionnels, ne sont pas autorisés dans le CCP. Notez que si l' **\[ \_ état \] d’erreur** apparaît en tant qu’attribut de paramètre, il ne peut pas apparaître en tant qu’attribut de fonction.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Spécifie le paramètre pour la fonction tel qu’il est défini dans le fichier IDL. Chaque paramètre de la fonction doit être spécifié dans la même séquence, en utilisant le même nom que celui défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ \_ état \] d’erreur** peut être utilisé en tant qu’attribut de fonction ou en tant qu’attribut de paramètre, mais il ne peut apparaître qu’une seule fois par fonction. Elle peut être appliquée à la fonction elle-même ou à un paramètre dans chaque fonction.

L’attribut **\[ \_ état \]** d’erreur peut être appliqué uniquement aux fonctions qui retournent le type d' [**État d’erreur \_ \_ t**](error-status-t.md). Lorsque la procédure distante échoue d’une manière qui provoque le retour d’une PDU d’erreur, un code d’erreur est renvoyé.

Lorsque l' **\[ \_ état \]** de l’erreur est utilisé en tant qu’attribut de paramètre, le paramètre doit être un **\[** [](out-idl.md) **\]** paramètre de sortie de type [**État d’erreur \_ \_ t**](error-status-t.md). Si une erreur de serveur se produit, le paramètre est défini sur le code d’erreur. Une fois l’appel distant terminé, la procédure définit la valeur.

Il n’est pas nécessaire de spécifier le paramètre associé à l’attribut d' **\[ \_ état \] d’erreur** dans le fichier IDL. Lorsque le paramètre n’est pas spécifié, un nouveau paramètre [**out**](out-idl.md) de type [**Error \_ Status \_ t**](error-status-t.md) est généré à la suite du dernier paramètre défini dans le fichier IDL DCE.

Il est possible que les attributs **\[ \_ état \]** de l’erreur et **\[** [**\_ État**](comm-status.md) de la communication **\]** apparaissent dans une seule fonction, en tant qu’attributs de fonction ou attributs de paramètre. Si les deux attributs sont des attributs de fonction, ou s’ils s’appliquent au même paramètre et qu’aucune erreur ne se produit, la fonction ou le paramètre a la valeur **« État d’erreur \_ \_ OK »**. Dans le cas contraire, elle contient la valeur de code d’État appropriée. Étant donné que les valeurs retournées pour l' **\[ \_ état \] d’erreur** sont différentes de celles retournées pour l' **\[ \_ état \] comm**, les valeurs retournées sont facilement interprétées.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**État comm. \_**](comm-status.md)
</dt> <dt>

[**État d’erreur \_ \_ t**](error-status-t.md)
</dt> <dt>

[**SansCode**](nocode.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> </dl>

 

 




