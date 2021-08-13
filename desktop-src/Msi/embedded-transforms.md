---
description: Les transformations incorporées sont stockées dans le fichier .msi du package. Cela garantit aux utilisateurs que la transformation est toujours disponible lorsque le package d’installation est disponible. Les transformations peuvent également être fournies aux utilisateurs en tant que fichiers. MST autonomes.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Transformations incorporées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d7afb2b28599cb9ee2f10c4bc1fb25fbb0939fe68da5e817972eb8fc94236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637461"
---
# <a name="embedded-transforms"></a>Transformations incorporées

Les transformations incorporées sont stockées dans le fichier .msi du package. Cela garantit aux utilisateurs que la transformation est toujours disponible lorsque le package d’installation est disponible. Les transformations peuvent également être fournies aux utilisateurs en tant que fichiers. MST autonomes.

Pour ajouter une transformation incorporée à la liste des transformations, ajoutez un signe deux-points ( :) préfixe du nom de fichier. Étant donné que le programme d’installation peut toujours obtenir la transformation à partir du stockage dans le fichier .msi, les transformations incorporées ne sont pas mises en cache sur l’ordinateur de l’utilisateur. Les transformations incorporées peuvent être utilisées en association avec des transformations [sécurisées](secured-transforms.md) ou des [transformations non sécurisées](unsecured-transforms.md). Pour plus d’informations, consultez [application de transformations](applying-transforms.md).

 

 



