---
description: Retourne les valeurs qu’un fournisseur de réseau peut définir.
ms.assetid: f8e6692f-4824-40fe-a5b3-9843689ea02e
title: Valeurs de retour de sécurité réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a362fde712d2a44565894aceb9d85172e488b53a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123366"
---
# <a name="network-security-return-values"></a>Valeurs de retour de sécurité réseau

Les valeurs de retour qu’un fournisseur réseau peut définir incluent les codes d’erreur suivants.



| Codes d’erreur         | Description                                                                                                                                                                                                                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WN- \_ réussite         | La fonction a réussi.                                                                                                                                                                                                                                                                                                                 |
| WN \_ non \_ pris en charge  | La fonction n’est pas prise en charge sur ce fournisseur de réseau.                                                                                                                                                                                                                                                                                 |
| \_erreur réseau \_ WN      | Une erreur réseau inconnue s’est produite.                                                                                                                                                                                                                                                                                                       |
| WN \_ plus de \_ données      | La mémoire tampon de données transmise est insuffisante pour contenir toutes les données disponibles.                                                                                                                                                                                                                                                         |
| WN \_ pointeur incorrect \_    | Un pointeur qui n’est pas valide a été spécifié lors de l’appel de fonction.                                                                                                                                                                                                                                                                     |
| WN \_ valeur incorrecte \_      | Une valeur numérique non valide a été spécifiée lors de l’appel de la fonction.                                                                                                                                                                                                                                                               |
| WN \_ \_ mot de passe incorrect   | Un mot de passe incorrect a été spécifié.                                                                                                                                                                                                                                                                                                    |
| \_accès à la WN \_ refusé  | L’appelant ne dispose pas des autorisations suffisantes pour terminer l’opération.                                                                                                                                                                                                                                                              |
| \_fonction WN \_ occupée  | Cette fonction ne peut pas être réentrée et est actuellement utilisée, ou le fournisseur est toujours en cours d’initialisation et n’est pas encore prêt à être appelé. Le fournisseur doit retourner ce code d’erreur uniquement s’il est disponible. Ce code de retour est transmis par le MPR à son appelant et est susceptible d’entraîner une nouvelle tentative de l’appelant.<br/> |
| \_erreur Windows \_ WN  | Une fonction requise a échoué.                                                                                                                                                                                                                                                                                                             |
| WN \_ utilisateur incorrect \_       | Un nom d’utilisateur non valide a été spécifié.                                                                                                                                                                                                                                                                                            |
| \_mémoire insuffisante \_ \_ | La mémoire est insuffisante pour terminer l’opération.                                                                                                                                                                                                                                                                                 |
| WN \_ non \_ connecté  | L’appareil n’est pas redirigé.                                                                                                                                                                                                                                                                                                           |
| WN \_ ouvre les \_ fichiers     | Impossible d’annuler la connexion, car des fichiers sont toujours ouverts.                                                                                                                                                                                                                                                                      |
| WN \_ \_ NetName incorrect    | Le nom réseau n’est pas valide.                                                                                                                                                                                                                                                                                                          |



 

 

 




