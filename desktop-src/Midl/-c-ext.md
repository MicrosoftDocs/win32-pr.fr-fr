---
title: commutateur/c_ext
description: Ce commutateur est obsolète à partir de la version 3,0 du compilateur MIDL. Toutefois, l’utilisation du \_ commutateur c ext ne génère pas d’erreur du compilateur. vous n’avez donc pas besoin de supprimer les références à/ms. \_ ext ou/c \_ ext d’un Makefile existant.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /commutateur c_ext MIDL
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093973"
---
# <a name="c_ext-switch"></a>\_commutateur/c ext

Ce commutateur est obsolète à partir de la version 3,0 du compilateur MIDL. Toutefois, l’utilisation du commutateur **c \_ ext** ne génère pas d’erreur du compilateur. vous n’avez donc pas besoin de supprimer les références à [**/ms. \_ ext**](-ms-ext.md) ou **/c \_ ext** d’un Makefile existant.

``` syntax
midl /c_ext
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Les fonctionnalités suivantes sont désormais disponibles par défaut :

-   De nombreux fichiers d’en-tête existants définissent des types avec des qualificateurs, tels que **Far** et **StdCall**, qui ne font pas partie de l’IDL DCE. Ces compilateurs (et le compilateur MIDL dans le mode de compatibilité DCE) génèrent des erreurs lorsqu’ils tentent de traiter ces qualificateurs. Le compilateur MIDL vous permet de compiler des fichiers IDL qui contiennent ces qualificateurs. Les qualificateurs de type n’affectent pas la manière dont les données sont transmises sur le réseau.
-   Vous pouvez omettre des attributs directionnels comme [**\[ in \]**](in.md) ou [**\[ out \]**](out-idl.md).

Les extensions de langage C suivantes sont prises en charge en mode par défaut :

-   Champs de bits dans les structures et les unions
-   Commentaires commençant par deux barres obliques (//)
-   Déclarations externes
-   Procédures avec des points de suspension dans la liste de paramètres (...)
-   Sur les plateformes 32 bits, [**int**](int.md) est un type de base 32 bits natif ; sur les plateformes 16 bits, **int** est reconnu, mais n’est pas un type accessible à distance
-   Tapez [**void \***](void.md) qui n’est pas utilisé dans les opérations distantes
-   Les qualificateurs de type (y compris le formulaire avec le préfixe conforme à la norme ANSI) contiennent deux caractères de soulignement : **cdecl**, **\_ \_ cdecl**, [**const**](const.md), **\_ \_ const**, **Exporter**, **\_ \_ Exporter**, **Far**, **\_ \_ Far**, **loadds**, **\_ \_ loadds**, **pres**, **\_ \_ near**, **Pascal**, **\_ \_ Pascal**, **StdCall**, **\_ \_ StdCall**, **volatile** et **\_ \_ volatile**.

Pour plus d’informations sur les qualificateurs de déclaration, consultez la documentation de Microsoft C/C++.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**configuration de/App \_**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




