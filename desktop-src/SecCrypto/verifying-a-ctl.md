---
description: Pour compliquer la tâche d’un Interloper pour remplacer une liste de certificats de confiance (CTL) erronée pour une liste existante, vérifiez la signature sur la liste CTL chaque fois que la liste CTL est utilisée.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Vérification d’une liste CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1068e26250f857893e0d5016962cf8df4f27adb137676d1d61af3254b5edabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970963"
---
# <a name="verifying-a-ctl"></a>Vérification d’une liste CTL

Pour compliquer la tâche d’un Interloper pour remplacer une liste de [*certificats de confiance*](../secgloss/c-gly.md) (CTL) erronée pour une liste existante, vérifiez la signature sur la liste CTL chaque fois que la liste CTL est utilisée. N’utilisez pas de liste CTL qui ne contient pas de signature approuvée.

**Pour vérifier une signature CTL**

1.  Ouvrez le [*magasin de certificats*](../secgloss/c-gly.md) contenant la liste de certificats de confiance souhaitée.
2.  Obtient un handle vers un [**\_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) pour la liste CTL. Pour ce faire, vous pouvez appeler l’une des fonctions qui retournent un handle vers le **\_ contexte** de la liste de certificats de confiance, par exemple [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
3.  Appelez [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), en passant [**le \_ contexte**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) de la liste de certificats de confiance récupéré à l’étape 2 dans le paramètre *hCryptMsg* , un descripteur du magasin de certificats contenant le certificat de la source approuvée pour les listes CTL dans le paramètre *rghSignerStore* et l' \_ indicateur de signataire approuvé CMSG \_ \_ dans le paramètre *dwFlags* . Si la fonction retourne la **valeur true**, la signature a été vérifiée et un pointeur vers le [**\_ contexte PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) du signataire de la liste de certificats de confiance est retourné dans le paramètre *ppSigner* .

 

 
