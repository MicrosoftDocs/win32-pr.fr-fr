---
description: Les méthodes suivantes sont définies par l’interface IOCSPAdmin. Les méthodes d’accès à la propriété ne sont pas indiquées ici. Pour afficher les propriétés de IOCSPAdmin, consultez Propriétés de IOCSPAdmin.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Méthodes de IOCSPAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a455ae5cfbb49d60cc0d0a03265d05c98efa2f2217746086b0acf0a4230709dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992849"
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



 

 

 
