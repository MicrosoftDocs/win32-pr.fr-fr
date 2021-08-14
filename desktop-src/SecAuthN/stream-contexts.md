---
description: Les contextes de flux gèrent les protocoles orientés flux sécurisés, tels que SSL ou PCT.
ms.assetid: 05a6b036-1f7f-473f-9813-a1e1534e0f0d
title: Contextes de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c843889df6aec3f82e8cb8516a7c23ccbf7a6de9957f9a0c572f6e6ca63ac75d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916678"
---
# <a name="stream-contexts"></a>Contextes de flux

Les contextes de flux gèrent les protocoles orientés flux sécurisés, tels que SSL ou PCT. Dans l’intérêt du partage de la même interface et de la gestion des informations d’identification similaires, SSPI assure la prise en charge des contextes de flux. Le [*protocole de sécurité*](../secgloss/s-gly.md) intègre le schéma d’authentification et les formats d’enregistrement du flux.

Pour fournir des protocoles orientés flux, les [*packages de sécurité*](../secgloss/s-gly.md) qui prennent en charge les contextes de flux présentent les caractéristiques de processus suivantes :

-   Le package définit l' \_ \_ indicateur de flux de l’indicateur SECPKG pour indiquer qu’il prend en charge la sémantique de flux.
-   Les applications de transport demandent la sémantique de flux en définissant les indicateurs du flux de demande ISC \_ \_ et du \_ \_ flux de demande ASC dans les appels aux fonctions [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) et [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
-   L’application appelle la fonction [**QueryContextAttributes (général)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) avec une structure [**SecPkgContext \_ StreamSizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes) pour interroger le contexte de [*sécurité*](../secgloss/s-gly.md) en fonction du nombre de mémoires tampons à fournir et des tailles à réserver pour les en-têtes ou les codes de fin.
-   L’application fournit des descripteurs de mémoire tampon à Spare pendant le traitement réel des données. En spécifiant la sémantique de flux, l’appelant indique la volonté d’effectuer un traitement supplémentaire afin que le [*package de sécurité*](../secgloss/s-gly.md) puisse gérer le blocage des messages. Par essence, pour les fonctions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) et [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) , l’appelant transmet une liste de mémoires tampons. Lorsqu’un message est reçu d’un canal orienté en continu (par exemple, un port TCP), l’appelant passe dans une liste de tampons comme suit.

    | Buffer | Longueur         | Type de mémoire tampon      |
    |--------|----------------|------------------|
    | 1      | Longueur du message | \_données SECBUFFER  |
    | 2      | 0              | SECBUFFER \_ vide |
    | 3      | 0              | SECBUFFER \_ vide |
    | 4      | 0              | SECBUFFER \_ vide |
    | 5      | 0              | SECBUFFER \_ vide |

    

     

    Le package de sécurité fonctionne alors sur l' [*objet BLOB*](../secgloss/b-gly.md). Si la fonction est correctement retournée, la liste de mémoires tampons se présente comme suit.

    

    | Buffer | Longueur         | Type de mémoire tampon                |
    |--------|----------------|----------------------------|
    | 1      | Longueur de l’en-tête  | \_ \_ en-tête de flux SECBUFFER  |
    | 2      | Longueur des données    | \_données SECBUFFER            |
    | 3      | Longueur de la remorque | Code de fin de \_ flux SECBUFFER \_ |
    | 4      | 0              | SECBUFFER \_ vide           |
    | 5      | 0              | SECBUFFER \_ vide           |

    

     

    Le package aurait peut-être également retourné buffer \# 4 avec la longueur x et le type de tampon SECBUFFER, \_ indiquant que les données de ce tampon font partie de l’enregistrement suivant et n’ont pas encore été traitées. À l’inverse, si la fonction de message retourne le \_ code d’erreur sec E \_ message incomplet \_ , la liste de tampons retournée ressemble à ce qui suit.

    

    | Buffer | Longueur | Type de mémoire tampon        |
    |--------|--------|--------------------|
    | 1      | x      | SECBUFFER \_ manquant |

    

     

    Cela indique qu’un plus grand nombre de données était nécessaire pour traiter l’enregistrement. Contrairement à la plupart des erreurs retournées par une fonction de message, ce type de mémoire tampon n’indique pas que le contexte a été compromis. Au lieu de cela, cela indique qu’un plus grand nombre de données est nécessaire. les [*packages de sécurité*](../secgloss/s-gly.md) ne doivent pas mettre à jour leur [*État*](../secgloss/s-gly.md) dans cette condition.

    De même, du côté de l’expéditeur de la communication, l’appelant peut appeler la fonction [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) . Le package de sécurité doit peut-être réallouer la mémoire tampon ou copier des éléments. L’appelant peut être plus efficace en fournissant une liste de tampons comme suit.

    

    | Buffer | Longueur         | Type                       |
    |--------|----------------|----------------------------|
    | 1      | Longueur de l’en-tête  | \_ \_ en-tête de flux SECBUFFER  |
    | 2      | Longueur des données    | \_données SECBUFFER            |
    | 3      | Longueur de la remorque | Code de fin de \_ flux SECBUFFER \_ |

    

     

    Cela permet à l’appelant d’utiliser plus efficacement les mémoires tampons. En appelant la fonction [**QueryContextAttributes**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) pour déterminer la quantité d’espace à réserver avant d’appeler [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), l’opération est plus efficace pour l’application et le package de sécurité.

 

 
