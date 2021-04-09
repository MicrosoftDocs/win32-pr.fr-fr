---
description: CryptoAPI fournit des fonctions permettant d’utiliser des certificats, des listes de révocation de certificats (CRL) et des listes de certificats de confiance (CTL).
ms.assetid: 23460329-44ed-4bcb-9727-5c841070f093
title: Opérations avec certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2f9f5d6d541b452741f2e4634752b979f26107
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867397"
---
# <a name="operations-with-certificates"></a>Opérations avec certificats

[*CryptoAPI*](../secgloss/c-gly.md) fournit des fonctions permettant d’utiliser des [*certificats*](../secgloss/c-gly.md), des [*listes de révocation de certificats*](../secgloss/c-gly.md) (CRL) et des listes de certificats de [*confiance*](../secgloss/c-gly.md) (CTL). Celles-ci incluent des fonctions de conversion de types encodés en types de contexte, des fonctions qui dupliquent des objets et des fonctions qui libèrent ces objets. Ces fonctions encodent les informations dans des contextes, mais n’ajoutent pas ce contexte à un magasin. Ces fonctions sont [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), [**CertCreateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)et [**CertCreateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext). Utilisez la fonction CertFree appropriée pour libérer des contextes créés par l’une de ces fonctions.

Les fonctions CryptoAPI pour dupliquer des certificats, des listes de révocation de certificats et des listes CTL incrémentent le [*compteur de référence*](../secgloss/r-gly.md) dans le contexte spécifié et retournent un pointeur vers le contexte. Les fonctions de duplication n’allouent pas d’espace supplémentaire ou copient les données d’un contexte dans un nouvel emplacement de mémoire. Ces fonctions sont [**CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext), [**CertDuplicateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)et [**CertDuplicateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext). Les contextes créés avec l’une de ces fonctions doivent être libérés à l’aide de la fonction CertFree appropriée.

Les fonctions CryptoAPI qui libèrent des certificats, des listes de révocation de certificats et des listes CTL sont [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)et [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext). Chacune de ces fonctions réduit le [*nombre de références*](../secgloss/r-gly.md) dans un contexte. Si le décompte de références atteint zéro, la mémoire allouée pour le contexte est libérée.

Pour obtenir la liste complète des fonctions permettant de travailler avec des certificats, des listes de révocation de certificats et des listes de certificats de confiance, consultez fonctions de maintenance des certificats [et](cryptography-functions.md)des certificats, [fonctions de certificats](cryptography-functions.md), fonctions de liste de [révocation de certificats](cryptography-functions.md)et fonctions de listes de certificats de [confiance](cryptography-functions.md).

 

 
