---
description: "Windows Les fonctions et les méthodes d’acquisition d’images (WIA) peuvent retourner des codes d’erreur de la liste suivante : erreur CodeMeaningCodeWIA l' \\_ \\_ appareil BUSYThe est occupé."
ms.assetid: 3abbe92b-32b7-4820-b208-45c847243078
title: Codes d’erreur (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6025616d46a5973692bb3cafbcf88e18836ad0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220012"
---
# <a name="error-codes-wia"></a>Codes d’erreur (WIA)

Windows Les fonctions et les méthodes d’acquisition d’images (WIA) peuvent retourner des codes d’erreur de la liste suivante : 

| Code d'erreur                                      | Signification                                                                                                                                                                                                                             | Code       |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| \_erreur WIA \_ occupée                                | L’appareil est occupé. Fermez toutes les applications qui utilisent cet appareil ou attendez qu’elles se terminent, puis réessayez.                                                                                                                          | 0x80210006 |
| \_couverture d’erreur WIA \_ \_ ouverte                         | Une ou plusieurs des couvertures de l’appareil sont ouvertes.                                                                                                                                                                                          | 0x80210016 |
| \_communication des \_ appareils d’erreur WIA \_               | Échec de la communication avec l’appareil WIA. Assurez-vous que l’appareil est sous tension et connecté au PC. Si le problème persiste, déconnectez et reconnectez l’appareil.                                                            | 0x8021000A |
| \_périphérique d’erreur WIA \_ \_ verrouillé                      | L’appareil est verrouillé. Fermez toutes les applications qui utilisent cet appareil ou attendez qu’elles se terminent, puis réessayez.                                                                                                                        | 0x8021000D |
| \_ \_ exception d’erreur WIA dans le \_ \_ pilote               | Le pilote de périphérique a levé une exception.                                                                                                                                                                                               | 0x8021000E |
| \_ \_ erreur générale de l’erreur WIA \_                      | Une erreur inconnue s’est produite avec l’appareil WIA.                                                                                                                                                                                  | 0x80210001 |
| \_paramètre matériel d’erreur WIA \_ incorrect \_ \_        | Un paramètre incorrect a été défini sur l’appareil WIA.                                                                                                                                                                                    | 0x8021000C |
| \_commande d’erreur WIA \_ non valide \_                    | L’appareil ne prend pas en charge cette commande.                                                                                                                                                                                            | 0x8021000B |
| \_réponse du pilote d’erreur WIA \_ non valide \_ \_           | La réponse du pilote n’est pas valide.                                                                                                                                                                                            | 0x8021000F |
| \_élément d’erreur WIA \_ \_ supprimé                       | L’appareil WIA a été supprimé. Elle n’est plus disponible.                                                                                                                                                                               | 0x80210009 |
| \_lampe d’erreur WIA \_ \_ désactivée                           | La lampe du scanneur est désactivée.                                                                                                                                                                                                          | 0x80210017 |
| \_ \_ nombre maximal d' \_ \_ approuveurs d’erreurs d’imprimante WIA \_ | Un travail d’analyse a été interrompu, car un élément d’imscanneur/d’endosseur a atteint le nombre maximal de valeurs valides pour l’option d' \_ \_ endosseur d’imprimante IPS WIA \_ \_ et a été réinitialisé à 0. cette fonctionnalité est disponible avec Windows 8 et les versions ultérieures de Windows. | 0x80210021 |
| \_multi- \_ \_ flux d’erreur WIA                         | Une erreur d’analyse s’est produite en raison d’une condition de flux de page multiple. cette fonctionnalité est disponible avec Windows 8 et les versions ultérieures de Windows.                                                                                            | 0x80210020 |
| \_erreur WIA \_ en mode hors connexion                             | L’appareil est hors connexion. Assurez-vous que l’appareil est sous tension et connecté au PC.                                                                                                                                                  | 0x80210005 |
| \_papier d’erreur WIA \_ \_ vide                        | Il n’y a aucun document dans le chargeur de documents.                                                                                                                                                                                      | 0x80210003 |
| \_ \_ bourrage papier sur les erreurs WIA \_                          | Le papier est coincé dans le chargeur de documents du scanneur.                                                                                                                                                                                   | 0x80210002 |
| \_problème de \_ papier d’erreur WIA \_                      | Un problème non spécifié s’est produit avec le chargeur de documents du scanneur.                                                                                                                                                                 | 0x80210004 |
| \_erreur WIA lors du \_ préchauffage \_                         | L’appareil est en état de préchauffage.                                                                                                                                                                                                           | 0x80210007 |
| INTERVENTION de l' \_ utilisateur d’erreur WIA \_ \_                  | Il y a un problème avec l’appareil WIA. Assurez-vous que l’appareil est allumé, en ligne et que tous les câbles sont correctement connectés.                                                                                                      | 0x80210008 |
| WIA \_ - \_ aucun \_ appareil \_ disponible                   | Aucun périphérique scanneur n’a été trouvé. Assurez-vous que l’appareil est en ligne, connecté au PC et que le pilote approprié est installé sur le PC.                                                                                                   | 0x80210015 |



 

 

 



