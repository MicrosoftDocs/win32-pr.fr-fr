---
title: Service d’authentification Internet & le serveur NPS (Network Policy Server)
description: En savoir plus sur le service d’authentification Internet et le serveur NPS (Network Policy Server). Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36751c66b525749afce0d5546f61fa35c1cbb856
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011516"
---
# <a name="internet-authentication-service--network-policy-server"></a>Service d’authentification Internet & le serveur NPS (Network Policy Server)

Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server).

## <a name="internet-authentication-service"></a>Service d'authentification Internet

Le service d’authentification Internet est l’implémentation Microsoft d’un serveur et d’un proxy RADIUS.

Le service d’authentification Internet prend en charge deux ensembles d’API : l’API des [extensions du serveur de stratégie réseau](ias-extensions.md) et l' [API des objets de données serveur](server-data-objects.md).

Pour plus d’informations sur IAS, voir [TechNet : service d’authentification Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .

## <a name="network-policy-server"></a>Serveur de stratégie réseau

le serveur nps (Network Policy server) est l’implémentation Microsoft d’un serveur et d’un proxy RADIUS et est disponible sur les serveurs Windows à partir de Windows Server 2008.

NPS prend en charge les deux mêmes jeux d’API que IAS : [API d’extension de serveur de stratégie réseau](ias-extensions.md) et [API d’objets de données serveur](server-data-objects.md).

En outre, NPS contient un ensemble de nouvelles fonctionnalités qui étendent les fonctionnalités d’IAS.




| Fonctionnalité | Nouveautés du serveur NPS | 
|---------|--------------------|
| <a href="/windows/desktop/NAP/network-access-protection-start-page">Protection d’accès réseau (NAP)</a><br /> | NPS est le serveur central de la protection d’accès réseau.<br /> NPS prend en charge la création de stratégies à l’aide des conditions supplémentaires suivantes :<br /><ul><li>Expiration de la stratégie.</li><li>Version du système d’exploitation.</li><li>Accédez à l’adresse IP du client.</li><li>Stratégies de contrôle d’intégrité.</li><li>Types EAP autorisés.</li><li>HCAP.</li></ul>NPS prend en charge la création de stratégies à l’aide des paramètres supplémentaires suivants :<br /><ul><li>Accompli.</li><li>Accès limité.</li><li>État étendu pour un accès limité.</li></ul>NPS, via NAP, interagit avec CISCO NAC.<br /> IAS ne prend pas en charge la protection d’accès réseau.<br /> | 
| <a href="/windows/win32/eap/eap-start-page">Protocole EAP</a> Prise en charge des stratégies et <a href="/windows/win32/eaphost/portal">EAPHost</a><br /> | NPS utilise EAPHost pour l’extensibilité de la méthode EAP. En outre, les administrateurs peuvent configurer la stratégie d’accès réseau pour le protocole EAP.<br /> IAS ne prend pas en charge l’intégration EAPHost ou les conditions de filtre de type EAP pour les stratégies.<br /> | 
| Prise en charge D’ipv6<br /> | NPS prend en charge le déploiement dans les environnements IPv6.<br /> IAS ne prend pas en charge les adresses réseau IPv6.<br /> | 
| Configuration XML<br /> | La configuration NPS peut être importée et exportée au format XML.<br /> IAS utilise une base de données Jet pour stocker la configuration du service.<br /> | 
| <a href="https://www.niap-ccevs.org/cc-scheme/">Critères communs</a> Supporter<br /> | NPS a été mis à jour pour prendre en charge son déploiement dans des environnements qui doivent respecter les normes de sécurité critères communs.<br /> | 
| <a href="ias-extensions.md">API des extensions NPS</a><br /> | Les dll d’extension NPS s’exécutent dans un processus distinct du service NPS. En cas de panne d’une DLL d’extension, NPS continue à s’exécuter et les demandes futures seront rejetées.<br /> Les dll d’extension IAS s’exécutent dans le même processus que le service IAS et peuvent avoir un impact négatif sur le service.<br /> | 
| Interface utilisateur de gestion<br /> | La console de gestion NPS (NPS. msc) a une nouvelle apparence, une plus grande facilité d’utilisation et couvre toutes les nouvelles fonctionnalités ajoutées à NPS.<br /> IAS utilise la console de gestion IAS. msc.<br /> | 
| Outil de gestion des rôles et intégration des Gestionnaire de serveur<br /> | NPS est intégré au Gestionnaire de serveur et à l’outil de gestion des rôles. Cette intégration facilite la configuration et la gestion du serveur NPS et des scénarios associés.<br /> Gestionnaire de serveur n’est pas disponible sur les ordinateurs exécutant IAS.<br /> | 
| Mise à jour des scripts de ligne de commande avec <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.<br /> | NPS prend en charge l’interface de ligne de commande « netsh nps ». « Netsh nps » contient de nouvelles commandes qui permettent de configurer entièrement NPS, y compris les fonctionnalités NAP.<br /> IAS prend en charge l’interface de ligne de commande « netsh aaaa ».<br /> | 
| Isolation de la stratégie<br /> | NPS permet l’implémentation de l’isolation de la stratégie en définissant la source de la stratégie réseau. Il est possible de configurer des stratégies qui s’appliquent uniquement à un type NAS prédéterminé.<br /> IAS ne prend pas en charge l’isolation de la stratégie.<br /> | 




 

Pour plus d’informations sur NPS, voir [TechNet : serveur NPS (Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) ).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification, autorisation et gestion des comptes RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Journalisation avec le serveur NPS](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Utilisation d’un serveur d’État](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

