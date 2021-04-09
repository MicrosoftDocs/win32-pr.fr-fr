---
description: Les modules de stratégie sont des programmes qui reçoivent des demandes des services de certificats, évaluent ces demandes et spécifient des propriétés facultatives des certificats qui sont générés pour remplir ces requêtes.
ms.assetid: 23d920ea-af62-42ce-ad48-c7a03ab55fc9
title: Modules de stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781a88ab714c402ea1670ac8c18ae4d80eb776e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952883"
---
# <a name="policy-modules"></a>Modules de stratégie

Les modules de stratégie sont des programmes qui reçoivent des demandes des services de certificats, évaluent ces demandes et spécifient des propriétés facultatives des certificats qui sont générés pour remplir ces requêtes. Un module de stratégie est implémenté en tant que [*bibliothèque de liens dynamiques*](../secgloss/d-gly.md) (dll). Un module de stratégie peut utiliser l’interface [ICertServerPolicy](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) pour communiquer avec les services de certificats. Les services de certificats communiquent avec un module de stratégie au moyen d’appels COM directs ou, si le module ne prend pas en charge les appels COM directs, par le biais de l’automatisation.

Un module de stratégie peut afficher des extensions et des propriétés de certificat existantes, et il peut également afficher les propriétés et les attributs de la requête. En outre, un module de stratégie peut définir ou modifier les propriétés des extensions de certificat et des propriétés « NotBefore » et « NotAfter », ainsi que le [*nom unique relatif*](../secgloss/r-gly.md) (RDN) d’un sujet de certificat, sous réserve de certaines restrictions. En dernier lieu, un module de stratégie émet ou refuse la [*demande de certificat*](../secgloss/c-gly.md) ou la conserve en attente.

Avant d’écrire un module de stratégie personnalisé, envisagez d’utiliser l’un des modules de stratégie par défaut. Les services de certificats de l' [*autorité de certification*](../secgloss/c-gly.md) d’entreprise et de l’autorité de certification autonome sont fournis avec un module de stratégie par défaut approprié. Les modules de stratégie par défaut entreprise et autonome émettent des demandes de certificat (bien que la stratégie par défaut autonome consiste à conserver le certificat en attente jusqu’à ce qu’il soit émis manuellement par un administrateur). Une autorité de certification d’entreprise doit utiliser uniquement le module de stratégie d’entreprise fourni par Microsoft.

L’autorité de certification d’entreprise requiert Active Directory. Les fonctionnalités supplémentaires de son module de stratégie par défaut incluent les modèles de certificats, la sécurité de la [*liste de contrôle d’accès*](../secgloss/a-gly.md) (ACL) sur les modèles de certificats pour s’assurer que les demandes sont émises uniquement pour les extensions autorisées et prédéfinies ajoutées au certificat émis, ainsi que pour la prise en charge des certificats de connexion au domaine de carte à puce.

Le module de stratégie d’autorité de certification autonome par défaut ne prend pas en charge la plupart des fonctionnalités du module entreprise par défaut, mais il prend en charge l’émission de certificats de carte à puce. Pour obtenir des informations spécifiques, ainsi que les fonctionnalités les plus récentes du module de stratégie par défaut, consultez la documentation du produit.

Pour les installations où le module de stratégie par défaut est inacceptable, les services de certificats autorisent les modules de stratégie personnalisés. Pour plus d’informations, consultez [écriture de modules de stratégie personnalisés](writing-custom-modules.md).

 

 
