---
title: Pools de capteurs
description: 'Décrit trois pools de capteurs possibles : privé, privé et non assigné.'
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382192"
---
# <a name="sensor-pools"></a>Pools de capteurs

Pour prendre en charge les scénarios d’authentification Windows et l’authentification définie par le fournisseur, le service de biométrie Windows organise les unités biométriques en trois pools de capteurs possibles :

-   **Pool privé** collection d’unités biométriques allouées pour une utilisation exclusive par une application cliente. Les pools privés peuvent prendre en charge des scénarios d’authentification qui ne sont pas basés sur Windows, et ils permettent à une application d’accéder au matériel d’une unité biométrique de manière définie par un fournisseur. Il peut y avoir autant de pools de capteurs privés sur le système qu’il y a d’unités biométriques.
-   **Pool de capteurs système** collection d’unités biométriques partageables qui fournissent l’accès aux services d’authentification Windows. Ce pool est utilisé par Winlogon, UAC et tout autre client qui associe un SID à un modèle biométrique spécifique. Chaque fournisseur de services biométriques possède un pool de capteurs système.
-   Le **pool non assigné** contient une collection (éventuellement vide) d’unités biométriques qui ne sont pas affectées au pool système ou au pool privé.

Les applications peuvent utiliser le pool de systèmes partagés ou créer un pool privé constitué d’unités biométriques supprimées du système ou de pools non attribués. Quand une application libère son pool privé, les unités biométriques sont reconfigurées et retournées à leurs pools d’origine. Pour empêcher les attaques par déni de service, seuls les utilisateurs privilégiés sont autorisés à supprimer le dernier capteur du pool système. Pour plus d'informations, consultez les rubriques ci-dessous.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                       | Description                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pool de capteurs privés](private-sensor-pool.md)<br/>   | Collection d’unités biométriques réservée pour une utilisation exclusive par une application cliente. Les pools privés prennent en charge les méthodes d’authentification propriétaires et permettent à une application cliente d’accéder à une unité biométrique à l’aide de commandes de contrôle spécifiées par le fournisseur.<br/> |
| [Pool de capteurs système](system-sensor-pool.md)<br/>     | Collection d’unités biométriques partageables qui fournissent l’accès aux services d’authentification Windows. Ce pool est utilisé par Winlogon, UAC et tout autre client qui associe un SID à un modèle biométrique spécifique.<br/>                                 |
| [Comportement du pool système](system-pool-behavior.md)<br/> | Discussion sur les actions effectuées par le pool système lorsque des notifications d’événements sont envoyées et lorsqu’aucune opération biométrique n’est en attente.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’API Windows Biometric Framework](./biometric-service-api-portal.md)
</dt> </dl>

 

