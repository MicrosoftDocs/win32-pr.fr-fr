---
description: Les fournisseurs implémentent des algorithmes de chiffrement, génèrent des clés, fournissent un stockage de clés et authentifient les utilisateurs. Les fournisseurs peuvent être implémentés dans le matériel, les logiciels ou les deux.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Comprendre les fournisseurs de services de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952558"
---
# <a name="understanding-cryptographic-providers"></a>Comprendre les fournisseurs de services de chiffrement

Le concept de fournisseur de services de chiffrement introduit dans l’API de chiffrement ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) et qui a évolué quelque peu dans l' [*API de chiffrement : Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) est essentiel à l’implémentation sécurisée des fonctionnalités de chiffrement sur les systèmes d’exploitation Microsoft. Ces deux SDK ont été utilisés pour créer de nombreuses applications et sont appelés en interne par d’autres kits de développement logiciel (SDK). Par exemple, Active Directory Services de certificats et l’API d’inscription de certificats s’appuient sur CryptoAPI et CNG.

En général, les fournisseurs implémentent des algorithmes de chiffrement, génèrent des clés, fournissent un stockage de clés et authentifient les utilisateurs. Les fournisseurs peuvent être implémentés dans le matériel, les logiciels ou les deux. Les applications générées à l’aide d’CryptoAPI ou CNG ne peuvent pas modifier les clés créées par les fournisseurs, et elles ne peuvent pas modifier l’implémentation de l’algorithme de chiffrement. Les différents fournisseurs créés par Microsoft sont distribués avec les systèmes d’exploitation. D’autres fournisseurs ont été créés et distribués par des tiers.

Les rubriques suivantes mettent en évidence les différences entre les fournisseurs associés à CryptoAPI et celles associées à CNG. En règle générale, cette documentation fait référence aux fournisseurs sans référence au kit de développement logiciel (SDK) auquel ils sont associés, en notant l’Association uniquement lorsqu’elle est pertinente.

-   [Fournisseurs de services de chiffrement CryptoAPI](cryptoapi-cryptographic-service-providers.md)
-   [Fournisseurs d’algorithmes de chiffrement CNG](cng-cryptographic-algorithm-providers.md)
-   [Fournisseurs de stockage de clés CNG](cng-key-storage-providers.md)
-   [Énumération des fournisseurs installés](enumerating-installed-providers.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’API d’inscription de certificats](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
