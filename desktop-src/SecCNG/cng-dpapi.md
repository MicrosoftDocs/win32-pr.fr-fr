---
description: Microsoft a introduit l’interface de programmation d’applications de protection des données (DPAPI) dans Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: DPAPI CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0273522580c806caa5fe7848ff32a2017cfb37c4499dee21f5a3787ecae57b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908628"
---
# <a name="cng-dpapi"></a>DPAPI CNG

Microsoft a introduit l’interface de programmation d’applications de protection des données (DPAPI) dans Windows 2000. L’API se compose de deux fonctions, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata). DPAPI fait partie de CryptoAPI et était destiné aux développeurs qui savent très peu utiliser le chiffrement. Les deux fonctions peuvent être utilisées pour chiffrer et déchiffrer des données statiques sur un seul ordinateur.

Toutefois, le Cloud Computing requiert souvent que le contenu chiffré sur un ordinateur soit déchiffré sur un autre. par conséquent, à partir de Windows 8, Microsoft a étendu l’idée d’utiliser une API relativement simple pour englober les scénarios de cloud. Cette nouvelle API, appelée DPAPI-GN, vous permet de partager en toute sécurité des secrets (clés, mots de passe, matériel de clé) et des messages en les protégeant sur un ensemble de principaux qui peuvent être utilisés pour les déprotéger sur des ordinateurs différents après une authentification et une autorisation appropriées. Les principaux suivants sont actuellement pris en charge :

-   Groupe dans une forêt Active Directory.
-   Informations d’identification Web.

Pour plus d'informations, voir les rubriques suivantes :

-   [Fournisseurs de protection](protection-providers.md)
-   [Descripteurs de protection](protection-descriptors.md)
-   [Format de données protégées](protected-data-format.md)

DPAPI-GN est basé sur le CNG (Cryptography Next Generation) et comprend les fonctions suivantes :

-   [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [**NCryptCloseProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [**NCryptProtectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [**NCryptQueryProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [**NCryptStreamClose**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [**NCryptStreamOpenToProtect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [**NCryptStreamOpenToUnprotect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [**NCryptStreamUpdate**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [**NCryptUnprotectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
