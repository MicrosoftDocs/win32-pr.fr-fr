---
description: une infrastructure à clé publique (PKI) Windows enregistre des certificats sur le serveur qui héberge l’autorité de certification (CA) et sur l’ordinateur ou l’appareil local.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Répertoire de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b77a7c63e234460394005aac416d41ff7845470139ba2cb8b700132bea0118c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904828"
---
# <a name="certificate-directory"></a>Répertoire de certificat

une infrastructure à clé publique (PKI) Windows enregistre des certificats sur le serveur qui héberge l’autorité de certification (CA) et sur l’ordinateur ou l’appareil local. Le stockage de l’autorité de certification est généralement désigné sous le nom de base de données de certificats, et le stockage local est appelé magasin de certificats.

## <a name="certificate-database"></a>Base de données de certificats

lorsque vous ajoutez des Services de certificats sur un serveur Windows et configurez une autorité de certification, une base de données de certificats est créée. Par défaut, la base de données est contenue dans le dossier *% systemroot%* \\ system32 \\ Certlog, et le nom est basé sur le nom de l’autorité de certification avec une extension. edb. La base de données peut contenir les éléments suivants :

-   Certificats émis
-   Certificats révoqués
-   Clés privées archivées
-   Demandes de certificat

Vous ne pouvez pas utiliser l’API d’inscription de certificats pour manipuler la base de données. Le processus d’inscription crée automatiquement les entrées nécessaires.

## <a name="certificate-stores"></a>Magasin de certificats

Les services de certificats Microsoft copient les certificats émis et les demandes en attente ou rejetées pour les ordinateurs et les appareils locaux. L’emplacement de stockage est appelé magasin de certificats et se compose des magasins logiques suivants.

| Magasin logique                                         | Description                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Personnel<br/>                                   | Contient des certificats associés à une clé privée contrôlée par l’utilisateur ou l’ordinateur.<br/>                     |
| Autorités de certification racine de confiance<br/>     | Contient des certificats provenant d’autorités de certification (ca) approuvées de manière implicite.<br/>                              |
| Enterprise Trust<br/>                           | Contient les listes de certificats de confiance généralement utilisées pour approuver des certificats auto-signés d’autres organisations.<br/> |
| Autorités de certification intermédiaires<br/>     | Contient les certificats émis pour des AC secondaires dans la hiérarchie de certification.<br/>                             |
| Objet utilisateur Active Directory<br/>               | Contient le ou les certificats de l’objet utilisateur publiés dans Active Directory.<br/>                         |
| Éditeurs approuvés<br/>                         | Contient des certificats provenant d’autorités de certification approuvées.<br/>                                                                     |
| Certificats non autorisés<br/>                     | Contient des certificats qui ont été identifiés explicitement comme non approuvés.<br/>                                    |
| Autorités de certification racine tierce partie<br/> | Contient des certificats racines approuvés provenant d’autorités de certification en dehors de la hiérarchie de certificats interne.<br/>                     |
| Personnes autorisées<br/>                             | Contient des certificats délivrés aux utilisateurs ou entités qui ont été explicitement approuvés.<br/>                        |
| Autres personnes<br/>                               | Contient des certificats délivrés aux utilisateurs ou entités qui ont été approuvés implicitement.<br/>                        |
| Demandes d'inscription de certificat<br/>            | Contient des demandes de certificat en attente ou rejetées.<br/>                                                          |



 

Vous ne pouvez pas utiliser l’API d’inscription de certificats pour spécifier ou récupérer des propriétés de stockage ou copier des certificats dans des magasins spécifiques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments PKI](about-pki-components.md)
</dt> </dl>

 

 




