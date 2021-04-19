---
description: Créez une liste de certificats de confiance (CTL) signée et enregistrez-la dans un magasin de certificats.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Création, signature et stockage d’une liste de certificats de confiance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513384"
---
# <a name="creating-signing-and-storing-a-ctl"></a>Création, signature et stockage d’une liste de certificats de confiance

Les procédures suivantes permettent de créer une [*liste de certificats de confiance*](../secgloss/c-gly.md) (CTL) signée et de l’enregistrer dans un magasin de [*certificats*](../secgloss/c-gly.md).

**Pour créer et signer une liste de certificats de confiance**

1.  Créez un tableau d’éléments à stocker dans la [*liste de certificats de confiance*](../secgloss/c-gly.md). Dans le cas de certificats approuvés, il doit s’agir des hachages SHA1 ou MD5 des certificats approuvés.
2.  Initialisez une structure d' [**\_ informations CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) qui comprend le tableau d’éléments que vous venez de créer.
3.  Initialise une structure [**d' \_ \_ \_ informations de codage signée par CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .
4.  Appelez [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl). Cet appel de fonction retourne un pointeur vers une liste de certificats de confiance (au \# format PKCS 7) signée qui contient la liste des éléments créés à l’étape 1.

**Pour ajouter une liste CTL à un magasin de certificats**

1.  Obtient un pointeur vers une liste de certificats de confiance (CTL) signée et encodée.
2.  Ouvrez le magasin de certificats cible avec un appel à [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
3.  Appelez [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).

 

 
