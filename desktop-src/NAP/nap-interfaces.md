---
title: Interfaces NAP
description: Interfaces NAP
ms.assetid: fff854b9-9c83-4db2-bceb-22509b261a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff67fe21922c5b1baf9c2825dc7ea2852f14331
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029720"
---
# <a name="nap-interfaces"></a>Interfaces NAP

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

Le système NAP est composé des interfaces suivantes.



| Nom de l'interface                                                                   | Description                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapCertRelyingParty**](inapcertrelyingparty.md)                             | Fournit des méthodes que les parties de confiance de certificat doivent utiliser pour communiquer avec le NapAgent.                                                        |
| [**INapClientManagement**](inapclientmanagement.md)                             | Utilisé pour la gestion des clients NAP du cache SoH et du déclenchement de l’échange SoH. Action déconseillée.                                                                |
| [**INapClientManagement2**](inapclientmanagement2.md)                           | Utilisé pour la gestion des clients NAP du cache SoH et du déclenchement de l’échange SoH.                                                                            |
| [**INapComponentConfig**](inapcomponentconfig.md)                               | Utilisé pour la configuration personnalisée des composants SHV. Action déconseillée.                                                                                    |
| [**INapComponentConfig2**](inapcomponentconfig2.md)                             | Fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système afin de configurer une interface utilisateur de serveur de stratégie réseau (NPS) à distance.   |
| [**INapComponentConfig3**](inapcomponentconfig3.md)                             | Fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système (SHV) afin de définir et de modifier les données de configuration d’un ID de configuration spécifique. |
| [**INapComponentInfo**](inapcomponentinfo.md)                                   | Doit être implémentée par les composants de plug-in, tels que les Sha et les validateurs d’intégrité du système, afin qu’ils puissent être communiqués par le système NAP.                          |
| [**INapEnforcementClientBinding**](inapenforcementclientbinding.md)             | Utilisé par les clients de mise en œuvre pour communiquer avec le NapAgent.                                                                                       |
| [**INapEnforcementClientCallback**](inapenforcementclientcallback.md)           | Les clients de contrainte doivent implémenter cette interface pour permettre à NapAgent de communiquer avec eux.                                                  |
| [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)       | Permet la gestion des connexions clientes. Action déconseillée.                                                                                                |
| [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)     | Permet la gestion des connexions clientes.                                                                                                            |
| [**INapServerCallback**](inapservercallback.md)                                 | Les programmes de validation d’intégrité système utilisent la méthode unique sur cette interface pour signaler la fin de la requête asynchrone.                                                             |
| [**INapServerInfo**](inapserverinfo.md)                                         | Utilisé par les clients de gestion (par exemple, les fournisseurs WMI, les outils en ligne de commande, etc.) pour interroger l’état du système de serveur NAP.                             |
| [**INapServerManagement**](inapservermanagement.md)                             | Utilisé pour la gestion de base du serveur NAP.                                                                                                        |
| [**INapSoHConstructor**](inapsohconstructor.md)                                 | Utilisé par l’SHA pour construire des demandes SoH et par les validateurs d’intégrité du système pour construire des réponses SoH.                                                                      |
| [**INapSoHProcessor**](inapsohprocessor.md)                                     | Utilisé par l’SHA pour traiter le contenu des réponses SoH et par les validateurs d’intégrité du système pour traiter le contenu des demandes SoH.                                          |
| [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)             | Les SHA doivent utiliser cette interface pour communiquer avec le NapAgent. Action déconseillée.                                                                          |
| [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)           | Les SHA doivent utiliser cette interface pour communiquer avec le NapAgent.                                                                                      |
| [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)           | SHA doit implémenter cette interface pour coordonner le traitement avec le système NAP.                                                                    |
| [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)             | SHA utilise cette interface pour communiquer et coordonner son traitement avec le système NAP.                                                         |
| [**INapSystemHealthValidator**](inapsystemhealthvalidator.md)                   | Fournit des méthodes qu’un SHV doit implémenter pour que le système NAP puisse communiquer avec lui.                                                         |
| [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)   | Les programmes de validation d’intégrité système utilisent cette interface pour la communication des données avec leur équivalent côté client. Action déconseillée.                                                      |
| [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) | Les programmes de validation d’intégrité système utilisent cette interface pour la communication des données avec leur équivalent côté client.                                                                  |



 

 

 




