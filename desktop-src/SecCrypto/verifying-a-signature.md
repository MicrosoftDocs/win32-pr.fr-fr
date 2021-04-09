---
description: Pour vérifier une signature, créez un objet de hachage à l’aide de CryptCreateHash. Cet objet de hachage accumule les données à vérifier. Les données sont ensuite ajoutées à l’objet de hachage avec la fonction CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Vérification d’une signature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114110"
---
# <a name="verifying-a-signature"></a>Vérification d’une signature

Pour vérifier une signature, créez un [*objet de hachage*](../secgloss/h-gly.md) à l’aide de [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Cet objet de hachage accumule les données à vérifier. Les données sont ensuite ajoutées à l’objet de hachage avec la fonction [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .

Une fois le dernier bloc de données ajouté au hachage, utilisez [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) pour vérifier la signature. L’adresse des données de signature, un descripteur de l’objet de hachage et le descripteur des clés publiques sont passés à **CryptVerifySignature**.

Une fois que la signature a été vérifiée (ou n’a pas réussi la vérification), détruisez l’objet de hachage à l’aide de la fonction [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) .

 

 
