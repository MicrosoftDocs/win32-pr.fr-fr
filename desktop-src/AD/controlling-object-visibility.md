---
title: Contrôle de la visibilité des objets
description: Les Active Directory Domain Services permettent de masquer les objets des utilisateurs qui se sont vu refuser certains droits.
ms.assetid: 3a65ec79-7de0-4d14-b980-1ca6a972ac70
ms.tgt_platform: multiple
keywords:
- contrôle de la visibilité des objets Active Directory
- Active Directory Active Directory, utilisation de, contrôle de la visibilité des objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b1ab364f0711174d5ac1dd1e4fbe98303c50b3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031039"
---
# <a name="controlling-object-visibility"></a>Contrôle de la visibilité des objets

Les Active Directory Domain Services permettent de masquer les objets des utilisateurs qui se sont vu refuser certains droits. Si un objet est masqué, une application qui s’exécute avec les informations d’identification d’un utilisateur ne sera pas en mesure d’effectuer une énumération ou une liaison à l’objet.

Si un utilisateur se voit accorder le droit de contrôle d’accès à la [**\_ \_ \_ liste ACTRL DS \_ List**](/windows/win32/api/iads/ne-iads-ads_rights_enum) dans un conteneur, il peut afficher tous les objets enfants du conteneur. De même, si un utilisateur se voit refuser le droit de contrôle d’accès à la **\_ \_ \_ liste ACTRL DS \_ List** dans un conteneur, l’utilisateur ne peut pas afficher les objets enfants du conteneur. Cela permet de masquer le contenu des conteneurs entiers.

Le serveur Active Directory peut également être placé dans un mode d’objet de liste spécial en définissant le troisième caractère de la propriété [**dSHeuristics**](/windows/desktop/ADSchema/a-dsheuristics) sur « 1 ». Le mode objet de liste peut être désactivé en définissant le troisième caractère de la propriété **dSHeuristics** sur « 0 ». Quand le serveur Active Directory est en mode d’objet liste, un objet est toujours visible si l’utilisateur a obtenu le droit [**\_ \_ ACTRL \_ DS \_ List**](/windows/win32/api/iads/ne-iads-ads_rights_enum) sur l’objet parent. Toutefois, si l’utilisateur a refusé la liste de **\_ \_ ACTRL \_ DS \_** de la liste de droits sur le parent, les objets enfants spécifiques peuvent toujours être rendus visibles si l’utilisateur reçoit l’objet de liste des **services de domaine Active \_ \_ Directory \_ \_** droit sur les objets parents et enfants. Le mode objet de liste permet à l’administrateur système d’accorder ou de refuser l’accès à des objets individuels pour des utilisateurs ou des groupes. Le mode d’objet de liste doit être utilisé avec modération, car il requiert un nombre beaucoup plus élevé d’appels de vérification d’accès que le service d’annuaire doit effectuer pour déterminer si un objet est visible pour un utilisateur. Il peut donc avoir un effet négatif sur les performances de la navigation ou de la lecture d’objets à partir de Active Directory Domain Services.

 

 