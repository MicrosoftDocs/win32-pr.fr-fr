---
description: Les transformations incorporées sont stockées dans le fichier. msi du package. Cela garantit aux utilisateurs que la transformation est toujours disponible lorsque le package d’installation est disponible. Les transformations peuvent également être fournies aux utilisateurs en tant que fichiers. MST autonomes.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Transformations incorporées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034642"
---
# <a name="embedded-transforms"></a>Transformations incorporées

Les transformations incorporées sont stockées dans le fichier. msi du package. Cela garantit aux utilisateurs que la transformation est toujours disponible lorsque le package d’installation est disponible. Les transformations peuvent également être fournies aux utilisateurs en tant que fichiers. MST autonomes.

Pour ajouter une transformation incorporée à la liste des transformations, ajoutez un signe deux-points ( :) préfixe du nom de fichier. Étant donné que le programme d’installation peut toujours obtenir la transformation à partir du stockage dans le fichier. msi, les transformations incorporées ne sont pas mises en cache sur l’ordinateur de l’utilisateur. Les transformations incorporées peuvent être utilisées en association avec des transformations [sécurisées](secured-transforms.md) ou des [transformations non sécurisées](unsecured-transforms.md). Pour plus d’informations, consultez [application de transformations](applying-transforms.md).

 

 



