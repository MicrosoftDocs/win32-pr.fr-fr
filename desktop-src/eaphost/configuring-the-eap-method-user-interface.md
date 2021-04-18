---
title: Configuration de l’interface utilisateur de la méthode EAP
description: Explique comment configurer le demandeur en fournissant une configuration de méthode EAP à EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106512293"
---
# <a name="configuring-the-eap-method-user-interface"></a>Configuration de l’interface utilisateur de la méthode EAP

Cette rubrique explique comment configurer le demandeur en fournissant une configuration de méthode EAP à EAPHost.

Pour qu’un demandeur effectue une authentification basée sur EAP à l’aide d’EAPHost, un demandeur doit fournir une configuration de méthode EAP à EAPHost via la fonction [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) .

1.  Pour obtenir la configuration de la méthode EAP, un demandeur interroge généralement EAPHost à l’aide de [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) pour connaître l’ensemble complet des méthodes EAP disponibles et installées sur l’ordinateur local. La liste des méthodes est généralement présentée à l’utilisateur dans une zone combinée ou un autre contrôle d’interface utilisateur qui permet à l’utilisateur de sélectionner la méthode de votre choix.
    > [!Note]  
    > Le demandeur peut choisir de filtrer la liste affichée des méthodes en fonction des bits de propriété de méthode indiqués dans informations sur la **\_ méthode EAP \_ . eapProperties**. Certaines méthodes peuvent ne pas convenir aux caractéristiques de sécurité du transport fournies par le demandeur, par exemple.

     

2.  Une fois que le contrôle d’interface utilisateur est rempli avec l’ensemble de méthodes EAP possibles, l’utilisateur sélectionne la méthode qu’il souhaite configurer. En règle générale, le demandeur fournit un bouton de **configuration** ou de **Propriétés** permettant à l’utilisateur d’accéder aux propriétés de configuration de la méthode EAP sélectionnée.
    > [!Note]
    > Le demandeur est conscient qu’il existe des propriétés configurables par l’utilisateur basées sur l’activation du bit **eapPropSupportsConfig** dans informations sur la **\_ méthode EAP \_ . eapProperties**.
    >
    > Pour plus d’informations, consultez Propriétés de la [**méthode EAP**](eap-method-properties.md).

     

3.  Lorsque l’utilisateur clique sur le contrôle d’interface utilisateur approprié, le demandeur appelle [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), en passant à la fonction la valeur **HWND** pour la propre interface utilisateur du demandeur, la structure de [**\_ \_ type de méthode EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) obtenue à partir de la structure de la requête vers la structure d' [**\_ \_ informations de méthode EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) et d’autres paramètres requis.
4.  L’appel de [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) appelle l’interface utilisateur de configuration de la méthode EAP. Au retour de **EapHostPeerInvokeConfigUI**, la fonction retourne un objet blob de configuration de méthode EAP en tant que paramètre out.
5.  Le demandeur stocke l’objet BLOB de configuration, ainsi que la structure de [**\_ \_ type de méthode EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) à utiliser avec [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).
6.  La méthode précise pour le stockage de l’objet BLOB configuration dépend entièrement du demandeur. Toutefois, le demandeur doit toujours stocker la configuration de manière sécurisée et appropriée pour les données de configuration d’authentification du système et des utilisateurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation de stratégie de groupe](enabling-group-policy.md)
</dt> <dt>

[Implémentation de la prise en charge de In-Band NAP pour les méthodes EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implémentation de la prise en charge NAP pour les méthodes EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Transfert de données entre le demandeur et les méthodes EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Demandeurs EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




