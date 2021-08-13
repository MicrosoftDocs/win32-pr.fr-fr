---
title: commutateur/RPCSS
description: Le commutateur/RPCSS, lorsqu’il est spécifié, agit comme si l' \_ attribut Enable Allocate était spécifié pour toutes les opérations de l’interface. L’utilisation de cet attribut n’est pas recommandée.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- MIDL du commutateur/RPCSS
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0c3087f47bd12c852ef168b2684d5b094239cdac45933c8e7d831fc6461c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643739"
---
# <a name="rpcss-switch"></a>commutateur/RPCSS

Le commutateur **/RPCSS** , lorsqu’il est spécifié, agit comme si l’attribut [**Enable \_ allocate**](enable-allocate.md) était spécifié pour toutes les opérations de l’interface. L’utilisation de cet attribut n’est pas recommandée.

``` syntax
midl /rpcss
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

En mode par défaut, le package RpcSs est activé uniquement si la procédure ou l’interface a l’attribut [**Enable \_ allocate**](enable-allocate.md) ou si le commutateur **/RPCSS** est spécifié sur la ligne de commande. En mode **/OSF** , le stub côté serveur Active le package d’allocation rpcss.

## <a name="examples"></a>Exemples

**MIDL/RPCSS NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**activer l' \_ allocation**](enable-allocate.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




