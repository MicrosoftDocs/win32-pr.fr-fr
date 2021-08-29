---
description: Une clé de chiffrement en bloc est générée par le hachage de l’une des clés MAC à l’aide de CryptHashSessionKey avec le contenu du message et d’autres données. Le message est chiffré/déchiffré avec l’une des clés de chiffrement en bloc de la manière habituelle.
ms.assetid: 08174502-3ff1-4c1c-bcd0-46fd85882305
title: Chiffrement des données en bloc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb50e156a2e689d01afba2cb383a08dad0b005377e2e745e013adde4b685d882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879479"
---
# <a name="bulk-data-encryption"></a>Chiffrement des données en bloc

Une [*clé de chiffrement en bloc*](../secgloss/b-gly.md) est générée par le [*hachage*](../secgloss/h-gly.md) de l’une des clés Mac à l’aide de [**CryptHashSessionKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) avec le contenu du message et d’autres données. Le message est chiffré/déchiffré avec l’une des clés de chiffrement en bloc de la manière habituelle.

Lors de l’utilisation d’un [*chiffrement par bloc*](../secgloss/b-gly.md), le moteur de protocole [*Schannel*](../secgloss/s-gly.md) effectue tous les [*remplissages*](../secgloss/p-gly.md)de *chiffrement par bloc* nécessaires. Quand [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) et [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) sont appelés, l’indicateur final est toujours **false** et la longueur des données est un multiple de longueurs entières de bloc.

> [!Note]  
> Le CSP ne doit jamais mettre en mémoire tampon les données en interne. Une fois que les données ont été chiffrées (ou déchiffrées), la taille du [*texte en clair*](../secgloss/p-gly.md) doit toujours correspondre exactement à la taille du [*texte chiffré*](../secgloss/c-gly.md).

 

 

 
