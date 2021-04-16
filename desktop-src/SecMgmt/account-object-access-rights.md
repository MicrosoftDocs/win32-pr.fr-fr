---
description: Le type de droits d’accès à l’objet de compte a les types d’accès suivants.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Droits d’accès à l’objet de compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529649"
---
# <a name="account-object-access-rights"></a>Droits d’accès à l’objet de compte

Le type de droits d’accès à l’objet de compte a les types d’accès suivants.



| Type d’accès                     | Description                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| vue de compte \_                   | Ce type d’accès est nécessaire pour lire les informations de compte. Cela comprend les [*privilèges*](/windows/desktop/SecGloss/p-gly) attribués au compte, les quotas de mémoire affectés et tout type d’accès spécial accordé. |
| \_privilèges d’ajustement de compte \_     | Ce type d’accès est nécessaire pour attribuer des privilèges à un compte ou en supprimer.                                                                                                                                                            |
| COMPTE- \_ ajuster les \_ quotas         | Ce type d’accès est requis pour modifier les quotas système attribués à un compte.                                                                                                                                                                      |
| COMPTE \_ ajuster \_ \_ l’accès système | Ce type d’accès est nécessaire pour mettre à jour les indicateurs d’accès système pour le compte.                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a>Masques d’accès génériques

L’objet [**Account**](account-object.md) publie les mappages suivants à partir de types d’accès génériques à des types d’accès spécifiques.

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>Types d’accès standard

Cet objet ne prend pas en charge le type d’accès standard SYNCHRONIZE (facultatif). Tous les types d’accès requis sont pris en charge. Le masque de tous les types d’accès pris en charge pour ce type d’objet est le suivant.

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
