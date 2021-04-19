---
description: Algorithmes pris en charge par le fournisseur de services de chiffrement DSS de base Microsoft et Diffie-Hellman.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: Algorithmes de fournisseur d’PROV_DSS_DH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532308"
---
# <a name="prov_dss_dh-provider-algorithms"></a>Algorithmes PROVen du \_ \_ fournisseur DH DSS

Le tableau suivant répertorie les algorithmes pris en charge par Microsoft Base DSS et Diffie-Hellman fournisseur de services de chiffrement.



| ID d’algorithme      | Description                                 | Commentaires                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ MD5         | Algorithme de hachage MD5.                      | Fourni uniquement pour le hachage.                                                                                      |
| CALG \_ SHA         | Algorithme de hachage SHA.                      | Doit être utilisé pour les signatures DSS.                                                                                |
| CALG \_ SHA1        | Identique à CALG \_ Sha.                          | Aucun commentaire.                                                                                                     |
| CALG \_ DSS \_   | Algorithme de signature de clé publique/privée DSS. | Longueur de clé : peut être défini, 512 bits à 1 024 bits dans des incréments de 64 bits. Longueur de clé par défaut : 1 024 bits.<br/> |
| CALG \_ DH \_ DF      | Échange de clé D-H pour le stockage et le transfert.         | Longueur de clé : peut être définie, 384 bits à 512 bits par incréments de 8 bits. Longueur de clé par défaut : 512 bits.<br/>      |
| CALG \_ DH \_ EPHEM   | Échange de clé D-H éphémère.                 | Longueur de clé : peut être définie, 384 bits à 512 bits par incréments de 8 bits. Longueur de clé par défaut : 512 bits.<br/>      |
| CALG \_ CYLINK \_ MEK | Variante 40 bits d’une clé DES.              | Longueur de clé : 40 bits.                                                                                            |



 

 

 




