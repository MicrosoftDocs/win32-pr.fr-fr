---
title: Activation de stratégie de groupe
description: Découvrez comment configurer le demandeur en activant la stratégie de groupe. Consultez éléments à prendre en considération pour les demandeurs et afficher les ressources disponibles supplémentaires.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2a388bf8dba155e42d5542c1379f7b0cc34d44579b92809387541d7e20cf65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784998"
---
# <a name="enabling-group-policy"></a>Activation de stratégie de groupe

Cette rubrique explique comment configurer le demandeur en activant la stratégie de groupe. Les demandeurs EAPHost peuvent participer à la stratégie de groupe pour permettre à un administrateur réseau de configurer de manière centralisée leurs ordinateurs réseau.

La méthode et le mécanisme précis par lesquels le demandeur choisit de participer à la stratégie de groupe sont à la discrétion du demandeur. Des exemples de mécanismes pour la participation à la stratégie de groupe incluent les extensions côté client/serveur, le modèle d’administration, etc.

## <a name="considerations-when-enabling-group-policy"></a>Considérations relatives à l’activation de stratégie de groupe

Voici les éléments à prendre en considération pour les demandeurs en ce qui concerne la stratégie de groupe et le protocole EAP.

1.  La configuration EAP doit toujours être stockée au format XML chaque fois que cela est possible et pas au format binaire. La stratégie de groupe peut être appliquée à n’importe quel ordinateur du domaine, et la configuration de la méthode EAP et les données utilisateur ne sont pas nécessairement portables entre les architectures de processeur 32 bits et 64 bits. XML résout les problèmes de limite d’architecture de processeur, car le demandeur convertit localement le XML indépendant de l’architecture du processeur en représentation binaire de la configuration au moment de l’authentification.

    Pour plus d’informations, voir les rubriques suivantes :

    -   [Forum aux questions (FAQ)](general-frequently-asked-questions.md)
    -   [Forum aux questions sur la méthode EAP](eap-method-frequently-asked-questions.md).
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Si une extension côté serveur de la stratégie de groupe est utilisée, l’extension appelle généralement [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) pour déterminer les méthodes disponibles et pour générer la configuration EAP appropriée pour cette stratégie. La stratégie est ensuite envoyée aux clients réseau appropriés sur lesquels la stratégie est appliquée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’interface utilisateur de la méthode EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Implémentation de la prise en charge de In-Band NAP pour les méthodes EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implémentation de la prise en charge NAP pour les méthodes EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transfert de données entre le demandeur et les méthodes EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Demandeurs EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




