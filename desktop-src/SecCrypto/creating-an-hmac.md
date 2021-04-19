---
description: Explique comment créer un HMAC.
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: Création d’un HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364314081bd1d84d6d9bfff889c234470cc6775c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536478"
---
# <a name="creating-an-hmac"></a>Création d’un HMAC

**Pour calculer un HMAC**

1.  Obtenir un pointeur vers le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) Microsoft en appelant [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
2.  Créez un handle vers un [](../secgloss/h-gly.md)[*objet de hachage*](../secgloss/h-gly.md) HMAC en appelant [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Transmettez \_ le HMAC CALG dans le paramètre *algid* . Transmettez le handle d’une [*clé symétrique*](../secgloss/s-gly.md) dans le paramètre *HKEY* . Cette clé symétrique est la clé utilisée pour calculer le code HMAC.
3.  Spécifiez le type de hachage à utiliser en appelant [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) avec le paramètre *dwParam* défini sur la valeur HP \_ HMAC \_ info. Le paramètre *pbData* doit pointer vers une structure [**d' \_ informations HMAC**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info) initialisée.
4.  Appelez [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) pour commencer à calculer le HMAC des données. Le premier appel à **CryptHashData** entraîne la combinaison de la valeur de clé à l’aide de l’opérateur XOR avec la chaîne interne et les données. Le résultat de l’opération XOR est haché, puis les données cibles pour le HMAC (vers lequel pointe le paramètre *pbData* passé dans l’appel à **CryptHashData**) sont hachées. Si nécessaire, les appels suivants à **CryptHashData** peuvent ensuite être effectués pour terminer le hachage des données cibles.
5.  Appelez [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) avec le paramètre *DWPARAM* défini sur HP \_ HASHVAL. Cet appel fait en sorte que le hachage interne soit terminé et que la chaîne externe soit combinée à l’aide de XOR avec la clé. Le résultat de l’opération XOR est haché, puis le résultat du hachage interne (effectué à l’étape précédente) est haché. Le hachage externe est ensuite terminé et retourné dans le paramètre *pbData* et la longueur dans le paramètre *dwDataLen* .

> [!Note]  
> N’utilisez pas la même clé [*symétrique*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)) pour le chiffrement de message et la génération de [*code d’Authentification de message*](../secgloss/m-gly.md) (Mac). L’utilisation de la même clé pour les deux augmente considérablement le risque de décodage des messages par des attaquants.

 

 

 
