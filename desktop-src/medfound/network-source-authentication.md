---
description: Authentification de la source réseau
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Authentification de la source réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034157"
---
# <a name="network-source-authentication"></a>Authentification de la source réseau

Certains hôtes de média peuvent nécessiter des informations d’identification de l’utilisateur des applications clientes avant d’autoriser l’accès au média. Les informations d’identification de l’utilisateur incluent l’identification et la preuve d’identification, telles que le nom d’utilisateur et le mot de passe, qui sont utilisées par le serveur multimédia pour accorder l’accès à la source réseau qu’il héberge. La source réseau peut fournir une authentification NTLM, Digest ou de base.

Les applications basées sur Media Foundation peuvent stocker les informations d’identification de l’utilisateur pour une URL spécifique dans un objet *d’informations d’identification* qui expose l’interface [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) . L’objet Credential stocke les informations d’identification chiffrées et fournit des méthodes pour retourner des informations telles que le nom d’utilisateur, le mot de passe et le domaine.

Les objets d’informations d’identification sont créés et conservés dans un cache. L’objet de *cache des informations d’identification* , exposé par l’interface [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) fournit des méthodes pour récupérer les objets d’informations d’identification à partir du cache des informations d’identification.

Une application qui prend en charge l’authentification doit implémenter l’interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) . Media Foundation ne fournit pas d’implémentation par défaut de cette interface. Le gestionnaire d’informations d’identification est responsable de la collecte des informations d’identification requises pour une URL à partir de l’entrée de l’utilisateur ou de la lecture à partir du stockage persistant.

Cette section contient les rubriques suivantes :

-   [Définition d’un gestionnaire d’informations d’identification](setting-a-credential-manager.md)
-   [Utilisation du cache des informations d’identification](using-the-credential-cache.md)
-   [Implémentation de IMFNetCredentialManager](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



