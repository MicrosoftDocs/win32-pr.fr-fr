---
description: Les méthodes suivantes sont définies par l’interface IOCSPAdmin. Les méthodes d’accès à la propriété ne sont pas indiquées ici. Pour afficher les propriétés de IOCSPAdmin, consultez Propriétés de IOCSPAdmin.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Méthodes de IOCSPAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecd14d2566c5e80e863ba06e38b2945492f59b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318514"
---
# <a name="methods-of-iocspadmin"></a>Méthodes de IOCSPAdmin

Les méthodes suivantes sont définies par l’interface [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) . Les méthodes d’accès à la propriété ne sont pas indiquées ici. Pour afficher les propriétés de **IOCSPAdmin**, consultez [Propriétés de IOCSPAdmin](properties-of-iocspadmin.md).



| Méthode                                                              | Description                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | Établit une connexion à un serveur répondeur OCSP (Online Certificate Status Protocol) et initialise un objet **OCSPAdmin** avec les informations de configuration du serveur.                                                                                                     |
| [**GetHashAlgorithms**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | Obtient une liste de noms d’algorithmes de hachage. Le serveur répondeur utilise l’un des algorithmes nommés pour signer les réponses OCSP pour une configuration d' [*autorité de certification*](../secgloss/c-gly.md) donnée. |
| [**GetMyRoles**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | Obtient le masque d’accès des rôles de privilège pour un utilisateur sur un serveur répondeur donné.                                                                                                                                                                                           |
| [**GetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | Obtient des informations de descripteur de sécurité pour un serveur répondeur.                                                                                                                                                                                                              |
| [**GetSigningCertificates**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | Obtient les certificats de signature disponibles sur un serveur répondeur pour un certificat d’autorité de certification donné.                                                                                                                                                                        |
| [**Ping**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | Teste une connexion DCOM avec un service de répondeur.                                                                                                                                                                                                                         |
| [**SetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | Met à jour un service de répondeur avec des modifications de configuration.                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | Met à jour les informations de descripteur de sécurité pour un serveur répondeur OCSP.                                                                                                                                                                                                     |



 

 

 
