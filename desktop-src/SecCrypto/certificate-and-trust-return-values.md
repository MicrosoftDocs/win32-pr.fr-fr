---
description: Répertorie les valeurs de retour du certificat et de l’approbation du certificat. Ces valeurs sont contenues dans le fichier d’en-tête winerror. h.
ms.assetid: f7d1bdcb-8e4f-493f-ad3c-9d4b9d21436b
title: Valeurs de retour de certificat et d’approbation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf575df785160682c132f38ccc280bb8b9377b15b64ed3efda163c68c1ef52e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127239"
---
# <a name="certificate-and-trust-return-values"></a>Valeurs de retour de certificat et d’approbation

Le tableau suivant répertorie les valeurs de retour du certificat et de l’approbation du certificat. Ces valeurs sont contenues dans le fichier d’en-tête winerror. h.



| Nom                            | Description                                                                                                                    | Valeur      |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------|------------|
| CERTIFICAT \_ E \_ critique               | Un certificat contient une extension inconnue qui est marquée comme « critique ».                                                         | 0x800B0105 |
| nom du certificat \_ \_ non valide \_          | Le certificat a un nom qui n’est pas valide. Le nom est soit non inclus dans la liste autorisée soit explicitement exclu. | 0x800B0114 |
| CERTIFICAT \_ E \_ - \_ stratégie non valide        | Le certificat a une stratégie qui n’est pas valide.                                                                                | 0x800B0113 |
| CERTIFICAT \_ E \_ ISSUERCHAINING         | Le parent d’un certificat donné n’a en fait pas émis ce certificat enfant.                                                  | 0x800B0107 |
| CERTIFICAT \_ E \_ mal formé              | Un certificat est manquant ou a une valeur vide pour un champ important, tel qu’un objet ou un nom d’émetteur.                       | 0x800B0108 |
| CERTIFICAT \_ E \_ PATHLENCONST           | Une contrainte de longueur du chemin d'accès dans la chaîne de certification a été violée.                                                         | 0x800B0104 |
| CERTIFICAT \_ E \_ UNTRUSTEDCA            | Une chaîne de certification a été traitée correctement, mais l’un des certificats de l’autorité de certification n’est pas approuvé par le fournisseur de stratégie.               | 0x800B0112 |
| chiffrer \_ E \_ aucun \_ contrôle de révocation \_ | La fonction de révocation n’a pas pu vérifier la révocation du certificat.                                                    | 0x80092012 |
| CONFIANCE \_ E \_ condensé incorrect \_           | La signature numérique de l'objet n'a pas été vérifiée.                                                                            | 0x80096010 |
| APPROUVER \_ les \_ contraintes de base E \_    | L'extension des contraintes de base d'un certificat n'a pas été observée.                                                         | 0x80096019 |
| APPROUVER \_ la \_ signature du certificat E \_       | La signature du certificat ne peut pas être vérifiée.                                                                           | 0x80096004 |
| APPROUVER \_ le \_ signataire du compteur E \_       | L’une des signatures de compteur n’est pas valide.                                                                                   | 0x80096003 |
| APPROUVER \_ E confiance \_ explicite \_    | Le certificat a été explicitement marqué comme non approuvé par l’utilisateur.                                                                | 0x800B0111 |
| APPROUVER \_ les \_ \_ critères financiers   | Le certificat ne correspond pas ou ne contient pas les extensions financières Authenticode.                                                | 0x8009601E |
| APPROUVER \_ E \_ aucun \_ certificat de signataire \_      | Le certificat du signataire du message n’est pas valide ou est introuvable.                                                       | 0x80096002 |
| \_ \_ erreur système de confiance E \_         | Une erreur au niveau du système s'est produite lors de la vérification de l'approbation.                                                                           | 0x80096001 |
| \_horodatage E \_ de \_ confiance           | Le certificat ou la signature d'horodatage n'a pas pu être vérifié ou est incorrect.                                                 | 0x80096005 |



 

 

 



