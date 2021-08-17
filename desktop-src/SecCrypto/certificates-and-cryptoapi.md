---
description: Un certificat standard X. 509, contient la version, le numéro de série, l’identificateur d’algorithme, le nom de l’émetteur, la plage de dates valides, le nom de l’objet, l’algorithme et les informations sur la clé publique du sujet, et éventuellement, l’ID unique de l’émetteur, l’ID unique de l’objet et les extensions.
ms.assetid: 91425185-2a06-4040-b83d-c42ee080d55f
title: Certificats et CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8af32073cc3f42bbee07d1702fd1e6044c424ac236cf05ed8374c33757c1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770740"
---
# <a name="certificates-and-cryptoapi"></a>Certificats et CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) prend en charge l’utilisation de certificats X. 509 tels que définis dans la [norme IETF RFC 3280](https://www.ietf.org/rfc/rfc3280.txt). Cette documentation suppose l’utilisation d’un [*certificat numérique*](../secgloss/c-gly.md)X. 509 ou comparable.

Un certificat standard X. 509 contient les informations suivantes.



| Champ                | Description                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version              | Numéro de version du certificat.                                                                                                                                                                                         |
| Numéro de série        | Numéro de série du certificat.                                                                                                                                                                                          |
| Identificateur d’algorithme | Algorithme de signature utilisé par le signataire de certificat.                                                                                                                                                                        |
| Nom de l’émetteur          | Nom de l’émetteur du certificat.                                                                                                                                                                                     |
| Pas avant           | Date avant laquelle le certificat n’est pas valide.                                                                                                                                                                            |
| Pas après            | Date après laquelle le certificat n’est pas valide.                                                                                                                                                                             |
| Nom de sujet         | Nom de la personne ou de l’entité à qui le certificat est émis.                                                                                                                                                      |
| Algorithm            | Algorithme utilisé pour la clé publique.                                                                                                                                                                                         |
| Clé publique de l’objet   | Clé publique réelle (une chaîne de bits).                                                                                                                                                                                          |
| ID unique de l’émetteur     | Champ facultatif. S’il est présent, la version doit être la version 2.                                                                                                                                                                     |
| ID unique de l’objet    | Champ facultatif. S’il est présent, la version doit être la version 2.                                                                                                                                                                     |
| Extensions           | Champ facultatif. Représente des données supplémentaires qu’un émetteur peut vouloir ajouter à un certificat, telles que l’adresse de messagerie ou l’autorisation d’émettre des certificats. Si des extensions sont présentes, la version doit être la version 3.<br/> |



 

 

 
