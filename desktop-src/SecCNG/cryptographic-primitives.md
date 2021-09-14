---
description: L’API CNG fournit un ensemble de fonctions qui effectuent des opérations de chiffrement de base telles que la création de hachages ou le chiffrement et le déchiffrement de données. Pour plus d’informations sur ces fonctions, consultez fonctions primitives de chiffrement CNG.
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: Primitives de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0f390b36bc500bf80b5b2ef0065651cf99f5e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013666"
---
# <a name="cryptographic-primitives"></a>Primitives de chiffrement

L’API CNG fournit un ensemble de fonctions qui effectuent des opérations de chiffrement de base telles que la création de hachages ou le chiffrement et le déchiffrement de données. Pour plus d’informations sur ces fonctions, consultez [fonctions primitives de chiffrement CNG](cng-cryptographic-primitive-functions.md).

CNG implémente de nombreux algorithmes de chiffrement. Chaque algorithme ou classe d’algorithmes expose sa propre API primitive. Plusieurs implémentations d’un algorithme donné peuvent être installées en même temps. Toutefois, une seule implémentation sera la valeur par défaut à un moment donné.

Chaque classe d’algorithme dans CNG est représentée par un routeur primitif. Les applications qui utilisent les fonctions primitives CNG sont liées au fichier binaire de routeur Bcrypt.dll en mode utilisateur, ou Ksecdd.sys en mode noyau avant d’appeler les fonctions. Diverses routines de routeur gèrent toutes les primitives d’algorithme. Ces routeurs suivent chaque implémentation d’algorithme installée sur le système et acheminent chaque appel de fonction vers le module de fournisseur primitif approprié.

CNG fournit des primitives pour les classes d’algorithmes suivantes.



| Classe d’algorithme                                                                                                                                                  | Description                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Générateur de nombres aléatoires<br/> | Génération de nombres aléatoires enfichables (RNG).<br/>                                                         |
| <span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hachage<br/>                                                                 | Algorithmes utilisés pour le hachage, tels que SHA1 et SHA2.<br/>                                               |
| <span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Chiffrement symétrique<br/>             | Algorithmes utilisés pour le chiffrement symétrique, tels que AES, 3DES et RC4.<br/>                             |
| <span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Chiffrement asymétrique<br/>         | Les algorithmes asymétriques (clé publique) qui prennent en charge le chiffrement, tels que RSA.<br/>                          |
| <span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature<br/>                                                         | Algorithmes de signature tels que DSA et ECDSA. Cette classe peut également être utilisée avec RSA.<br/>                 |
| <span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Accord secret<br/>                             | Les algorithmes d’accord secret tels que Diffie-Hellman (DH) et ECDH (Elliptic Curve Diffie-Hellman).<br/> |



 

L’illustration suivante montre la conception et la fonction des primitives de chiffrement CNG.

![conception et fonction des primitives de chiffrement CNG](images/ssdk-cng1c.png)

Le fichier d’en-tête bcrypt. h définit la constante du **\_ \_ fournisseur de la primitive MS** comme « fournisseur primitif Microsoft ». Pour utiliser le fournisseur primitif Microsoft, transmettez cette valeur à [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).

 

 




