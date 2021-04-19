---
description: Le chiffrement à clé publique (également appelé cryptographie à clé asymétrique) utilise une paire de clés pour chiffrer et déchiffrer le contenu.
ms.assetid: 93f65367-ca4b-4b44-9833-0653cfd3f3d3
title: Infrastructure à clé publique (PKI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e4ff0b2b3912bc44851be105c2e2b15200eb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519382"
---
# <a name="public-key-infrastructure"></a>Infrastructure à clé publique (PKI)

Le chiffrement à clé publique (également appelé cryptographie à clé asymétrique) utilise une paire de clés pour chiffrer et déchiffrer le contenu. La paire de clés se compose d’une clé publique et d’une clé privée qui sont liées mathématiquement. Une personne qui envisage de communiquer en toute sécurité avec d’autres personnes peut distribuer la [*clé publique*](/windows/desktop/SecGloss/p-gly) , mais doit conserver le secret de la [*clé privée*](/windows/desktop/SecGloss/p-gly) . Le contenu chiffré à l’aide de l’une des clés peut être déchiffré à l’aide de l’autre. Supposons, par exemple, que Bob souhaite envoyer un message électronique sécurisé à Alice. Cela peut être accompli de la manière suivante :

1.  Bob et Alice ont leurs propres paires de clés. Ils ont gardé leurs clés privées en toute sécurité et ont envoyé leurs clés publiques directement les unes aux autres.
2.  Bob utilise la clé publique d’Alice pour chiffrer le message et l’envoyer à son destinataire.
3.  Alice utilise sa clé privée pour déchiffrer le message.

Cet exemple simplifié met en évidence au moins un problème évident que Bob doit avoir sur la clé publique qu’il a utilisée pour chiffrer le message. Autrement dit, il ne peut pas savoir avec certitude que la clé qu’il a utilisée pour le chiffrement appartenait réellement à Alice. Il est possible qu’un autre tiers surveillant le canal de communication entre Bob et Alice ait remplacé une clé différente.

Le concept d’infrastructure à clé publique a évolué pour aider à résoudre ce problème et d’autres. Une infrastructure à clé publique (PKI) se compose d’éléments logiciels et matériels qu’un tiers de confiance peut utiliser pour établir l’intégrité et la propriété d’une clé publique. La partie approuvée, appelée [*autorité de certification*](/windows/desktop/SecGloss/c-gly) , l’effectue généralement en émettant des certificats binaires signés (chiffrés) qui affirment l’identité de l’objet du certificat et lient cette identité à la clé publique contenue dans le certificat. L’autorité de certification signe le certificat à l’aide de sa clé privée. Il émet la clé publique correspondante à toutes les parties intéressées dans un certificat d’autorité de certification auto-signé. Lorsqu’une autorité de certification est utilisée, l’exemple précédent peut être modifié de la manière suivante :

1.  Supposons que l’autorité de certification a émis un certificat numérique signé contenant sa clé publique. L’autorité de certification auto-signe ce certificat à l’aide de la clé privée qui correspond à la clé publique dans le certificat.
2.  Alice et Bob conviennent d’utiliser l’autorité de certification pour vérifier leurs identités.
3.  Alice demande un certificat de clé publique auprès de l’autorité de certification.
4.  L’autorité de certification vérifie son identité, calcule un hachage du contenu qui constitue son certificat, signe le hachage à l’aide de la clé privée qui correspond à la clé publique dans le certificat d’autorité de certification publié, crée un nouveau certificat en concaténant le contenu du certificat et le hachage signé, puis rend le nouveau certificat disponible publiquement.
5.  Bob récupère le certificat, déchiffre le hachage signé à l’aide de la clé publique de l’autorité de certification, calcule un nouveau hachage du contenu du certificat et compare les deux hachages. Si les hachages correspondent, la signature est vérifiée et Bob peut supposer que la clé publique dans le certificat appartient effectivement à Alice.
6.  Bob utilise la clé publique vérifiée d’Alice pour chiffrer un message.
7.  Alice utilise sa clé privée pour déchiffrer le message de Bob.

En résumé, le processus de signature de certificat permet à Bob de vérifier que la clé publique n’a pas été falsifiée ou endommagée pendant le transit. Avant d’émettre un certificat, l’autorité de certification hache le contenu, signe (chiffre) le hachage à l’aide de sa propre clé privée et comprend le hachage chiffré dans le certificat émis. Bob vérifie le contenu du certificat en déchiffrant le hachage avec la clé publique de l’autorité de certification, en effectuant un hachage distinct du contenu du certificat et en comparant les deux hachages. S’ils correspondent, Bob peut être raisonnablement certain que le certificat et la clé publique qu’il contient n’ont pas été modifiés.

Une infrastructure à clé publique standard est constituée des éléments suivants.

| Élément                            | Description                                                                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Autorité de certification<br/> | Fait office de racine de confiance dans une infrastructure à clé publique et fournit des services qui authentifient l’identité des individus, des ordinateurs et d’autres entités d’un réseau.<br/>      |
| Autorité d’inscription<br/>  | Est certifié par une autorité de certification racine pour émettre des certificats pour des utilisations spécifiques autorisées par la racine. Dans une infrastructure à clé publique (PKI) Microsoft, une autorité d’inscription (RA) est généralement appelée autorité de certification secondaire.<br/> |
| Base de données de certificats<br/>    | Enregistre les demandes de certificat et les certificats émis et révoqués, ainsi que les demandes de certificats sur l’autorité de certification ou RA.<br/>                                                                       |
| Magasin de certificats<br/>       | Enregistre les certificats émis et les demandes de certificat en attente ou rejetées sur l’ordinateur local.<br/>                                                                                  |
| Serveur d’archivage de clé<br/>     | Enregistre les clés privées chiffrées dans la base de données de certificats pour la récupération après perte.<br/>                                                                                              |



 

L’API d’inscription de certificats vous permet de soumettre des demandes d’archivage de certificat et de clé à des autorités de certification et d’inscription et d’installer le certificat émis sur un ordinateur local. Elle ne vous permet pas de manipuler directement la base de données de certificats ou le magasin de certificats.

Les rubriques suivantes traitent de l’infrastructure de clé publique de Microsoft plus en détail :

-   [Certificats de clé publique X. 509](about-x-509-public-key-certificates.md)
-   [Éléments PKI](about-pki-components.md)
-   [Modèles d’approbation](about-trust-models.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’API d’inscription de certificats](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

