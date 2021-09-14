---
title: commutateur/app_config
description: Le commutateur de configuration/App \_ sélectionne le mode de configuration de l’application, ce qui vous permet d’utiliser des mots clés ACF dans le fichier IDL. Avec ce commutateur MIDL du compilateur, vous pouvez omettre le ACF et spécifier une interface dans un fichier IDL unique.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /commutateur app_config MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093974"
---
# <a name="app_config-switch"></a>\_commutateur de configuration/App

Le **commutateur \_ de configuration/App** sélectionne le mode de configuration de l’application, ce qui vous permet d’utiliser des mots clés ACF dans le fichier IDL. Avec ce commutateur MIDL du compilateur, vous pouvez omettre le ACF et spécifier une interface dans un fichier IDL unique.

``` syntax
midl /app_config
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Microsoft RPC prend en charge l’utilisation des attributs ACF suivants dans le fichier IDL :

-   Handle implicite \_
-   \_Handle automatique
-   \_Handle explicite

Les versions ultérieures de Microsoft RPC peuvent prendre en charge l’utilisation d’autres attributs ACF dans le fichier IDL. L’option de **\_ configuration/App** représente une extension Microsoft de la spécification OSF-DCE et, par conséquent, s’exclut mutuellement avec l’option [**/OSF**](-osf.md) .

Pour plus d’informations sur le commutateur de configuration **/app \_** , consultez fichier de [configuration d’application (ACF)](application-configuration-file-acf-.md) et [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Exemples

**\_nom du fichier. idl de la configuration MIDL/App**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




