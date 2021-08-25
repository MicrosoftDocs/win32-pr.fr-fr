---
title: Pools de capteurs
description: 'Décrit trois pools de capteurs possibles : privé, privé et non assigné.'
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d28bd03d84e2558f0fb1ba090440aa2bda62292c51773d54d5094466ba9e494
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035259"
---
# <a name="sensor-pools"></a>Pools de capteurs

pour prendre en charge les scénarios d’authentification Windows et l’authentification définie par le fournisseur, le service biométrique Windows organise les unités biométriques en trois pools de capteurs possibles :

-   **Pool privé** collection d’unités biométriques allouées pour une utilisation exclusive par une application cliente. les pools privés peuvent prendre en charge des scénarios d’authentification qui ne sont pas Windows, et ils permettent à une application d’accéder au matériel d’une unité biométrique de manière définie par un fournisseur. Il peut y avoir autant de pools de capteurs privés sur le système qu’il y a d’unités biométriques.
-   **pool de capteurs système** collection d’unités biométriques partageables qui fournissent l’accès aux services d’authentification Windows. Ce pool est utilisé par Winlogon, UAC et tout autre client qui associe un SID à un modèle biométrique spécifique. Chaque fournisseur de services biométriques possède un pool de capteurs système.
-   Le **pool non assigné** contient une collection (éventuellement vide) d’unités biométriques qui ne sont pas affectées au pool système ou au pool privé.

Les applications peuvent utiliser le pool de systèmes partagés ou créer un pool privé constitué d’unités biométriques supprimées du système ou de pools non attribués. Quand une application libère son pool privé, les unités biométriques sont reconfigurées et retournées à leurs pools d’origine. Pour empêcher les attaques par déni de service, seuls les utilisateurs privilégiés sont autorisés à supprimer le dernier capteur du pool système. Pour plus d’informations, voir les rubriques suivantes :

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                       | Description                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pool de capteurs privés](private-sensor-pool.md)<br/>   | Collection d’unités biométriques réservée pour une utilisation exclusive par une application cliente. Les pools privés prennent en charge les méthodes d’authentification propriétaires et permettent à une application cliente d’accéder à une unité biométrique à l’aide de commandes de contrôle spécifiées par le fournisseur.<br/> |
| [Pool de capteurs système](system-sensor-pool.md)<br/>     | collection d’unités biométriques partageables qui fournissent l’accès aux services d’authentification Windows. Ce pool est utilisé par Winlogon, UAC et tout autre client qui associe un SID à un modèle biométrique spécifique.<br/>                                 |
| [Comportement du pool système](system-pool-behavior.md)<br/> | Discussion sur les actions effectuées par le pool système lorsque des notifications d’événements sont envoyées et lorsqu’aucune opération biométrique n’est en attente.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos de l’API Windows Biometric Framework](./biometric-service-api-portal.md)
</dt> </dl>

 

