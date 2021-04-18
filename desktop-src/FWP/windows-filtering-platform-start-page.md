---
title: Plateforme de filtrage Windows
description: La plateforme de filtrage Windows (WFP) est un ensemble de services système et d’API qui fournissent une plate-forme pour la création d’applications de filtrage réseau.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Plateforme de filtrage Windows
- Page de démarrage de la plateforme de filtrage Windows, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "106511913"
---
# <a name="windows-filtering-platform"></a>Plateforme de filtrage Windows

## <a name="purpose"></a>Objectif

La plateforme de filtrage Windows (WFP) est un ensemble de services système et d’API qui fournissent une plate-forme pour la création d’applications de filtrage réseau. L'API WFP permet aux développeurs d'écrire du code qui interagit avec le traitement de paquets qui a lieu au niveau de plusieurs couches dans la pile de mise en réseau du système d'exploitation. Les données de réseau peuvent être filtrées et peuvent également être modifiées avant qu'elles atteignent leur destination.

En fournissant une plateforme de développement plus simple, WFP est conçu pour remplacer les technologies de filtrage de paquets précédentes, telles que les filtres d’interface TDI (TDI), les filtres NDIS (Network Driver Interface Specification) et les fournisseurs de services en couche (LSP) Winsock. À compter de Windows Server 2008 et Windows Vista, le hook de pare-feu et les pilotes de raccordement de filtre ne sont pas disponibles. les applications qui utilisaient ces pilotes doivent à la place utiliser WFP.

Avec l’API WFP, les développeurs peuvent implémenter des pare-feu, des systèmes de détection d’intrusion, des antivirus, des outils d’analyse réseau et des contrôles de contrôle parental. WFP s’intègre à et assure la prise en charge des fonctionnalités de pare-feu, telles que la communication authentifiée et la configuration de pare-feu dynamique basée sur l’utilisation par les applications de l’API de Sockets (stratégie basée sur l’application). WFP fournit également l’infrastructure pour la gestion des stratégies IPsec, les notifications de modifications, les diagnostics réseau et le filtrage avec état.

La plateforme de filtrage Windows est une plateforme de développement et non un pare-feu lui-même. L’application de pare-feu intégrée à Windows Vista, Windows Server 2008 et aux systèmes d’exploitation ultérieurs Windows Firewall with Advanced Security (WFAS) est implémentée à l’aide de WFP. Par conséquent, les applications développées avec l’API WFP ou l' [API WFAS](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) utilisent la logique d’arbitrage de filtrage commune qui est intégrée à WFP.

L’API WFP se compose d’une API en mode utilisateur et d’une API en mode noyau. Cette section fournit une vue d’ensemble de l’ensemble de la plateforme WFP et décrit en détail uniquement la partie mode utilisateur de l’API WFP. Pour obtenir une description détaillée de l’API WFP en mode noyau, consultez l’aide en ligne de [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .

## <a name="developer-audience"></a>Développeurs concernés

L’API de la plateforme de filtrage Windows est conçue pour être utilisée par les programmeurs qui utilisent le logiciel de développement C/C++. Les programmeurs doivent être familiarisés avec les concepts de mise en réseau et la conception de systèmes utilisant des composants en mode utilisateur et en mode noyau.

## <a name="run-time-requirements"></a>Conditions d’exécution

La plateforme de filtrage Windows est prise en charge sur les clients exécutant Windows Vista et versions ultérieures, et sur les serveurs exécutant Windows Server 2008 et versions ultérieures. Pour plus d’informations sur les spécifications d’exécution d’un élément de programmation spécifique, consultez la section Configuration requise de la page de référence de cet élément.





 

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                               | Description                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Nouveautés de la plateforme de filtrage Windows](what-s-new-in-windows-filtering-platform.md)<br/> | Informations sur les nouvelles fonctionnalités et les nouvelles API de la plateforme de filtrage Windows.<br/>                    |
| [À propos de la plateforme de filtrage Windows](about-windows-filtering-platform.md)<br/>                 | Vue d’ensemble de la plateforme de filtrage Windows.<br/>                                             |
| [Utilisation de la plateforme de filtrage Windows](using-windows-filtering-platform.md)<br/>                 | Exemple de code utilisant l’API de la plateforme de filtrage Windows. <br/>                                |
| [Informations de référence sur l’API de plateforme de filtrage Windows](fwp-reference.md)<br/>                            | Documentation pour les fonctions, structures et constantes de la plateforme de filtrage Windows.<br/> |



 

## <a name="additional-resources"></a>Ressources supplémentaires

Pour poser des questions et avoir des discussions sur l’utilisation de l’API WFP, visitez le Forum sur la [plateforme de filtrage Windows](https://social.msdn.microsoft.com/forums/wfp/threads/).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de plateforme de filtrage Windows en mode noyau-Guide de conception](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[API de la plateforme de filtrage Windows en mode noyau-référence](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[Pare-feu Windows avec fonctions avancées de sécurité](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[Classe d’assistance extensible pour les diagnostics WFP](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[Extensions Winsock Secure Socket](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

