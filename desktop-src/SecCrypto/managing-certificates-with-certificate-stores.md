---
description: Utilisation des fonctions CryptoAPI pour gérer les magasins de certificats et les certificats, les listes de révocation de certificats et les listes de certificats de confiance dans ces banques.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Gestion des certificats avec des magasins de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98abb2b612f77db3f1c59e53fb9c7bf0f34cefb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567391"
---
# <a name="managing-certificates-with-certificate-stores"></a>Gestion des certificats avec des magasins de certificats

Sur une période donnée, les [*certificats*](../secgloss/c-gly.md) s’accumulent sur l’ordinateur d’un utilisateur. Les outils sont requis pour gérer ces certificats. [*CryptoAPI*](../secgloss/c-gly.md) fournit ces outils comme fonctions pour stocker, récupérer, supprimer, répertorier (énumérer) et vérifier des certificats. CryptoAPI offre également la possibilité de joindre des certificats aux messages.

CryptoAPI offre deux catégories principales de fonctions pour la gestion des certificats : les fonctions qui gèrent les [*magasins de certificats*](../secgloss/c-gly.md)et les fonctions qui fonctionnent avec les certificats, les [*listes de révocation de certificats*](../secgloss/c-gly.md) (CRL) et les listes de certificats de [*confiance*](../secgloss/c-gly.md) (CTL) au sein de ces banques.

Les fonctions qui gèrent [*les magasins de certificats*](../secgloss/c-gly.md) incluent des fonctions permettant de travailler avec des magasins logiques ou [*virtuels*](../secgloss/v-gly.md), des magasins [*distants*](../secgloss/r-gly.md), des [*magasins externes*](../secgloss/e-gly.md)et des magasins qui peuvent être déplacés.

Les certificats, les [*listes de révocation*](../secgloss/c-gly.md)de certificats et les [*listes CTL*](../secgloss/c-gly.md) peuvent être conservés et gérés dans les [*magasins de certificats*](../secgloss/c-gly.md). Ils peuvent être récupérés à partir d’un magasin dans lequel ils ont été rendus persistants pour une utilisation dans les processus d’authentification.

Le [*magasin de certificats*](../secgloss/c-gly.md) est central pour toutes les fonctionnalités de certificat. Les certificats sont gérés dans le magasin à l’aide de fonctions avec un préfixe « CERT ». Un magasin de certificats standard est une liste liée de [*certificats*](../secgloss/c-gly.md) , comme indiqué dans l’illustration suivante.

![magasin de certificats](images/certstore1.png)

L’illustration précédente présente :

-   Chaque [*magasin de certificats*](../secgloss/c-gly.md) a un pointeur vers le premier bloc de certificat de ce magasin.
-   Un bloc de certificat comprend un pointeur vers les données de ce certificat et un pointeur « suivant » vers le bloc de certificat suivant dans le magasin.
-   Le pointeur « suivant » dans le dernier bloc de certificat est défini sur **null**.
-   Le bloc de données d’un certificat contient le contexte de certificat en lecture seule et toutes les propriétés étendues du certificat.
-   Le bloc de données de chaque certificat contient un [*nombre de références*](../secgloss/r-gly.md) qui effectue le suivi du nombre de pointeurs vers le certificat qui existe.

Les certificats dans un [*magasin de certificats*](../secgloss/c-gly.md) sont normalement conservés dans un certain type de stockage permanent, tel qu’un fichier de disque ou le registre système. Les magasins de certificats peuvent également être créés et ouverts strictement en mémoire. Un magasin de mémoire fournit un stockage de certificats temporaire pour l’utilisation de certificats qui n’ont pas besoin d’être conservés.

Les emplacements de magasin supplémentaires permettent de conserver et de rechercher des magasins dans différentes parties du registre d’un ordinateur local ou, avec les autorisations appropriées définies, dans le registre d’un ordinateur distant.

Chaque utilisateur a un mon magasin personnel dans lequel les certificats de cet utilisateur sont stockés. Mon magasin peut se trouver dans n’importe quel autre emplacement physique, y compris le registre sur un ordinateur local ou distant, un fichier disque, une base de données, un service d’annuaire, une [*carte à puce*](../secgloss/s-gly.md)ou un autre emplacement. Si un certificat peut être stocké dans le magasin My, ce magasin doit être réservé pour les certificats personnels d’un utilisateur : les certificats utilisés pour signer et déchiffrer les messages de cet utilisateur.

L’utilisation de certificats pour l’authentification dépend de l’émission de certificats émis par un émetteur de certificat approuvé. Les certificats pour les émetteurs de certificats approuvés sont généralement conservés dans le magasin racine, qui est actuellement conservé dans une sous-clé de registre. Dans le contexte CryptoAPI, le magasin racine est protégé et les boîtes de dialogue de l’interface utilisateur rappellent à l’utilisateur de placer uniquement les certificats approuvés dans ce magasin. Dans les situations de réseau d’entreprise, les certificats peuvent être envoyés (copiés) par un administrateur système à partir de l’ordinateur contrôleur de domaine vers les magasins racine sur les ordinateurs clients. Ce processus fournit à tous les membres d’un domaine des listes de confiance similaires.

D’autres certificats peuvent être stockés dans le magasin système de l' [*autorité de certification*](../secgloss/c-gly.md) ou dans des magasins de fichiers créés par l’utilisateur.

Pour obtenir la liste des fonctions permettant d’utiliser et de gérer des magasins de certificats, consultez [fonctions du magasin de certificats](cryptography-functions.md).

Pour obtenir un exemple d’utilisation de certaines de ces fonctions, consultez [exemple de programme C : opérations du magasin de certificats](example-c-program-certificate-store-operations.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de l’état d’un magasin de certificats](managing-a-certificate-store-state.md)
</dt> <dt>

[Utilisation de certificats dans les magasins de certificats](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[Liens de certificat](certificate-links.md)
</dt> <dt>

[Magasins de collection](collection-stores.md)
</dt> <dt>

[Magasins logiques et physiques](logical-and-physical-stores.md)
</dt> <dt>

[Emplacements du magasin système](system-store-locations.md)
</dt> <dt>

[Migration du magasin de certificats](certificate-store-migration.md)
</dt> </dl>

 

 
