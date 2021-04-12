---
title: attribut auto_handle
description: L’attribut \ auto \_ handle \ ACF indique au stub d’établir automatiquement la liaison pour une fonction qui n’a pas de paramètre de handle de liaison explicite. Remarque Cet attribut est obsolète et n’est plus pris en charge.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462542"
---
# <a name="auto_handle-attribute"></a>\_attribut de descripteur automatique

L’attribut **\[ auto \_ handle \]** ACF indique au stub d’établir automatiquement la liaison pour une fonction qui n’a pas de paramètre de handle de liaison explicite.

> [!Note]  
> Cet attribut est obsolète et n’est plus pris en charge. L’utilisation du commutateur [**/Robust**](-robust.md) est recommandée.

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*interface-attribut-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à l’interface dans son ensemble, par exemple [**code**](code.md) ou [**nocode**](nocode.md). Séparez les attributs d’interface par des virgules.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Spécifie le nom de l’interface.

</dd> <dt>

*définition d’interface* 
</dt> <dd>

Spécifie les instructions IDL qui forment la définition de l’interface.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ \_ handle \] automatique** s’affiche dans l’en-tête d’interface du CCP. Elle apparaît également dans l’en-tête d’interface du fichier IDL lorsque vous spécifiez le commutateur de compilateur MIDL [**/app \_ config**](-app-config.md).

Lorsque le client appelle une fonction qui utilise la liaison automatique et qu’il n’existe aucune liaison à un serveur, le stub établit automatiquement la liaison. La liaison est réutilisée pour les appels suivants à d’autres fonctions dans l’interface qui utilisent la liaison automatique. Le programme d’application cliente n’a pas besoin de déclarer ou d’effectuer un traitement relatif au handle de liaison.

Lorsque le ACF n’est pas présent ou n’inclut pas l’attribut de [**\[ \_ handle \] implicite**](implicit-handle.md) , le compilateur MIDL utilise le **\[ \_ handle \] automatique** et émet un message d’information. Le compilateur MIDL utilise également le **\[ \_ handle \] automatique**, si nécessaire, pour établir la liaison initiale pour un [**\[ \_ handle \] de contexte**](context-handle.md).

L’attribut de **\[ \_ handle \] automatique** peut se produire uniquement si le [**\[ \_ handle \] implicite**](implicit-handle.md) ou l’attribut de [**\[ \_ handle \] explicite**](explicit-handle.md) ne se produit pas. L’attribut de **\[ \_ handle \] automatique** peut se produire dans l’en-tête de l’interface ACF ou IDL au plus une fois.

> [!Note]  
> Vous ne pouvez pas utiliser la liaison automatique (avec l’attribut **\[ \_ handle \] automatique** ou par défaut) si vous traitez des données par le biais de canaux.

 

## <a name="examples"></a>Exemples

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**configuration de/App \_**](-app-config.md)
</dt> <dt>

[**code**](code.md)
</dt> <dt>

[**\_handle explicite**](explicit-handle.md)
</dt> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[**handle implicite \_**](implicit-handle.md)
</dt> <dt>

[**SansCode**](nocode.md)
</dt> </dl>

 

 




