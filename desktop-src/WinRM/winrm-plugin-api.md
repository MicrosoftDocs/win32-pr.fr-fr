---
title: API du plug-in WinRM
description: L’interface de programmation d’applications (API) du plug-in WinRM fournit des fonctionnalités qui permettent à un utilisateur d’écrire des plug-ins en implémentant certaines API pour les opérations et URI de ressources pris en charge.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940121"
---
# <a name="winrm-plug-in-api"></a>API du plug-in WinRM

Les plug-ins Windows Remote Management sont des bibliothèques de liens dynamiques (dll) natives qui s’y connectent et étendent les fonctionnalités de WinRM. L’interface de programmation d’applications (API) du plug-in WinRM fournit des fonctionnalités qui permettent à un utilisateur d’écrire des plug-ins en implémentant certaines API pour les opérations et [*URI de ressources*](windows-remote-management-glossary.md) pris en charge. Une fois les plug-ins configurés pour le service WinRM ou Internet Information Services (IIS), ils sont chargés dans l’hôte WinRM ou l’hôte IIS, respectivement. Les demandes distantes sont routées vers ces points d’entrée de plug-in pour effectuer des opérations.

La section informations de référence sur l’API du plug-in WinRM contient des informations détaillées sur les éléments d’API suivants :

-   [Points d’entrée du plug-in d’autorisation](authorization-plug-in-entry-points.md)
-   [Méthodes de plug-in d’autorisation](authorization-plug-in-methods.md)
-   [Points d’entrée du plug-in opérations](operations-plug-in-entry-points.md)
-   [Méthodes de plug-in Operations](operations-plug-in-methods.md)
-   [Structures](winrm-plug-in-api-structures.md)

 

 




