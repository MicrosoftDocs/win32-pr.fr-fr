---
title: attribut Async
description: L’attribut \ Async \ ACF définit un appel de procédure distante en tant qu’opération asynchrone.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- MIDL, attribut Async
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093766"
---
# <a name="async-attribute"></a>attribut Async

L' \[  \] attribut Async ACF définit un appel de procédure distante en tant qu’opération asynchrone.

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*opt-ACF-Attributes* 
</dt> <dd>

Spécifie des attributs de configuration d’application facultatifs.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction dans le fichier IDL.

</dd> <dt>

*Param-liste* 
</dt> <dd>

Spécifie une liste de paramètres facultative.

</dd> </dl>

## <a name="remarks"></a>Notes

Cet attribut n’est pas applicable dans les interfaces COM.

Pour déclarer une fonction RPC comme asynchrone, commencez par déclarer la fonction dans le cadre d’une définition d’interface dans un fichier IDL. Modifiez ensuite cette déclaration de fonction, dans le fichier de configuration de l’application (ACF), en appliquant l' \[  \] attribut Async. Notez que la déclaration de fonction ne fait pas mention du handle asynchrone et que le handle de liaison est le premier paramètre. L’application \[  \] de l’attribut Async dans le fichier ACF génère le code approprié afin que lorsque cette fonction est appelée, le serveur asynchrone s’attend à recevoir un handle asynchrone avant les autres paramètres.

> [!Note]  
> L’attribut Async ne peut pas être utilisé avec le commutateur de ligne de commande [**/OSF**](-osf.md) .

 

## <a name="examples"></a>Exemples

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[RPC asynchrone](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 