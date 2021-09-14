---
title: Implémentation du modèle de sécurité Teredo
description: le modèle de sécurité Teredo est basé sur la technologie de plateforme de filtrage Windows (WFP) intégrée à Windows Vista. Par conséquent, il est recommandé que les pare-feu tiers utilisent la plateforme WFP pour appliquer le modèle de sécurité Teredo.
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a39668f8e1c86e0cd5b12056df5eb9a5fd9cd3ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013396"
---
# <a name="implementing-the-teredo-security-model"></a>Implémentation du modèle de sécurité Teredo

le modèle de sécurité Teredo est basé sur la technologie de [plateforme de filtrage Windows](/windows/desktop/FWP/windows-filtering-platform-start-page) (WFP) intégrée à Windows Vista. Par conséquent, il est recommandé que les pare-feu tiers utilisent la plateforme WFP pour appliquer le modèle de sécurité [Teredo](about-teredo.md) .

L’implémentation générale du [modèle de sécurité Teredo](the-teredo-security-model.md) requiert les éléments suivants :

-   un pare-feu hôte compatible IPv6 doit être inscrit auprès de Sécurité Windows Center (WSC) sur l’ordinateur. En l’absence d’un pare-feu basé sur l’hôte ou de WSC, l’interface Teredo n’est pas disponible pour utilisation. Il s’agit de la seule exigence de recevoir le trafic sollicité d’Internet via l’interface Teredo.
-   toute application qui reçoit le trafic non sollicité d’Internet via l’interface Teredo doit s’inscrire auprès d’un pare-feu compatible IPv6, comme [Windows pare-feu](/previous-versions/windows/desktop/ics/windows-firewall-start-page), avant de recevoir le trafic non sollicité.

Une adresse Teredo devient dormante si le trafic n’a pas été envoyé ou reçu via l’interface Teredo pendant une heure et si les applications qui répondent aux critères de sécurité requis pour le trafic non sollicité ne sont pas en cours d’exécution ou si les sockets d’écoute ne sont pas ouverts.

après le redémarrage d’un ordinateur, ou si l’adresse Teredo perd ses qualifications, Windows Vista qualifie automatiquement l’adresse et le rend disponible pour une utilisation dès qu’une application est liée à des sockets compatibles IPv6. il est important de noter que l’option de traversée « Edge » du pare-feu Windows définie par une application pour autoriser le trafic non sollicité via Teredo est persistante entre les redémarrages.

## <a name="firewall-requirements-for-teredo"></a>Configuration de pare-feu pour Teredo

les fournisseurs de pare-feu peuvent facilement incorporer la prise en charge Teredo dans leurs produits et protéger leurs utilisateurs à l’aide des fonctionnalités de la plateforme de filtrage Windows. pour ce faire, vous pouvez enregistrer le pare-feu compatible IPv6 avec le centre de Sécurité Windows, ajouter des règles appropriées à la sous-couche Teredo de WFP et utiliser des api intégrées dans Windows pour énumérer les applications qui peuvent écouter le trafic non sollicité sur Teredo. Dans les cas où une application n’a pas besoin d’écouter le trafic sollicité sur Teredo, les pare-feu ne nécessitent pas d’ajout de règles supplémentaires à la plateforme WFP. toutefois, une inscription de pare-feu compatible IPv6 avec Sécurité Windows Center est toujours nécessaire pour que l’adresse Teredo puisse être utilisée.

pour prendre en charge ce scénario, le pare-feu doit être compatible IPv6 et être inscrit auprès du centre de Sécurité Windows. en outre, le pare-feu ne doit pas modifier l’état en cours d’exécution ou de démarrage du service Sécurité Windows Center (wscsvc), car Teredo dépend des informations d’état fournies via les api WSC.

L’API utilisée pour enregistrer un pare-feu avec le WSC peut être obtenue en contactant Microsoft à l’adresse wscisv@microsoft.com . Un accord de non-divulgation est requis pour la divulgation de cette API en raison de problèmes de sécurité.

La documentation suivante détaille les filtres et les exceptions utilisés pour garantir une compatibilité optimale avec Teredo :

-   [Implémentation de filtres de pare-feu pour Teredo](implementing-firewall-filters-for-teredo.md)
-   [Exceptions de pare-feu requises pour Teredo](required-firewall-exceptions-for-teredo.md)
-   [Exceptions de la plateforme de filtrage Windows requises pour Teredo](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a>Configuration de pare-feu pour d’autres technologies de transition IPv6

Pour prendre en charge d’autres technologies de transition IPv6 (telles que 6to4 et ISATAP), le produit de pare-feu d’hôte doit être en mesure de traiter le trafic IPv6. Le protocole IP 41 indique quand un en-tête IPv6 suit un en-tête IPv4. Lorsqu’un pare-feu hôte rencontre le protocole 41, il doit reconnaître que le paquet est un paquet encapsulé IPv6 et, par conséquent, doit traiter le paquet de manière appropriée et prendre les décisions d’acceptation et de refus basées sur les règles IPv6 de sa stratégie.

 

 