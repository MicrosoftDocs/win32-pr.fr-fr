---
title: Interface utilisateur des versions précédentes supprimées pour les volumes locaux
description: Interface utilisateur des versions précédentes supprimées pour les volumes locaux
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104463830"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a>Interface utilisateur des versions précédentes supprimées pour les volumes locaux

## <a name="platform"></a>Plateforme

**Clients** – Windows 8 


## <a name="description"></a>Description

Les versions antérieures de Windows permettaient aux utilisateurs de restaurer des versions précédentes de fichiers individuels à partir de « clichés instantanés » de volumes locaux. Ces clichés instantanés sont créés par la fonctionnalité « versions précédentes » via le service de cliché instantané des volumes (VSS). Dans Windows 7, les utilisateurs pouvaient configurer et planifier des clichés instantanés dans l’interface utilisateur de protection du système disponible via les propriétés système.

Toutefois, les versions précédentes étaient rarement utilisées et ont eu un impact négatif sur les performances globales de Windows. par conséquent, la fonctionnalité a été supprimée. Dans Windows 8, ces fonctionnalités ne sont plus disponibles :

-   Possibilité de parcourir, de rechercher ou de restaurer des versions précédentes de fichiers par le biais de l’interface utilisateur des versions précédentes
-   Possibilité de configurer ou de planifier des versions précédentes de fichiers par le biais de l’interface utilisateur de la protection du système

Toutefois, les utilisateurs peuvent toujours utiliser l’onglet versions précédentes pour accéder aux partages de fichiers sur un serveur Windows.

## <a name="manifestation"></a>Manifestation

L’option versions précédentes n’est plus disponible pour les volumes locaux dans le menu des propriétés de l’Explorateur Windows.

## <a name="solution"></a>Solution

Les développeurs qui ont besoin de créer des clichés instantanés de volumes locaux peuvent toujours le faire en appelant des API VSS dans du code personnalisé.

 

 




