---
title: À propos de l’API de mastérisation d’image
description: Cette documentation se concentre sur une description de l’implémentation Adaptec d’IMAPi pour Microsoft (IMAPIv1).
ms.assetid: 596ec3ea-17d1-4e60-8789-528ff00ae421
keywords:
- API de mastérisation d’image IMAPi, décrite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db1dc7846d2e47483abf2ca8856d593b874467f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104569680"
---
# <a name="about-the-image-mastering-api"></a>À propos de l’API de mastérisation d’image

Cette documentation se concentre sur une description de l’implémentation Adaptec d’IMAPi pour Microsoft (IMAPIv1). Ainsi, les descriptions des quatre objets COM principaux et de leurs interfaces sont incluses dans ce document. Les quatre objets principaux sont les suivants : **MSDiscMasterObj**, **MSDiscRecorderObj**, **MSDiscStashObj** et **MSBurnEngineObj**.

Plusieurs objets **MSDiscMasterObj** peuvent être instanciés sur un système, mais une seule application peut accéder à un enregistreur à la fois. Le **MSDiscMasterObj** implémente plusieurs interfaces, comme indiqué dans le diagramme d’objet suivant.

![msdiscmasterobj implémente plusieurs interfaces](images/imapi.png)

Les applications utilisent l’interface [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) pour effectuer les tâches suivantes :

-   Ouvrir IMAPi
-   Énumérer les formats pris en charge (Joliet et Redbook)
-   Sélectionner un format
-   Obtenir la liste des enregistreurs
-   Sélectionner un enregistreur
-   Démarrer une gravure

Les interfaces [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) et [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) sont retournées à une application par le biais de l’interface [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) lorsqu’un format est sélectionné. Ces interfaces contrôlent le contenu d’une donnée ou d’un disque audio, respectivement. Il n’est pas prévu que chaque application comprenne les interfaces de format spécifiques. Les applications peuvent accéder aux propriétés génériques de l’interface **IJolietDiscMaster** , telles que le nom du volume ou le nom du fichier hérité.

Les objets **MSDiscRecorderObj** sont accessibles par le biais de l’interface [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) . Chaque périphérique CD-R ou CD-RW compatible avec IMAPi est associé à un objet **MSDiscRecorderObj** . Une application utilise des pointeurs vers l’interface **IDiscRecorder** sur ces objets pour sélectionner l’appareil qui sera utilisé par IMAPI pour enregistrer un CD. En outre, les applications peuvent accéder aux propriétés génériques d’un enregistreur via **IDiscRecorder**. Cela comprend des propriétés telles que la vitesse de l’enregistreur ou d’autres paramètres de gravure.

Les objets restants, **MSDiscStashObj** et **MSBurnEngineObj**, sont des objets internes auxquels IMAPI accède. Ils sont mentionnés ici uniquement pour clarifier l’architecture IMAPi. Le **MSDiscStashObj** représente (via l’interface **IDiscStash** ) un fichier brut d’une taille maximale de 800 Mo utilisée par **MSDiscMasterObj** pour créer des images audio ou des disques de données à graver. La dissimulation est transmise à **MSBurnEngineObj** (via l’interface **IMSBurnEngine** ) lorsqu’une gravure est demandée à partir du moteur de niveau inférieur. L’objet **MSBurnEngineObj** s’attend à ce que le contenu de la dissimulation soit dans un format connu. À cet égard, **MSDiscMasterObj** et **MSBurnEngineObj** ont un contrat concernant le contenu de la dissimulation.

 

 




