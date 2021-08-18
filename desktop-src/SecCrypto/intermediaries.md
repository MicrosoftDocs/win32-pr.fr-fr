---
description: Les intermédiaires communiquent avec les applications clientes pour leur permettre de soumettre des demandes de certificat et (en supposant que la requête génère un certificat émis) pour télécharger le certificat émis vers le client.
ms.assetid: c696f09e-98d3-4cea-8ea1-cd8f40b74f12
title: Intermédiaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f9dbd48d5af575658c04760740ad0b1f64f373d76bb20ba80253b874c67de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005287"
---
# <a name="intermediaries"></a>Intermédiaires

Les intermédiaires communiquent avec les applications clientes pour leur permettre de soumettre des [*demandes de certificat*](../secgloss/c-gly.md)et (en supposant que la requête génère un certificat émis) pour télécharger le certificat émis vers le client. Chaque protocole de couche de transport requiert son propre intermédiaire.

Les services de certificats Microsoft sont fournis avec un intermédiaire (les pages d’inscription par le Web) pour HTTP. un autre exemple d’intermédiaire est le composant logiciel enfichable Microsoft Windows certificates MMC (qui permet l’appel de l’assistant demande de certificat). Si d’autres protocoles de couche de transport doivent être utilisés avec les services de certificats, un développeur peut créer un intermédiaire pour chaque protocole de couche de transport souhaité.

Les intermédiaires communiquent avec les services de certificats à l’aide des interfaces [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) et [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) fournies par le moteur serveur. La méthode [**ICertRequest :: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) est utilisée pour envoyer une [*demande de certificat*](../secgloss/c-gly.md)et [**ICertRequest :: GetCertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcertificate) est utilisé pour obtenir le certificat émis résultant. De même, [**ICertConfig :: GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig) est utilisé pour déterminer l’autorité de certification qui peut être utilisée pour émettre le certificat.

Un intermédiaire n’est pas dépendant de la langue. il peut s’agir d’un programme écrit en C++, Visual Basic, Java, script ou autre langage.

En plus de collecter des données à partir du client pour créer une demande de certificat, un intermédiaire peut spécifier des attributs de demande. Les demandes soumises à une [*autorité de certification*](../secgloss/c-gly.md) exécutant le module de stratégie d’entreprise doivent indiquer le type de certificat demandé en spécifiant un attribut « CertificateTemplate » ou une extension de modèle de certificat dans la demande elle-même.

Notez que lors de la création d’une demande de certificat, les développeurs (et les intermédiaires) sont responsables du maintien de la confidentialité de la clé privée. Une fois qu’une clé privée a été compromise (le secret est perdu), elle est inutile.

Les pages d’inscription par le Web des services de certificats utilisent les [interfaces d’inscription de certificats](cryptography-interfaces.md), qui protègent les clés privées en les générant sur la station de travail. En plus de maintenir le secret de la clé privée, le contrôle d’inscription de certificats permet à un intermédiaire de spécifier le fournisseur de services de chiffrement, la spécification de clé, la puissance de clé et l’algorithme de hachage.

Le composant logiciel enfichable MMC Certificats utilise également le contrôle d’inscription de certificats (Xenroll.dll). Toutefois, lorsque les pages d’inscription par le Web des services de certificats entraînent le téléchargement de la ressource de contrôle d’inscription de certificat (Xenroll.dll) sur le client, le cas échéant, le composant logiciel enfichable MMC Certificats s’exécute dans un environnement où Xenroll.dll est déjà une ressource disponible.

Outre [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) et [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig), les développeurs d’intermédiaires peuvent trouver les interfaces d' [inscription de certificats](cryptography-interfaces.md) et le contrôle d' [inscription de carte à puce](certificate-enrollment-control.md) pour être utiles.

 

 
