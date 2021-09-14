---
description: Windows Le programme d’installation effectue les actions suivantes lors de la suppression d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Suppression de composants isolés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009655"
---
# <a name="removal-of-isolated-components"></a>Suppression de composants isolés

Windows Le programme d’installation effectue les actions suivantes lors de la suppression d’une application lorsque le package contient des composants isolés. En règle générale, \_ le composant partagé est une DLL partagée par l' \_ application composant et d’autres exécutables client.

## <a name="uninstall"></a>Désinstaller l’interface

-   Supprimer les fichiers du composant \_ partagé du dossier contenant l' \_ application composant uniquement si l' \_ application composant est également en cours de suppression.
-   Si le bit msidbComponentAttributesSharedDllRefCount est défini dans la [table des composants](component-table.md) , décrémente le refcount SharedDLL.
-   Supprimez. Fichier de zéro octet LOCAL à partir du dossier contenant l’application du composant \_ .
-   Supprimer \_ l’application composant de la liste des clients du composant \_ partagé.
-   Supprimez toutes les ressources de l' \_ application de composant comme d’habitude.

Si d’autres produits sont encore dans la liste des clients du composant \_ partagé :

-   Supprimer aucun fichier de l’emplacement partagé du composant \_ partagé.

Si le refcount SharedDLL pour le composant \_ partagé est 0 après avoir été décrémenté, ou s’il n’y a pas d’autres clients du composant \_ partagés :

-   Supprimez les fichiers du composant \_ partagés à partir de l’emplacement partagé.
-   Traiter toutes les actions de désinstallation par rapport à ce composant.

 

 



