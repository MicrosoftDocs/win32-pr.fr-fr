---
title: Protection d’accès réseau (NAP)
description: 'Remarque : la plateforme de protection d’accès réseau n’est pas disponible à partir de la protection d’accès réseau de Windows 10 (NAP) est un ensemble de composants du système d’exploitation qui offrent une plateforme pour l’accès protégé aux réseaux privés.'
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Protection d’accès réseau (NAP)
- Protection d’accès réseau, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672734"
---
# <a name="network-access-protection"></a>Protection d’accès réseau (NAP)

## <a name="purpose"></a>Objectif

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La protection d’accès réseau (NAP) est un ensemble de composants du système d’exploitation qui fournissent une plateforme pour l’accès protégé aux réseaux privés. La plateforme NAP offre un moyen intégré d’évaluer l’état d’intégrité du système d’un client réseau qui tente de se connecter ou de communiquer sur un réseau et de restreindre l’accès du client réseau jusqu’à ce que les conditions de la stratégie de contrôle d’intégrité soient remplies.

La protection NAP est une plateforme extensible qui fournit une infrastructure et un ensemble d’API permettant d’ajouter des composants qui stockent, signalent, valident et corrigent l’état d’intégrité du système d’un ordinateur. La plateforme NAP ne fournit pas de composants pour accumuler et évaluer les attributs de l’état d’intégrité d’un ordinateur. D’autres composants, appelés agents d’intégrité système (SHA) et validateurs d’intégrité du système (SHV), fournissent la validation de la stratégie réseau et la conformité de la stratégie réseau.

## <a name="where-applicable"></a>Le cas échéant

La protection NAP est conçue pour être extensible. Il peut interagir avec n’importe quel logiciel de fournisseur qui fournit les logiciels Sha et SHV ou qui reconnaît son ensemble d’API publié. La protection NAP permet de fournir une solution pour les scénarios courants suivants :

-   Vérifiez l’intégrité et l’état des ordinateurs portables itinérants.
-   Vérifiez l’intégrité des ordinateurs de bureau.
-   Vérifier la conformité et l’intégrité des ordinateurs des bureaux distants.
-   Déterminez l’intégrité des ordinateurs portables visités.
-   Vérifier la conformité et l’intégrité des ordinateurs personnels non gérés.

## <a name="developer-audience"></a>Développeurs concernés

L’API NAP est conçue pour les développeurs C/C++. Pour les méthodes de contrainte de mise en conformité NAP, les programmeurs doivent être familiarisés avec les protocoles de mise en réseau et les technologies telles que RADIUS (Remote Authentication Dial-in User Service), DHCP (Dynamic Host Configuration Protocol), les réseaux privés virtuels (VPN), la norme IEEE 802.1 X pour l’accès câblé et sans fil et IPsec (Internet Protocol Security).

## <a name="run-time-requirements"></a>Conditions d’exécution

La plateforme NAP requiert des serveurs d’infrastructure NAP exécutant Windows Server 2008 ou version ultérieure et des clients NAP exécutant Windows XP avec Service Pack 3 (SP3), Windows Vista ou des systèmes d’exploitation ultérieurs. Pour obtenir des informations spécifiques sur les systèmes d’exploitation qui prennent en charge un élément de programmation particulier, reportez-vous aux sections exigences des API NAP dans la documentation de référence NAP.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                         | Description                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [À propos de NAP](about-nap.md)<br/>         | Informations générales sur l’API NAP.<br/>                                     |
| [Utilisation de NAP](using-nap.md)<br/>         | Exemples d’utilisation de l’API NAP.<br/>                                            |
| [Référence NAP](nap-reference.md)<br/> | Documentation sur les interfaces NAP, les structures et les autres éléments de code.<br/> |



 

 

 





