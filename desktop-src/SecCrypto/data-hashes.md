---
description: Un hachage d’un texte ou d’une autre chaîne d’octets est une valeur associée de longueur fixe, unique et statistique.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Hachages de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868426"
---
# <a name="data-hashes"></a>Hachages de données

Un [*hachage*](../secgloss/h-gly.md) d’un texte ou d’une autre chaîne d’octets est une valeur associée de longueur fixe, unique et statistique. Dans certains documents, le *hachage* d’un texte est également appelé un condensé. Toutefois, dans cette documentation, le terme hachage est toujours utilisé. Les fonctions CryptoAPI offrent un moyen de créer un hachage pour tout texte ou une autre chaîne d’octets. Ce hachage, Then, peut être utilisé comme identificateur unique de ses données associées.

Pour garantir l' [*intégrité*](../secgloss/i-gly.md) d’un texte, un [*hachage*](../secgloss/h-gly.md) de texte peut être envoyé pour accompagner le texte. Le récepteur peut ensuite calculer un hachage sur les données reçues et comparer le hachage calculé avec le hachage reçu. Si les deux correspondances sont identiques, les données reçues doivent être les mêmes que celles à partir desquelles le hachage reçu a été créé.

Pour obtenir une valeur de hachage, créez un objet de hachage à l’aide de [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Cet objet accumule les données à vérifier. Les données sont ensuite ajoutées à l’objet de hachage avec la fonction [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .

Une fois le dernier bloc de données ajouté au hachage, la fonction [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) est utilisée pour obtenir la valeur de hachage des données.

Une meilleure sécurité est fournie en détruisant l’objet de hachage avec [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) dès que la valeur de hachage a été obtenue.

 

 
