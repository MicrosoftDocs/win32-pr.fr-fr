---
description: TAPI 3 définit cinq objets ACD principaux, le gestionnaire de l’agent, la file d’attente dans laquelle ACD regroupe l’agent et la session de l’agent. Il étend également l’objet TAPI avec une interface supplémentaire ITTAPICallCenter.
ms.assetid: 6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7
title: À propos des contrôles de centre d’appels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c91601fadeb1c3ba83e3ed5756eefb3ed34427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115530"
---
# <a name="about-call-center-controls"></a>À propos des contrôles de centre d’appels

TAPI 3 définit cinq objets ACD principaux : le gestionnaire de l’agent, la file d’attente, le groupe ACD, l’agent et la session de l’agent. Il étend également l’objet TAPI avec une interface supplémentaire, [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter).

## <a name="agent-object"></a>Objet agent

L’objet agent représente un agent qui prend en charge la gestion des appels. Il s’agit généralement d’une personne, qui peut être un IVR ou une autre combinaison de logiciels et de matériel. Les agents sont la clé d’un centre d’appels ; ils sont chargés de recevoir et de traiter les appels entrants et, parfois, d’effectuer des appels sortants aux clients ou aux prospects.

Dans l’interface TAPI, l’objet agent est directement associé à un compte d’utilisateur, pour assurer la compatibilité avec les systèmes de commutation hérités existants. En outre, pour assurer la compatibilité avec les systèmes de commutation hérités existants, l’agent peut également être associé à un ID d’agent de commutateur.

L’objet agent expose l’interface [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent) . Cette interface implémente des méthodes qui peuvent créer une session d’agent et récupérer des statistiques telles que le nombre total d’appels gérés. Les applications peuvent utiliser l’objet agent pour manipuler l’état de l’agent et déterminer les statistiques globales de l’agent.

## <a name="agent-handler-object"></a>Objet gestionnaire d’agent

Un gestionnaire d’agent représente des logiciels ou du matériel qui peuvent transmettre des appels à un groupe d’agents. En règle générale, il s’agit d’un commutateur propriétaire qui se connecte en dehors des lignes à des téléphones sur les stations d’agents. La plupart des systèmes ACD n’ont qu’un seul commutateur, mais les opérations de grande taille peuvent en avoir davantage. Dans le cas où un agent possède des appareils sur plusieurs systèmes ACD, l’agent voit un nombre correspondant d’objets de gestionnaire d’agent. Il y aura également une instance de l’objet agent relative à l’apparence de l’agent sur chaque système ACD.

L’objet de gestionnaire d’agent expose l’interface [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) . Cette interface implémente des méthodes qui fournissent des informations sur les [groupes ACD](#acd-group-object) associés au gestionnaire de l’agent et les adresses qu’il peut utiliser.

## <a name="agent-session-object"></a>Objet de session de l’agent

Une session de l’agent représente un agent qui s’est connecté et qui est qualifié pour gérer les appels d’un [groupe ACD](#acd-group-object)particulier. Une session de l’agent est un objet créé dynamiquement, qui lie un agent à un groupe ACD, pour lequel il fournira un service, ainsi qu’à l’adresse, où il recevra des appels (tourelle, station, téléphone, etc.). Les applications peuvent utiliser l’objet session de l’agent pour suivre l’activité de l’agent dans un groupe ACD particulier.

L’objet session de l’agent expose l’interface [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession) . Cette interface implémente des méthodes qui peuvent récupérer des informations telles que le temps de conversation moyen pour un appel.

## <a name="acd-group-object"></a>Objet de groupe ACD

Un groupe ACD représente une classe d’appels qui requiert un type particulier de gestion. Par exemple, certains appels entrants pour le centre d’appels d’une banque peuvent concerner les comptes existants, tandis que d’autres peuvent être liés aux nouveaux comptes. Certains agents peuvent avoir une expertise dans les deux domaines, mais la plupart d’entre eux sont spécialisés en un seul. Les groupes ACD seront créés pour gérer chaque type d’appel. Un groupe ACD service une ou plusieurs files d’attente. Comme les appels entrants sont classifiés, ils sont transmis aux files d’attente associées au groupe ACD approprié. Un appel sortant de la file d’attente est passé à un agent qui a créé un [objet de session de l’agent](#agent-session-object) , indiquant qu’il est en mesure de gérer les appels à partir de ce groupe ACD.

L’objet groupe ACD expose l’interface [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup) . Cette interface implémente des méthodes qui fournissent l’accès aux files d’attente associées au groupe ACD actuel.

## <a name="queue-object"></a>Objet file d’attente

L’objet de file d’attente représente un point dans le système ACD où les appels sont temporairement détenus en attente. L’objet de file d’attente expose l’interface [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue) . Cette interface implémente des méthodes qui recueillent des statistiques sur une file d’attente, telles que le nombre d’appels actuellement mis en file d’attente. Le [proxy ACD](acd-proxy.md) utilise ces informations pour distribuer les appels aux agents et pour produire des rapports d’administration.

L’accès à un objet de file d’attente permet à une application de lire diverses statistiques standard relatives à l’utilisation de la file d’attente, mais elle ne lui donne pas la possibilité de contrôler les appels sur la file d’attente. Seules les applications ayant accès aux adresses et aux lignes associées (en général l’application ACD proxy) sont en mesure de contrôler les appels sur la file d’attente.

La plupart des files d’attente sont directement associées à un [objet de groupe ACD](#acd-group-object)et contiendront un appel jusqu’à ce qu’un agent puisse la gérer. D’autres files d’attente peuvent exister pour permettre les guides d’appels complexes (le chemin d’accès défini qu’un appel sans réponse effectue via un commutateur). Par exemple, les appels peuvent être placés dans les files d’attente avant d’être acheminés vers une file d’attente dont se servira un groupe ACD.

 

 
