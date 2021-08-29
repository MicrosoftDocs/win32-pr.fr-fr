---
description: 'Contrairement à l’API de chiffrement (CryptoAPI), API de chiffrement : Next Generation (CNG) sépare les fournisseurs de chiffrement des fournisseurs de stockage de clés (KSP).'
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: fournisseurs de Stockage de clé CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edef5858f4df370c7495c8796b552e00c080cc6a9da75e34fc21216bf2adc7bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670229"
---
# <a name="cng-key-storage-providers"></a>fournisseurs de Stockage de clé CNG

Contrairement à l’API de chiffrement (CryptoAPI), API de chiffrement : Next Generation (CNG) sépare les fournisseurs de chiffrement des fournisseurs de stockage de clés (KSP). KSP peut être utilisé pour créer, supprimer, exporter, importer, ouvrir et stocker des clés. En fonction de l’implémentation, elles peuvent également être utilisées pour le chiffrement asymétrique, l’accord secret et la signature. Microsoft installe les ksp suivants à partir de Windows Vista et Windows Server 2008. Les fournisseurs peuvent créer et installer d’autres fournisseurs.

## <a name="microsoft-software-key-storage-provider"></a>fournisseur de Stockage de clés logicielles Microsoft

Prend en charge la création et le stockage des clés logicielles, ainsi que les algorithmes suivants.



| Algorithm                                          | Objectif                           | Longueur de la clé (bits)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                | Accord secret et échange de clé | 512 à 4096 par incréments de 64 bits  |
| Algorithme de signature numérique (DSA)                  | Signatures                        | 512 à 1024 par incréments de 64 bits  |
| ECDH (Elliptic Curve Diffie-Hellman)               | Accord secret et échange de clé | P256, P384, P521                  |
| Algorithme ECDSA (Elliptic Curve Digital Signature Algorithm) | Signatures                        | P256, P384, P521                  |
| RSA                                                | Chiffrement et signature asymétriques | 512 à 16384 par incréments de 64 bits |



 

## <a name="microsoft-smart-card-key-storage-provider"></a>fournisseur de Stockage de clés de carte à puce Microsoft

Prend en charge la création et le stockage des clés de carte à puce, ainsi que les algorithmes suivants.



| Algorithm                                          | Objectif                           | Longueur de la clé (bits)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                | Accord secret et échange de clé | 512 à 4096 par incréments de 64 bits  |
| ECDH (Elliptic Curve Diffie-Hellman)               | Accord secret et échange de clé | P256, P384, P521                  |
| Algorithme ECDSA (Elliptic Curve Digital Signature Algorithm) | Signatures                        | P256, P384, P521                  |
| RSA                                                | Chiffrement et signature asymétriques | 512 à 16384 par incréments de 64 bits |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Identificateurs d’algorithme CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[fonctions de Stockage de clé CNG](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[Comprendre les fournisseurs de services de chiffrement](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
