---
title: commutateur/ms_ext
description: Efficace avec MIDL version 3,0, les fonctionnalités activées par le \_ commutateur MS ext sont à présent le mode par défaut pour le compilateur MIDL.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /commutateur ms_ext MIDL
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093905"
---
# <a name="ms_ext-switch"></a>\_commutateur/ms. ext

Efficace avec MIDL version 3,0, les fonctionnalités activées par le commutateur **MS \_ ext** sont à présent le mode par défaut pour le compilateur MIDL.

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

L’utilisation du commutateur ne génère pas d’erreur du compilateur. vous n’avez donc pas besoin de supprimer les références à **/ms. \_ ext** ou [**/c \_ ext**](-c-ext.md) d’un Makefile existant.

Les extensions Microsoft suivantes à l’ETCD OSF sont désormais disponibles par défaut :

-   Définitions d’interface pour les objets OLE. Pour plus d’informations sur les fichiers générés pour les interfaces OLE, consultez [fichiers générés pour une interface com](files-generated-for-a-com-interface.md) .
-   Attribut de [**\[ rappel \]**](callback.md) spécifiant une fonction de rappel statique sur le client
-   [**\_ DEM quote**](cpp-quote.md)(*\_ chaîne entre guillemets*) et [**\# pragma MIDL \_ echo**](pragma.md)
-   types de caractères larges de [**WCHAR \_ t**](wchar-t.md) , constantes et chaînes
-   [**initialisation d’enum**](enum.md) (énumérateurs épars)
-   Expressions telles que la taille et les spécificateurs de discriminateur
-   [Gérer les extensions](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [Héritage de type d’attribut de pointeur](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [Plusieurs interfaces](/windows/desktop/Rpc/registering-interfaces)
-   Définitions en dehors du bloc d’interface
-   Vous pouvez omettre les [attributs directionnels](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**dans**](in.md), [**out**](out-idl.md)\]

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Héritage de type d’attribut de pointeur](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**configuration de/App \_**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 