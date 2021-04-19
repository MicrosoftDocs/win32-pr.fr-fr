---
title: commutateur/version_stamp
description: Le \_ commutateur d’horodatage/version supprime la génération de macros qui spécifient le numéro de version minimal requis du fichier d’en-tête RPC, Rpcndr. h.
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /commutateur version_stamp MIDL
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511054"
---
# <a name="version_stamp-switch"></a>\_commutateur de tampon/version

Le commutateur d' **\_ horodatage/version** supprime la génération de macros qui spécifient le numéro de version minimal requis du fichier d’en-tête RPC, Rpcndr. h.

Les nouvelles fonctionnalités MIDL peuvent nécessiter des définitions supplémentaires pour compiler correctement le stub, de sorte que le stub possède des macros qui vérifient la compatibilité entre les fichiers binaires MIDL et l’environnement de génération. Vous devrez peut-être utiliser ce commutateur si vous déplacez MIDL vers un environnement de génération différent de celui dans lequel vous avez installé les fichiers binaires MIDL pour la première fois.

Notez que le mélange d’environnements de génération n’est pas pris en charge.

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

 

 




