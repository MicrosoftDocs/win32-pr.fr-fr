---
description: Les transformations qui n’ont pas été sécurisées, comme décrit dans transformations sécurisées, sont des transformations non sécurisées par défaut.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Transformations non sécurisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545160"
---
# <a name="unsecured-transforms"></a>Transformations non sécurisées

Les transformations qui n’ont pas été sécurisées, comme décrit dans [transformations sécurisées](secured-transforms.md) , sont des transformations non sécurisées par défaut.

Pour appliquer une transformation non sécurisée lors de l’installation d’un package, transmettez les noms des fichiers de transformation dans la chaîne de la propriété [**TRANSformations**](transforms.md) ou de la ligne de commande. Ne commencez pas la chaîne par les caractères @ ou \| , ou définissez la [stratégie TransformsSecure](transformssecure-policy.md) ou la propriété [**TransformsSecure**](transformssecure.md) . Notez que vous ne pouvez pas combiner des transformations sécurisées et des transformations [sécurisées](secured-transforms.md) dans la même liste de transformations.

Si le package est installé ou publié dans le [contexte d’installation](installation-context.md)par utilisateur et qu’il comporte des transformations non sécurisées, le programme d’installation enregistre la source de transformation dans le dossier Application Data du profil de l’utilisateur. Cela permet à un utilisateur de gérer la personnalisation d’un produit tout en se déplaçant d’un ordinateur à l’autre.

Si le package est installé ou publié dans le [contexte d’installation](installation-context.md)par ordinateur et utilise des transformations non sécurisées, le programme d’installation enregistre la source de transformation dans le dossier% windir% \\ installer.

Lors de la première installation du package, le programme d’installation commence par Rechercher la transformation à la source fournie par la propriété [**TRANSformations**](transforms.md) ou la chaîne de ligne de commande. Si cette source n’est pas disponible, le programme d’installation recherche la transformation à la source du package à côté du fichier. msi.

Pendant une [installation de maintenance](maintenance-installation.md), le programme d’installation recherche la transformation à l’emplacement du cache. Si la copie mise en cache de la transformation devient indisponible, le programme d’installation recherche la transformation à la source du package à côté du fichier. msi.

Pour plus d’informations, consultez [application de transformations](applying-transforms.md) et [résilience source](source-resiliency.md).

 

 



