---
description: Répertorie et décrit les droits d’accès de l’objet TrustedDomain.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Droits d’accès à l’objet TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efeaf621cc3727cb936e69806bbcf89dabe5d41eb39b38dce3f9f23a0200dcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893007"
---
# <a name="trusteddomain-object-access-rights"></a>Droits d’accès à l’objet TrustedDomain

Le type d’objet [**trustedDomain**](trusteddomain-object.md) a les types d’accès suivants :



| Type d’accès                  | Description                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| nom de domaine de la \_ requête approuvée \_ \_ | Ce type d’accès est nécessaire pour interroger le nom du domaine approuvé.              |
| \_contrôleurs de jeu approuvés \_    | Ce type d’accès est nécessaire pour définir la liste des contrôleurs du domaine approuvé. |
| requête de confiance \_ \_ POSIX        | Ce type d’accès est nécessaire pour récupérer le décalage d’ID POSIX d’un domaine approuvé.  |
| jeu de confiance \_ \_ POSIX          | Ce type d’accès est nécessaire pour définir le décalage d’ID POSIX d’un domaine approuvé.       |



 

## <a name="generic-access-masks"></a>Masques d’accès génériques

Ce type d’objet contient les mappages d’accès génériques suivants :

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a>Types d’accès standard

Cet objet ne prend pas en charge le type d’accès standard SYNCHRONIZE (facultatif). Tous les types d’accès requis sont pris en charge. Le masque de tous les types d’accès pris en charge pour ce type d’objet est :

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



