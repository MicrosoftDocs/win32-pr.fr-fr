---
description: La table CounterDetails décrit un compteur spécifique sur un ordinateur particulier.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: CounterDetails
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952018"
---
# <a name="counterdetails"></a>CounterDetails

La table **CounterDetails** décrit un compteur spécifique sur un ordinateur particulier.

La table **CounterDetails** définit les champs suivants :

-   **CounterID :** Identificateur unique dans la base de données qui mappe à une chaîne de texte de nom de compteur spécifique. Ce champ est la clé primaire de cette table.
-   **MachineName :** Nom de l’ordinateur qui a enregistré ce jeu de données.
-   **ObjectName :** Nom de l’objet de performance.
-   **CounterName :** Nom du compteur.
-   Au-dessus de **:** Type de compteur. Pour obtenir la liste des types de compteurs et leurs formules, consultez la section types de compteurs du [Kit de déploiement de Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).
-   **DEFAULTSCALE :** Mise à l’échelle par défaut à appliquer aux données de compteur de performances brutes.
-   **Nom_instance :** Nom de l’instance de compteur.
-   **InstanceIndex :** Numéro d’index de l’instance de compteur.
-   **ParentName :** Certains compteurs sont logiquement associés à d’autres, et sont appelés parents. Par exemple, le parent d’un thread est un processus et le parent d’un pilote de disque logique est un lecteur physique. Ce champ contient le nom du parent. Soit la valeur de ce champ, soit le champ **ParentObjectID** identifie une instance parent spécifique. Si la valeur de ce champ est **null**, la valeur du champ **ParentObjectID** doit être vérifiée pour identifier le parent. Si les valeurs des deux champs sont **null**, le compteur n’a pas de parent.
-   **ParentObjectID :** Identificateur unique du parent. La valeur de ce champ ou du champ **ParentName** identifie une instance parent spécifique. Si la valeur de ce champ est **null**, la valeur du champ **ParentName** doit être vérifiée pour identifier le parent.

 

 
