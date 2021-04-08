---
title: CENUMSCH. COTISATIONS
description: Dans l’exemple de composant fournisseur, l’énumération d’un objet de schéma utilise les méthodes de cenumsch. cpp, énumérées dans le tableau suivant.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcc6d053bb698817ff73db876b00640ed00c8ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839229"
---
# <a name="cenumschcpp"></a>CENUMSCH. COTISATIONS

Dans l’exemple de composant fournisseur, l’énumération d’un objet de schéma utilise les méthodes de cenumsch. cpp, énumérées dans le tableau suivant.



| Méthode                                        | Description                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **CSampleDSSchemaEnum :: Create**               | Créez un objet pour permettre l’énumération d’un objet de classe de schéma ADSI.                                                |
| **CSampleDSSchemaEnum::CSampleDSSchemaEnum**  | Constructeur standard.                                                                                                |
| **CSampleDSSchemaEnum :: ~ CSampleDSSchemaEnum** | Destructeur standard.                                                                                                 |
| **CSampleDSSchemaEnum :: suivant**                 | Récupère le nombre spécifié d’éléments de l’objet de schéma indiqué.                                          |
| **CSampleDSSchemaEnum :: EnumObjects**          | Gérez la récupération des pointeurs d’interfaces vers les objets du type d’objet indiqué.                               |
| **CSampleDSSchemaEnum :: EnumObjects**          | Gérer la récupération des pointeurs d’interface vers les objets du type d’objet par défaut.                                  |
| **CSampleDSSchemaEnum::EnumClasses**          | Gérer la récupération des pointeurs d’interface uniquement sur les objets de classe de schéma contenus dans cet objet.                  |
| **CSampleDSSchemaEnum :: GetClassObject,**       | Récupère la définition de classe de schéma suivante ; s’il est trouvé, créez un objet de classe de schéma et retournez le pointeur d’interface. |
| **CSampleDSSchemaEnum :: EnumProperties,**       | Gérer la récupération des pointeurs d’interface vers les objets de propriété contenus uniquement dans cet objet.                      |
| **CSampleDSSchemaEnum::GetPropertyObject**    | Récupère la définition de propriété suivante ; s’il est trouvé, créez un objet de classe de schéma et retournez le pointeur d’interface.     |
| **CSampleDSSchemaEnum::EnumSyntaxes**         | Gérer la récupération des pointeurs d’interface vers les objets de syntaxe contenus uniquement dans cet objet.                        |
| **CSampleDSSchemaEnum::GetSyntaxObject**      | Récupérer la définition de la syntaxe suivante ; s’il est trouvé, créez un objet de classe de schéma et retournez le pointeur d’interface.       |



 

 

 




