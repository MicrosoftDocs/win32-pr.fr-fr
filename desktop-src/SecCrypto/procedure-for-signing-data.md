---
description: Affiche la relation entre les paramètres de fonction qui pointent vers des structures ou des tableaux et leurs données initialisées.
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: Procédure de signature des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba289928ab39c690e1c44bdbf65c77c18b7edab3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120845"
---
# <a name="procedure-for-signing-data"></a>Procédure de signature des données

Une seule fonction, [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage), effectue toutes les tâches listées dans la [création d’un message signé](creating-a-signed-message.md). Toutefois, l’initialisation des structures et d’autres données est toujours nécessaire. L’illustration suivante montre la relation entre les paramètres de fonction qui pointent vers des structures ou des tableaux et leurs données initialisées. L’illustration montre uniquement les paramètres de fonction et les membres de structure dérivés d’autres structures ou fonctions. Les autres paramètres sont des initialisations simples.

![mappage d’initialisation pour un appel à cryptsignmessage](images/crypsign.png)

**Pour signer des données à l’aide de CryptSignMessage**

1.  Obtient un pointeur vers les données à signer.
2.  Assignez le pointeur aux données pour indexer zéro d’un tableau de « données à signer ».
3.  Obtenir un handle pour le fournisseur de services de chiffrement.
4.  Ouvrez un [*magasin de certificats*](../secgloss/c-gly.md) qui contient le certificat du signataire.
5.  Procurez-vous une adresse dans le certificat du signataire.
6.  Assignez l’adresse du certificat à l’index zéro du tableau *MsgCert* .
7.  Assignez les adresses de tous les autres certificats à inclure avec le message dans le tableau *MsgCert* .
8.  Initialisez la structure d' [**\_ \_ identificateur d’algorithme**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) de chiffre, en initialisant le membre **pszObjId** avec l’algorithme de hachage souhaité et les autres membres, le cas échéant.
9.  Initialisez la structure du [**\_ \_ message \_ de signature**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) du chiffre, en initialisant le membre **pSigningCert** sur l’adresse du certificat du signataire, le membre du tableau **MsgCert** sur l’adresse du signataire et les certificats de l’autre, le membre **HashAlgorithm** à l’adresse de la structure de l’identificateur de l' [**\_ algorithme \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) de chiffrement et les autres membres, le cas échéant.
10. Appelez la fonction [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) , en passant la structure du [**\_ \_ message \_ de signature**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) de chiffre pour le paramètre *pSignPara* , l’adresse du tableau « données à signer » pour le paramètre *rgpbToBeSigned* , une adresse pour le paramètre de sortie *pbSignedBlob* et des valeurs pour les autres paramètres, le cas échéant.

 

 
