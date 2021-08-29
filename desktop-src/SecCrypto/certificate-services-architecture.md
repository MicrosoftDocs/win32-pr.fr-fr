---
description: Une plate-forme de développement pour créer des autorités de certification pour les entreprises ou les applications Internet sécurisées.
ms.assetid: 6f217682-94bc-4d18-88ea-2f8a06eb83de
title: Architecture des services de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d41a2dedb2ab576009a23f1a67417fb8230b4dfcc1d15629c2c9454469c734
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126872"
---
# <a name="certificate-services-architecture"></a>Architecture des services de certificats

Les services de certificats constituent une plateforme de développement permettant de créer des autorités de certification pour les entreprises ou les applications Internet sécurisées. Une autorité de certification configurée et opérationnelle permet à un site d’émettre, de suivre, de gérer et de révoquer des certificats avec une charge d’administration minimale et une sécurité maximale.

Les services de certificats se composent du moteur du serveur, de la base de données du serveur et d’un ensemble de modules et d’outils qui fonctionnent ensemble pour fonctionner en tant qu’autorité de certification. Les applications externes, les modules et les outils d’administration utilisent des interfaces COM (Component Object Model) pour interagir avec le moteur du serveur. Le diagramme suivant montre les interfaces utilisées par le moteur de serveur :

![architecture des services de certificats](images/certapi.png)

Un système de certification opérationnel aura généralement quatre sous-systèmes principaux.



| Subsystem             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client                | Le client est le logiciel utilisé par l’utilisateur final pour générer une demande de [*certificat*](../secgloss/c-gly.md), envoyer la demande et recevoir le certificat terminé. Microsoft Internet Explorer version 5 est un exemple de client. Le client interagit généralement avec une interface personnalisée gérée par l’application intermédiaire.                                                                                                                                                                                                                                                                                              |
| Intermédiaire          | L’intermédiaire est un sous-système qui se compose de l’application intermédiaire et de l’interface du client des services de certificats (*client Web des services de certificats* dans le programme d’installation). L’application intermédiaire interagit directement avec le client, en recevant des demandes de certificat et en renvoyant des certificats terminés. Il communique avec le moteur du serveur via l’interface du client des services de certificats, qui contient les interfaces COM [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) et [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) . Microsoft Internet Information Services est un exemple d’application intermédiaire. L’application intermédiaire peut être implémentée entièrement via des pages Active Server. |
| Serveur                | Le serveur est le système qui génère le certificat. Outre le moteur serveur, deux composants configurables sont inclus. le module de stratégie et le module de sortie. Le module de stratégie interagit avec le moteur du serveur via les interfaces [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) et [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) . Les modules de sortie (il peut y en avoir plusieurs) interagissent avec le moteur du serveur via les interfaces [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) et [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) .                                                                                                                                                                                       |
| Client d’administration | Le client administratif est le système qui surveille et gère les certificats et les demandes. Le client d’administration utilise l’interface [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) pour communiquer avec le moteur du serveur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Pour plus d’informations sur l’architecture des services de certificats, consultez la page [interfaces de chiffrement](cryptography-interfaces.md), [génération d’un certificat](building-a-certificate.md)et les rubriques suivantes.



| Section                                      | Content                                                                                                                                                                                                                                                                    |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modules de stratégie](policy-modules.md)         | Programmes personnalisables qui peuvent être utilisés lors de l’évaluation des [*demandes de certificat*](../secgloss/c-gly.md); ces programmes appliquent les règles selon lesquelles les services de certificats délivrent ou refusent la demande. |
| [Modules de sortie](exit-modules.md)             | Programmes personnalisables qui reçoivent des notifications du moteur de serveur lorsque des opérations se produisent, par exemple lors de l’émission d’un certificat.                                                                                                                                       |
| [Gestionnaires d’extensions](extension-handlers.md) | Objets COM qui fournissent des routines pour l’encodage des extensions et des types de données plus complexes.                                                                                                                                                                                 |
| [Intermédiaires](intermediaries.md)         | Les programmes qui communiquent avec les applications clientes pour autoriser l’envoi de demandes de certificat.                                                                                                                                                                        |



 

 

 
