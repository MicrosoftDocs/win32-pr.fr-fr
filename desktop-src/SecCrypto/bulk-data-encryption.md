---
description: Une clé de chiffrement en bloc est générée par le hachage de l’une des clés MAC à l’aide de CryptHashSessionKey avec le contenu du message et d’autres données. Le message est chiffré/déchiffré avec l’une des clés de chiffrement en bloc de la manière habituelle.
ms.assetid: 08174502-3ff1-4c1c-bcd0-46fd85882305
title: Chiffrement des données en bloc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecfb55c162e5aa576d8baa3d0ccbc45e9588c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539744"
---
# <a name="bulk-data-encryption"></a>Chiffrement des données en bloc

Une [*clé de chiffrement en bloc*](../secgloss/b-gly.md) est générée par le [*hachage*](../secgloss/h-gly.md) de l’une des clés Mac à l’aide de [**CryptHashSessionKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) avec le contenu du message et d’autres données. Le message est chiffré/déchiffré avec l’une des clés de chiffrement en bloc de la manière habituelle.

Lors de l’utilisation d’un [*chiffrement par bloc*](../secgloss/b-gly.md), le moteur de protocole [*Schannel*](../secgloss/s-gly.md) effectue tous les [*remplissages*](../secgloss/p-gly.md)de *chiffrement par bloc* nécessaires. Quand [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) et [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) sont appelés, l’indicateur final est toujours **false** et la longueur des données est un multiple de longueurs entières de bloc.

> [!Note]  
> Le CSP ne doit jamais mettre en mémoire tampon les données en interne. Une fois que les données ont été chiffrées (ou déchiffrées), la taille du [*texte en clair*](../secgloss/p-gly.md) doit toujours correspondre exactement à la taille du [*texte chiffré*](../secgloss/c-gly.md).

 

 

 
