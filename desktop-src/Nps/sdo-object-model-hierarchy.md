---
title: Hiérarchie du modèle objet
description: Les objets dans le modèle objet SDO sont organisés dans une hiérarchie. Cela signifie que les objets dans SDO fournissent un accès à d’autres objets dans SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f63b5692571bab49580251d6ef879adde8ae9a57af4c541404aabc48538e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063337"
---
# <a name="object-model-hierarchy"></a>Hiérarchie du modèle objet

Les objets dans le modèle objet SDO sont organisés dans une hiérarchie. Cela signifie que les objets dans SDO fournissent un accès à d’autres objets dans SDO.

Les objets permettent d’accéder à d’autres objets de deux manières. L’une des manières est que l’objet expose une interface qui fournit des méthodes pour récupérer d’autres objets. L’objet machine est un exemple de cette approche. L’objet ordinateur expose l’interface [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) . La méthode [**ISdoMachine :: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) récupère un objet de service. La méthode [**ISdoMachine :: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) récupère un objet utilisateur.

![objet ordinateur exposant l’interface isdomachine](images/sdo01.png)

Pour plus d’informations, consultez la page [obtention d’SDOs de service et d’utilisateur](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).

La deuxième façon dont les objets fournissent l’accès aux autres objets est qu’une collection d’objets est représentée comme une propriété de l’objet qui le contient. Pour récupérer une collection d’objets, appelez [**ISdo :: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) sur la propriété d’un objet qui représente la collection. Par exemple, pour récupérer la collection de stratégies, appelez **ISdo :: GetProperty** sur l’interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) exposée par l’objet NPS.

> [!Note]  
> le Service d’authentification Internet (IAS) a été renommé serveur nps (network Policy Server) à partir de Windows Server 2008.

 

![récupération de la collection de stratégies](images/sdo02.png)

Pour obtenir un exemple de code qui récupère la collection de stratégies, consultez [récupération d’une collection](/windows/desktop/Nps/sdo-retrieving-a-collection).

L' [**objet de données du serveur NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) possède les propriétés suivantes qui représentent des collections :

<dl> <dt>

<span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auprès
</dt> <dd>

Le seul auditeur de la collection d’auditeurs est le [**Journal des événements NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).

</dd> <dt>

<span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Directives
</dt> <dd>

Chaque [**objet de stratégie**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) a une propriété qui représente une collection de conditions.

</dd> <dt>

<span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profils
</dt> <dd>

Chaque [**objet de profil**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) dans les collections de profils a une propriété qui représente une collection d’attributs. Consultez [attributs pris en charge par SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) pour obtenir la liste des attributs pris en charge par SDO.

</dd> <dt>

<span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Relatifs
</dt> <dd>

La collection Protocols contient l’objet de protocole RADIUS, qui contient une collection de clients qui représente des clients RADIUS. Consultez [Ajout d’un client](/windows/desktop/Nps/sdo-adding-a-client) pour obtenir un exemple de code qui montre comment récupérer la collection de clients.

</dd> <dt>

<span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Stratégies de proxy
</dt> <dd>

Cette collection contient les stratégies d’accès réseau utilisées pour le traitement des demandes de connexion.

</dd> <dt>

<span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Profils de proxy
</dt> <dd>

Cette collection contient les profils utilisés pour le traitement des demandes de connexion.

</dd> <dt>

<span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Groupes de serveurs RADIUS
</dt> <dd>

Chaque [**groupe de serveurs RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) de la collection de groupes de serveurs RADIUS a une propriété qui représente la collection de serveurs dans ce groupe de serveurs.

</dd> <dt>

<span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Gestionnaires de demandes
</dt> <dd>

Cette collection contient la collection « Microsoft Realms évaluateur ». Les paramètres « authentification SAM Microsoft NT » et « Microsoft Accounting » sont également disponibles dans ce regroupement.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets et propriétés SDO](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[Attributs pris en charge par SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 