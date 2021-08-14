---
description: Une autorité de certification est chargée d'attester l'identité des utilisateurs, des ordinateurs et des organisations.
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: Autorités de certification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b5f48c897c74e5f0bf7d4d3b1e21b8f89d33e72cdfa46aefe726f714fbc267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904498"
---
# <a name="certification-authorities"></a>Autorités de certification

Une [*autorité de certification*](/windows/desktop/SecGloss/c-gly) est chargée d’attester de l’identité des utilisateurs, des ordinateurs et des organisations. Elle authentifie une entité et se porte garante de cette identité en émettant un certificat signé numériquement. Elle gère, révoque et renouvelle également les certificats.

Une autorité de certification peut être publique ou privée. Une autorité de certification publique fournit des services de certification, en général payants, au public via Internet. Une autorité de certification privée fournit ce service aux membres d’un remplissage délimité, tel que les employés d’une entreprise ou les membres d’un autre groupe privé.

Le moyen par lequel une autorité de certification authentifie un utilisateur final varie et dépasse le cadre de cette documentation. Toutefois, il est clair que les méthodes d’authentification varient selon le type de fournisseur. Par exemple, une autorité de certification privée peut établir l’identité des utilisateurs finaux en faisant référence à une liste de groupes, telle qu’une base de données Employee ou Active Directory. Les méthodes d’authentification effectuées par une autorité de certification publique sont généralement plus complexes et dépendent en partie du niveau de garantie promis par le certificat.

À mesure que le remplissage d’une infrastructure à clé publique (PKI) augmente, il peut devenir difficile pour une autorité de certification unique de gérer efficacement tous les certificats qu’elle a émis. L’autorité de certification peut compenser en autorisant d’autres autorités de certification dans l’infrastructure à clé publique d’émettre des certificats. L’autorité de certification initiale est appelée racine, et les autorités de certification qu’elle autorise sont appelées subordonnées. Les autorités de certification secondaires peuvent également désigner leurs propres filiales dans les limites définies par la racine. La structure qui en résulte est appelée hiérarchie de certificats. Les certificats émis pour les autorités de certification inférieures dans la hiérarchie contiennent suffisamment de certificats pour retracer un chemin d’accès à la racine. C’est ce que l’on appelle une chaîne de certificats.

Le terme « autorité de certification » peut faire référence à la fois à l’organisation qui est l’identité d’un utilisateur final et le serveur utilisé par l’Organisation pour émettre et gérer des certificats. un serveur de Windows peut être configuré pour agir en tant que serveur d’autorité de certification, et cette documentation fait généralement référence au serveur lors de l’utilisation du terme « ca ».

L’API d’inscription de certificats interagit principalement avec une autorité de certification à l’aide de l’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . La méthode d' [**inscription**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) sur cet objet peut encoder automatiquement une demande de certificat, l’envoyer à l’autorité de certification et installer le certificat émis. Vous pouvez également utiliser un objet **IX509Enrollment** initialisé pour l’inscription hors bande ou pour l’inscription différée. En outre, vous pouvez utiliser l’objet [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) pour surveiller l’état de l’inscription.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments PKI](about-pki-components.md)
</dt> </dl>

 

 
