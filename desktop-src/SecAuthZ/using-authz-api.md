---
description: L’API auth permet aux applications d’effectuer des vérifications d’accès personnalisables avec de meilleures performances et un développement plus simplifié que les Access Control de bas niveau.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Utilisation de l’API auth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320858"
---
# <a name="using-authz-api"></a>Utilisation de l’API auth

L’API auth permet aux applications d’effectuer des vérifications d’accès personnalisables avec de meilleures performances et un développement plus simplifié que les [Access Control de bas niveau](low-level-access-control.md).

AUTH API permet aux applications de mettre en cache les contrôles d’accès pour améliorer les performances, d’interroger et de modifier les contextes du client, et de définir des règles d’entreprise qui peuvent être utilisées pour évaluer dynamiquement l’autorisation d’accès.

## <a name="in-this-section"></a>Dans cette section



| Rubrique                                                                             | Description                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Initialisation d’un contexte client](initializing-a-client-context.md)<br/>     | Une application doit créer un contexte client pour pouvoir utiliser l’API auth pour effectuer des vérifications d’accès ou un audit.<br/>                                                                                                                                            |
| [Interrogation d’un contexte client](querying-a-client-context.md)<br/>             | Les applications peuvent appeler la fonction [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) pour demander des informations sur un contexte client existant.<br/>                                                                                       |
| [Ajout de sid à un contexte client](adding-sids-to-a-client-context.md)<br/> | Une application peut ajouter des [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) à un contexte client existant en appelant la fonction [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .<br/> |
| [Vérification de l’accès avec l’API auth](checking-access-with-authz-api.md)<br/>   | Les applications déterminent s’il faut accorder l’accès aux objets sécurisables en appelant la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .<br/>                                                                                                                |
| [Mise en cache des contrôles d’accès](caching-access-checks.md)<br/>                     | Quand une application effectue une vérification d’accès en appelant la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , les résultats de cette vérification d’accès peuvent être mis en cache.<br/>                                                                                       |



 

 

