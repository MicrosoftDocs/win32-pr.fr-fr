---
description: L’un des avantages de l’utilisation des listes de certificats de confiance (CTL) est que les applications peuvent être conçues pour vérifier automatiquement les messages signés par rapport à des certificats approuvés sans déranger l’utilisateur avec des boîtes de dialogue.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Vérification des messages signés à l’aide de listes CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1624a132ed976800d1c8a8ab0dcd878f533f0d0b947879e87e3e8dc21ccff51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896230"
---
# <a name="verifying-signed-messages-by-using-ctls"></a>Vérification des messages signés à l’aide de listes CTL

L’un des avantages de l’utilisation des [*listes de certificats de confiance*](../secgloss/c-gly.md) (CTL) est que les applications peuvent être conçues pour vérifier automatiquement les messages signés par rapport à des certificats approuvés sans déranger l’utilisateur avec des boîtes de dialogue. Il permet également de faire confiance aux sources de contrôle de l’administrateur réseau.

La procédure suivante peut être utilisée pour vérifier la signature d’un message signé à l’aide d’une liste CTL.

**Pour vérifier un message signé à l’aide d’une liste de certificats de confiance**

1.  Décodez le message comme suit :

    1.  Obtient un pointeur vers le message reçu (l' [*objet BLOB*](../secgloss/b-gly.md)encodé).
    2.  Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), en passant les arguments nécessaires.
    3.  Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) une fois, en passant le handle récupéré à l’étape b et un pointeur vers les données qui doivent être décodées. Cela entraîne le suivi des actions appropriées sur le message, en fonction du type de message.

2.  Vérifiez la signature du message décodé, signé, et récupérez un pointeur vers le [**\_ contexte de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)du signataire.

    Pour ce faire, vous pouvez appeler [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), en passant le handle de message récupéré à l’étape 1C comme paramètre *hCryptMsg* . Si l’appel de fonction retourne la **valeur true**, la signature a été vérifiée et un pointeur vers [**le \_ contexte PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) du signataire est retourné dans le paramètre *ppSigner* .

3.  Vérifiez que le signataire est une source approuvée comme suit :

    1.  Ouvrez le magasin de certificats contenant la liste CTL appropriée.
    2.  Obtient un pointeur vers le [**\_ contexte**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) de la liste de certificats de confiance en appelant [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
    3.  Pour confirmer que le signataire est une source approuvée, appelez [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), en passant le pointeur récupéré à l’étape précédente dans le paramètre *pCtlContext* , le \_ \_ type de sujet du certificat CTL \_ dans le paramètre *DwSubjectType* et le pointeur vers le [**\_ contexte de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) récupéré à l’étape 2 dans le paramètre *pvSubject* . Si l’appel de fonction retourne la **valeur true**, le **\_ contexte de certificat** transmis à la fonction est une source approuvée dans la liste de certificats de confiance.

 

 
