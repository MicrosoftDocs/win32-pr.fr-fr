---
title: Fonctions d’extraction
description: Les fonctions d’extraction de gestion de réseau récupèrent les informations relatives à un domaine. Vous pouvez également appeler ces fonctions pour récupérer des informations sur les comptes d’utilisateur locaux, globaux, de station de travail et de serveur.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507291"
---
# <a name="get-functions"></a>Fonctions d’extraction

Les fonctions d’extraction de gestion de réseau récupèrent les informations relatives à un domaine. Vous pouvez également appeler ces fonctions pour récupérer des informations sur les comptes d’utilisateur locaux, globaux, de station de travail et de serveur.

Les fonctions d’extraction de gestion de réseau sont répertoriées ci-dessous.



| Fonction                                                               | Description                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Retourne le nom d’un contrôleur de domaine pour un domaine qui est directement approuvé par un serveur spécifié.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Retourne le nom du contrôleur de domaine principal (PDC) pour le domaine spécifié.                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Retourne l’index de la première entrée d’informations d’affichage dont le nom commence par une chaîne spécifiée ou qui suit la chaîne par ordre alphabétique. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Retourne des informations sur le compte de l’utilisateur, de l’ordinateur ou du groupe global.                                                                             |



 

Les informations retournées par la fonction [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) sont disponibles aux niveaux suivants :

-   [**\_groupe d’affichage net \_**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [**\_ordinateur net Display \_**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [**\_utilisateur NET Display \_**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




