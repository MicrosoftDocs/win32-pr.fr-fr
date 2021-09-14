---
title: attribut error_status_t
description: Le \_ mot clé Error Status \_ t désigne un type pour un objet qui contient des informations relatives à l’état de la communication ou de l’erreur.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t MIDL de l’attribut
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093610"
---
# <a name="error_status_t-attribute"></a>attribut d’état d’erreur \_ \_ t

Le mot clé **Error \_ Status \_ t** désigne un type pour un objet qui contient des informations relatives à l’état de la communication ou de l’erreur.

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*ACF-Function-Attributes* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de fonction ACF, tels que l' **\[** [**\_ État comm**](comm-status.md) **\]** , l' **\[** [**\_ État d’erreur**](fault-status.md) **\]** ou **\[** [**nocode**](nocode.md) **\]** . Les attributs de fonction sont placés entre crochets. Zéro, un ou plusieurs attributs peuvent être appliqués à une fonction. Séparez plusieurs attributs de fonction par des virgules.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.

</dd> <dt>

*ACF-Parameter-Attributes* 
</dt> <dd>

Spécifie les attributs qui s’appliquent à un paramètre. Notez que zéro, un ou plusieurs attributs peuvent être appliqués au paramètre. Séparez les attributs de plusieurs paramètres par des virgules. Les attributs de paramètres sont placés entre crochets. Les attributs de paramètres IDL, tels que les attributs directionnels, ne sont pas autorisés dans le CCP.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Spécifie le paramètre pour la fonction tel qu’il est défini dans le fichier IDL. Chaque paramètre de la fonction doit être spécifié dans la même séquence, en utilisant le même nom que celui défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

Le type d' **État d’erreur \_ \_ t** est utilisé dans le cadre de l’architecture de gestion des exceptions dans IDL. Ce type est mappé à un entier [**long**](long.md) [**non signé**](unsigned.md) . Les applications qui interceptent des situations d’erreur ont un **\[** [](out-idl.md) **\]** paramètre de sortie ou un type de retour d’une procédure spécifié en tant qu' **État d’erreur \_ \_ t**, et qualifient l' **État d’erreur \_ \_ t** avec les attributs état de la **\[** [**communication \_**](comm-status.md) **\]** ou **\[** [**\_ État**](fault-status.md) **\]** de l’erreur dans le CCP. Si le paramètre ou le type de retour n’est pas qualifié avec les attributs d’état de **\[ communication \_ \]** ou d' **\[ \_ état \] d’erreur** , le paramètre fonctionne comme s’il s’agissait d’un entier long non signé.

À partir de la version 2,0, le compilateur MIDL génère des stubs qui contiennent l’architecture de gestion des erreurs appropriée. Toutefois, les versions antérieures du compilateur MIDL géraient un paramètre ou un type de retour de l' **État d’erreur \_ \_ t** comme si les **\[** attributs [**\_ État comm**](comm-status.md) **\]** et **\[** [**\_ État**](fault-status.md) d’erreur **\]** étaient appliqués, même si ce n’est pas le cas. Avec MIDL 2,0 ou version ultérieure, vous devez appliquer explicitement les attributs **\[ \_ état \] comm** et **\[ \_ état \] d’erreur** au paramètre ou à la procédure dans le CCP.

Le type d' **État d’erreur \_ \_ t** est l’un des types prédéfinis du langage de définition d’interface. Les types prédéfinis peuvent apparaître en tant que spécificateurs de type dans les déclarations [**typedef**](typedef.md) , en déclarations générales et dans les déclarateurs de fonction (comme les spécificateurs de type fonction-retour ou en tant que spécificateurs de type paramètre).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**État comm. \_**](comm-status.md)
</dt> <dt>

[**État de l’erreur \_**](fault-status.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**non signé**](unsigned.md)
</dt> </dl>

 

 




