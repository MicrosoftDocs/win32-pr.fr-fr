---
title: attribut comm_status
description: L’attribut \ comm \_ Status \ ACF provoque le renvoi d’un code d’erreur lorsqu’une erreur de communication se produit pendant l’exécution d’une fonction.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status MIDL de l’attribut
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093721"
---
# <a name="comm_status-attribute"></a>\_attribut de statut comm

L’attribut CCP **\[ \_ Status \]** ACF provoque le renvoi d’un code d’erreur lorsqu’une erreur de communication se produit pendant l’exécution d’une fonction.

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*ACF-Function-Attributes* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs de fonction ACF, tels que l' **\[ \_ état \] comm** et le **\[** [**nocode**](nocode.md) **\]** . Les attributs de fonction sont placés entre crochets. Zéro, un ou plusieurs attributs peuvent être appliqués à une fonction. Séparez plusieurs attributs de fonction par des virgules. Notez que si l' **\[ \_ état \]** de la communication apparaît en tant qu’attribut de fonction, il ne peut pas apparaître en tant qu’attribut de paramètre.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.

</dd> <dt>

*ACF-Parameter-Attributes* 
</dt> <dd>

Spécifie les attributs qui s’appliquent à un paramètre. Notez que zéro, un ou plusieurs attributs peuvent être appliqués au paramètre. Séparez les attributs de plusieurs paramètres par des virgules. Les attributs de paramètres sont placés entre crochets. Les attributs de paramètres IDL, tels que les attributs directionnels, ne sont pas autorisés dans le CCP. Notez que si l' **\[ \_ état \] comm** apparaît en tant qu’attribut de paramètre, il ne peut pas apparaître en tant qu’attribut de fonction.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Spécifie le paramètre pour la fonction tel qu’il est défini dans le fichier IDL. Chaque paramètre de la fonction doit être spécifié dans la même séquence, en utilisant le même nom que celui défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ \_ état \] comm** peut être utilisé en tant qu’attribut de fonction ou en tant qu’attribut de paramètre, mais il ne peut apparaître qu’une seule fois par fonction. Elle peut être appliquée à la fonction ou à un paramètre dans chaque fonction.

L’attribut d' **\[ \_ état \] de communication** peut être appliqué uniquement aux fonctions qui retournent le type d’état d' [**erreur \_ \_ t**](error-status-t.md). Lorsqu’une erreur de communication se produit pendant l’exécution de la fonction, un code d’erreur est retourné.

Lorsque l' **\[ \_ état \] comm** est utilisé en tant qu’attribut de paramètre, le paramètre doit être défini dans le fichier IDL et doit être un **\[** [](out-idl.md) **\]** paramètre out de type [**Error \_ Status \_ t**](error-status-t.md). Lorsqu’une erreur de communication se produit pendant l’exécution de la fonction, le paramètre est défini sur le code d’erreur. Lorsque l’appel à distance est effectué avec succès, la procédure définit la valeur.

Il est possible que les attributs **\[ \_ état \]** de la communication et **\[** [**\_ État**](fault-status.md) de l’erreur **\]** apparaissent dans une fonction unique, en tant qu’attributs de fonction ou attributs de paramètre. Si les deux attributs sont des attributs de fonction ou s’ils s’appliquent au même paramètre et qu’aucune erreur ne se produit, la fonction ou le paramètre a la valeur **État d’erreur \_ \_ OK**. Dans le cas contraire, elle contient la valeur appropriée de l’état de la **\[ communication \_ \]** ou de l' **\[ \_ état \] d’erreur** . Étant donné que les valeurs retournées pour l' **\[ \_ état \] comm** sont différentes des valeurs retournées pour l' **\[ \_ état \] Fault**, les valeurs retournées sont facilement interprétées.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**État d’erreur \_ \_ t**](error-status-t.md)
</dt> <dt>

[**État de l’erreur \_**](fault-status.md)
</dt> <dt>

[**SansCode**](nocode.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> </dl>

 

 




