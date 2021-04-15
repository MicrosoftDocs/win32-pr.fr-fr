---
description: Répertorie et décrit les droits d’accès de l’objet de données privées.
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: Droits d’accès à un objet de données privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484577"
---
# <a name="private-data-object-access-rights"></a>Droits d’accès à un objet de données privées

Les types d’accès de ce type d’objet sont :



| Type d’accès          | Description                                      |
|----------------------|--------------------------------------------------|
| valeur de la \_ requête secrète \_ | Ce type d’accès est nécessaire pour récupérer un secret. |
| valeur de l’ensemble de secrets \_ \_   | Ce type d’accès est nécessaire pour modifier un secret.   |



 

## <a name="generic-access-masks"></a>Masques d’accès génériques

Ce type d’objet contient les mappages d’accès génériques suivants :

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Types d’accès standard :

Cet objet ne prend pas en charge le type d’accès standard SYNCHRONIZE (facultatif). Tous les types d’accès requis sont pris en charge. Le masque de tous les types d’accès pris en charge pour ce type d’objet est :

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



