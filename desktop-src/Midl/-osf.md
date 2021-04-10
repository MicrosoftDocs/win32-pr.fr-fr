---
title: commutateur/OSF
description: Le commutateur/OSF force une compatibilité stricte avec l’ETCD OSF.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- MIDL du commutateur/OSF
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031125"
---
# <a name="osf-switch"></a>commutateur/OSF

Le commutateur **/OSF** force une compatibilité stricte avec l’ETCD OSF.

``` syntax
midl /osf
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Utilisez ce commutateur si votre application requiert une compatibilité stricte avec l’ETCD OSF pour des raisons de portabilité.

En mode **/OSF** , le package RPCSS est activé automatiquement lorsque vous utilisez des pointeurs complets, les arguments nécessitent une allocation de mémoire ou lorsque vous utilisez l’attribut [**Enable \_ allocate**](enable-allocate.md) . Cela signifie que vous n’avez pas besoin de fournir à l’utilisateur MIDL les fonctions d' [**\_ \_ allocation**](/windows/desktop/Rpc/the-midl-user-allocate-function) et de [**\_ \_ libération d’utilisateur MIDL**](/windows/desktop/Rpc/the-midl-user-free-function) dans votre application cliente et serveur.

Les fonctionnalités étendues Microsoft suivantes ne sont pas disponibles quand vous compilez avec le commutateur **/OSF** :

-   Déclarateurs abstraits (paramètres sans nom) dans le fichier IDL.
-   Définitions d’interface pour les objets COM.
-   Noms d’interface avec plus de 17 caractères.
-   Attributs MIDL uniquement, tels que le [**\_ marshaling de câble**](wire-marshal.md), le [**\_ Marshal d’utilisateur**](user-marshal.md)et les extensions de TypeLib (ODL).
-   Utilisation de mots clés ACF dans un fichier IDL (option de **\_ configuration MIDL/App** ).
-   Fonctions de rappel statiques sur le client.
-   Attribut [**Async**](async.md) .
-   echo [**RPC \_ quote**](cpp-quote.md) et **\# pragma MIDL \_ echo**.
-   types de caractères étendus [**WCHAR \_ t**](wchar-t.md) , constantes et chaînes.
-   initialisation d' [**enum**](enum.md) (énumérateurs épars).
-   spécification de taille en [**sortie**](out-idl.md)seule.
-   Tableaux de tailles et de pointeurs mixtes.
-   Expressions utilisées pour les spécificateurs de taille et de discriminateur.
-   Paramètres de handle explicites dans n’importe quelle position dans la liste d’arguments. En mode **/OSF** , le compilateur MIDL recherche un handle de liaison explicite comme premier paramètre. Lorsque le premier paramètre n’est pas un handle de liaison et qu’un ou plusieurs descripteurs de contexte sont spécifiés, le descripteur de contexte le plus à gauche est utilisé comme handle de liaison. Lorsque le premier paramètre n’est pas un handle et qu’il n’existe aucun descripteur de contexte, la procédure utilise une liaison implicite à l’aide du handle [**implicite \_**](implicit-handle.md) de l’attribut ACF ou du [**\_ handle automatique**](auto-handle.md).
-   Héritage de type pointeur-Attribute. Le DCE OSF n’autorise pas les pointeurs non attributs. Par conséquent, en mode **/OSF** , chaque fichier IDL doit définir des attributs pour ses pointeurs. Si un pointeur n’a pas d’attribut explicite, le fichier IDL doit avoir une spécification de [**pointeur \_ par défaut**](pointer-default.md) pour définir le type de pointeur.
-   Plusieurs interfaces dans un fichier IDL.
-   Définitions en dehors du bloc d’interface.
-   Qualificateurs de type tels que **Far** et **StdCall**.
-   Omission des attributs directionnels.

Les extensions de langage C/C++ suivantes ne sont pas disponibles quand vous compilez avec le commutateur **/OSF** :

-   Champs de bits dans les structures et les unions.
-   Les commentaires sur une seule ligne sont séparés par deux barres obliques (//).
-   Déclarations externes.
-   Procédures avec des ellipses dans la liste de paramètres.
-   Tapez [**int**](int.md).
-   Tapez **void \*** (sauf avec l' [**attribut \_ handle de contexte**](context-handle.md) ).
-   Les qualificateurs de type, y compris le formulaire avec le préfixe conforme à la norme ANSI, contiennent deux caractères de soulignement : **\_ \_ cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ Exporter**, **Exporter**, **\_ \_ Far**, **Far**, **\_ \_ loadds**, **loadds**, **\_ \_ near**, **pres**, **\_ \_ Pascal**, **Pascal**, **\_ \_ StdCall**, **StdCall**, **\_ \_ volatile** et **volatile**.
-   Un \# Avertissement [**pragma**](pragma.md) ou un commentaire **\# pragma** .
-   Sérialisation de type.
-   Type de données [**\_ \_ int3264**](--int3264.md) .
-   Le commutateur [**/Protocol**](-protocol.md) et la syntaxe de transfert ndr64.

## <a name="examples"></a>Exemples

**MIDL/OSF NomFichier. idl**

**MIDL/OSF/App \_ config nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**configuration de/App \_**](-app-config.md)
</dt> <dt>

[**/ms. \_ ext**](-ms-ext.md)
</dt> <dt>

[Package de gestion de mémoire RPCSS](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 