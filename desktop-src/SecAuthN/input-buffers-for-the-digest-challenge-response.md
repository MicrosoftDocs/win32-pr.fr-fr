---
description: L’authentification HTTP à l’aide de Microsoft Digest requiert trois mémoires tampons d’entrée pour générer une réponse de stimulation. Le tableau suivant récapitule ces mémoires tampons.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Mémoires tampons d’entrée pour la réponse de stimulation Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011283"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a>Mémoires tampons d’entrée pour la réponse de stimulation Digest

L’authentification HTTP à l’aide de Microsoft Digest requiert trois mémoires tampons d’entrée pour générer une réponse de stimulation. Le tableau suivant récapitule ces mémoires tampons.



| Numéro de mémoire tampon | Contient                                                                                                                                             | Type de mémoire tampon                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| 0             | Défi reçu du serveur                                                                                                                   | \_jeton SECBUFFER                                            |
| 1             | Méthode HTTP                                                                                                                                          | \_paramètres SECBUFFER                                           |
| 2             | H (entité)                                                                                                                                            | \_paramètres SECBUFFER                                           |
| 3             | [*Nom de principal du service*](../secgloss/s-gly.md) (SPN) du serveur cible. | **SECBUFFER \_ \_** \| **SECBUFFER en \_ lecture seule** de l’hôte cible      |
| 4             | Valeurs de jeton des liaisons de canal                                                                                                                        | **SECBUFFER \_ \_liaisons de canal** \| **SECBUFFER \_ ReadOnly** |



 

La mémoire tampon zéro contient la stimulation du condensé reçue du serveur en réponse à la demande initiale d’une ressource protégée par l’accès.

La mémoire tampon 1 contient la représentation sous forme de chaîne de la méthode, telle que « obtient » ou « poster ». La méthode est utilisée dans le calcul de a2, comme décrit dans le [document RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).

La mémoire tampon 2 est le hachage [*MD5*](../secgloss/m-gly.md) du corps de l’entité du message, comme décrit dans le document RFC 2617.

La mémoire tampon 3 contient le nom principal de service du serveur cible au format UTF-8 quand Digest est utilisé avec les liaisons de canal.

Buffer 4 contient la valeur du jeton de liaison de canal quand Digest est utilisé avec les liaisons de canal.

## <a name="input-buffers-for-sasl"></a>Mémoires tampons d’entrée pour SASL

Mémoire tampon d’approvisionnement zéro uniquement. Pour la compatibilité avec d’autres SSP, vous pouvez appeler [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) sans une demande de serveur valide. Dans ce cas, le paramètre *pInput* doit avoir la valeur **null**.

 

 
