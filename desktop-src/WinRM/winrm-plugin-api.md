---
title: API du plug-in WinRM
description: L’interface de programmation d’applications (API) du plug-in WinRM fournit des fonctionnalités qui permettent à un utilisateur d’écrire des plug-ins en implémentant certaines API pour les opérations et URI de ressources pris en charge.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7359ed212e50b71343ce9a96832060e9ec8121cdf3e11f3f353698e1a4fa9dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742776"
---
# <a name="winrm-plug-in-api"></a>API du plug-in WinRM

Windows Les plug-ins de gestion à distance sont des bibliothèques de liens dynamiques (dll) natives qui se connectent et étendent les fonctionnalités de WinRM. L’interface de programmation d’applications (API) du plug-in WinRM fournit des fonctionnalités qui permettent à un utilisateur d’écrire des plug-ins en implémentant certaines API pour les opérations et [*URI de ressources*](windows-remote-management-glossary.md) pris en charge. une fois les plug-ins configurés pour le service winrm ou Internet Information Services (iis), ils sont chargés dans l’hôte WinRM ou l’hôte iis, respectivement. Les demandes distantes sont routées vers ces points d’entrée de plug-in pour effectuer des opérations.

La section informations de référence sur l’API du plug-in WinRM contient des informations détaillées sur les éléments d’API suivants :

-   [Points d’entrée du plug-in d’autorisation](authorization-plug-in-entry-points.md)
-   [Méthodes de plug-in d’autorisation](authorization-plug-in-methods.md)
-   [Points d’entrée du plug-in opérations](operations-plug-in-entry-points.md)
-   [Méthodes de plug-in Operations](operations-plug-in-methods.md)
-   [Structures](winrm-plug-in-api-structures.md)

 

 




