---
description: Explique comment créer un hachage CALG \_ SSL3 \_ SHAMD5.
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Création d’un hachage de CALG_SSL3_SHAMD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536711"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a>Création d’un \_ hachage CALG SSL3 \_ SHAMD5

**Pour créer un \_ hachage CALG SSL3 \_ SHAMD5**

1.  À l’aide de la méthodologie CryptoAPI standard, créez un [](../secgloss/s-gly.md) [*hachage*](../secgloss/h-gly.md) MD5 et un hachage SHA des données cibles.
2.  Concaténez les deux hachages, avec la valeur MD5 la plus à gauche et la valeur SHA la plus à droite. Cela génère une valeur de 36 octets (16 octets + 20 octets).
3.  Obtient un handle vers un [*objet de hachage*](../secgloss/h-gly.md) en appelant [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) avec CALG \_ SSL3 \_ SHAMD5 passé dans le paramètre *algid* .
4.  Définissez la valeur de hachage avec un appel à [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam). Les valeurs de hachage concaténées sont passées en tant qu' **octets** \* dans le paramètre *pbData* , et la \_ valeur HP HASHVAL doit être transmise dans le paramètre *dwParam* . L’appel de [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) à l’aide du handle retourné par [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) à l’étape 3 échouera.
5.  Appelez [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) pour générer la signature.
6.  Appelez [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) pour détruire l’objet de hachage.

 

 
