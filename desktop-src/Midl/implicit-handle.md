---
title: attribut implicit_handle
description: L’attribut \ CCP (handle implicite) \_ \ ACF spécifie le descripteur utilisé pour les fonctions qui n’incluent pas de handle explicite en tant que paramètre de procédure.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093506"
---
# <a name="implicit_handle-attribute"></a>attribut de handle implicite \_

L’attribut CCP de **\[ \_ handle \] implicite** spécifie le descripteur utilisé pour les fonctions qui n’incluent pas de handle explicite en tant que paramètre de procédure.

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*handle-type* 
</dt> <dd>

Spécifie le type de données handle, tel que le type de base [**handle \_ t**](handle-t.md) ou un type de handle défini par l’utilisateur.

</dd> <dt>

*handle-nom* 
</dt> <dd>

Spécifie le nom du descripteur.

</dd> </dl>

## <a name="remarks"></a>Notes

Le descripteur spécifié par l’attribut de **\[ \_ handle \] implicite** est utilisé de différentes façons en fonction de la nature de la procédure. Si la procédure est distante, le handle sera utilisé comme handle de liaison pour l’appel distant. Le handle implicite peut également être utilisé pour établir une liaison initiale pour une fonction qui utilise un handle de contexte. Si la procédure est une procédure de sérialisation, le handle est utilisé comme handle de sérialisation contrôlant l’opération. Dans le cas de la sérialisation de type, le handle est utilisé comme handle de sérialisation pour tous les types sérialisés.

L’attribut **\[ \_ handle \] implicite** spécifie une variable globale qui contient un handle utilisé par n’importe quelle fonction nécessitant des handles implicites.

Le type de handle de liaison implicite doit être [**handle \_ t**](handle-t.md) (ou un type basé sur **handle \_ t**) ou un type de handle défini par l’utilisateur spécifié avec l’attribut [**descripteur**](handle.md) . Le handle de sérialisation implicite doit être un type basé sur le **handle \_ t**.

Si le type de handle implicite n’est pas défini dans le fichier IDL ou dans tous les fichiers inclus et importés par le fichier IDL pour l’ordinateur MIDL, vous devez fournir le fichier contenant la définition de type handle-type lors de la compilation des stubs. Utilisez l’instruction CCP [**include**](include.md) pour inclure le fichier contenant la définition handle-type.

L’attribut de **\[ \_ handle \] implicite** peut se produire une seule fois, au plus. L’attribut **\[ \_ handle \] implicite** peut se produire uniquement si les attributs [**\[ \_ handle \] automatique**](auto-handle.md) et [**\[ \_ handle \] explicite**](explicit-handle.md) ne se produisent pas.

## <a name="examples"></a>Exemples

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**\_handle automatique**](auto-handle.md)
</dt> <dt>

[**\_handle explicite**](explicit-handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**inclusion**](include.md)
</dt> </dl>

 

 




