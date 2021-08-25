---
title: fonctions du Client Microsoft Media DRM pour Microsoft Windows
description: fonctions du Client Microsoft Media DRM pour Microsoft Windows
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media Format SDK, fonctions
- gestion des droits numériques (DRM), fonctions
- DRM (gestion des droits numériques), fonctions
- API étendues du client DRM, fonctions
- API étendues clientes, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aaf5f3c536027801a85f8d38120e6e14c5d366a6d727498a5bc1d1200cb041
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931169"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>fonctions du Client Microsoft Media DRM pour Microsoft Windows

les fonctions suivantes sont implémentées dans le cadre des api étendues du Client Windows Microsoft Media DRM.



| Fonction                                                             | Description                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMDRMCreateProvider**](wmdrmcreateprovider.md)                   | Crée une fabrique de classes qui peut créer les autres objets DRM. Cette fonction ne nécessite pas de bibliothèque de stubs de la part de Microsoft et crée des objets qui ne prennent pas en charge les fonctionnalités DRM protégées. |
| [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) | Crée une fabrique de classes qui peut créer les autres objets DRM. Cette fonction requiert une bibliothèque de stubs de la part de Microsoft et crée des objets qui prennent en charge les fonctionnalités DRM protégées.                |
| [**WMDRMShutdown**](wmdrmshutdown.md)                               | Libère les ressources utilisées par les API.                                                                                                                                                            |
| [**WMDRMStartup**](wmdrmstartup.md)                                 | Initialise les ressources utilisées par les API.                                                                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](drm-programming-reference.md)
</dt> </dl>

 

 




