---
description: Lorsqu’un client démarre, il sélectionne un package de sécurité pour ses transactions avec un serveur, puis il contacte ce serveur. Un serveur sélectionne un ou plusieurs packages de sécurité et attend une connexion cliente.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Obtention d’informations sur les packages de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113807"
---
# <a name="getting-information-about-security-packages"></a>Obtention d’informations sur les packages de sécurité

Lorsqu’un client démarre, il sélectionne un [*package de sécurité*](/windows/desktop/SecGloss/s-gly) pour ses transactions avec un serveur, puis il contacte ce serveur. Un serveur sélectionne un ou plusieurs packages de sécurité et attend une connexion cliente.

Pour obtenir des informations spécifiques sur les packages de sécurité SSPI disponibles avec un SSP particulier, la fonction [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) peut être appelée pour récupérer une structure [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .

Pour récupérer la structure de sortie, l’appelant passe à la fonction l’adresse d’un pointeur vers le type de la structure de retour. La fonction alloue de la mémoire et retourne les données à l’appelant en affectant l’adresse du tampon de données de retour à l’argument. La Convention SSPI est que la fonction alloue de la mémoire pour la structure, et que l’application appelante libère cette mémoire à l’aide de [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).

L’appel de la fonction [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) récupère les attributs d’un [*package de sécurité*](/windows/desktop/SecGloss/s-gly). Le serveur et le client peuvent appeler la fonction **QuerySecurityPackageInfo** pour connaître la longueur maximale du jeton de sécurité du membre **cbMaxToken** de la structure [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) . Pour obtenir un exemple, consultez l’appel à la fonction **QuerySecurityPackageInfo** présentée dans [utilisation de SSPI avec un serveur Windows Sockets](using-sspi-with-a-windows-sockets-server.md).

Pour plus d’informations sur les fonctions de package, consultez [Package Management](authentication-functions.md).

 

 
