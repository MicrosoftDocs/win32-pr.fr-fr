---
description: Les transformations sécurisées sont parfois nécessaires pour des raisons de sécurité.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Transformations sécurisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869041"
---
# <a name="secured-transforms"></a>Transformations sécurisées

Les transformations sécurisées sont parfois nécessaires pour des raisons de sécurité. Les transformations sécurisées sont stockées localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur n’a pas d’accès en écriture sur un système de fichiers sécurisé. Ces transformations sont mises en cache à cet emplacement lors de l’installation ou de la publication du package. Seuls les administrateurs et le système local ont accès en écriture à cet emplacement. Un utilisateur non-administrateur ne peut pas modifier le fichier de transformation. Lors des installations ultérieures d’installation à la [demande](installation-on-demand.md) ou de [maintenance](maintenance-installation.md) du package, le programme d’installation utilise les transformations mises en cache.

Pour spécifier un stockage de transformation sécurisé, définissez la [stratégie TransformsSecure](transformssecure-policy.md), définissez la propriété [**TransformsSecure**](transformssecure.md) ou transmettez le \| symbole @ ou dans la liste transformations. Notez que vous ne pouvez pas inclure des transformations sécurisées et non sécurisées dans la même liste de transformations. Consultez [application de transformations](applying-transforms.md).

La suppression du produit par un utilisateur supprime toutes les transformations sécurisées pour ce produit de l’ordinateur de l’utilisateur.

Si le programme d’installation détecte qu’une transformation sécurisée n’est pas disponible localement, il tente de restaurer le cache de transformation à partir d’une source. Les transformations sécurisées peuvent être sécurisées au niveau source ou sécurisé-complet :

-   Les [transformations sécurisées à la source](secure-at-source-transforms.md) qui manquent dans le cache de transformation local sont restaurées à partir de la racine de la source du fichier. msi.
-   Les [transformations sécurisées de chemin d’accès complet](secure-full-path-transforms.md) qui manquent dans le cache de transformation local sont restaurées à partir du chemin d’accès complet d’origine spécifié par la liste des transformations.

 

 



