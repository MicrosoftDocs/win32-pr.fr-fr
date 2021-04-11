---
title: Mise à jour des règles de détection des applications de sécurité
description: Mise à jour des règles de détection des applications de sécurité
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031989"
---
# <a name="security-app-detection-rules-update"></a>Mise à jour des règles de détection des applications de sécurité

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


### <a name="description"></a>Description

Les applications du Windows Store ajoutées dans Windows 8 sont toutes installées à un emplacement commun sous « Program Files » (% ProgramFiles%) appelé \\ Program Files \\ WindowsApps.

### <a name="manifestation"></a>Manifestation

Cela peut provoquer des collisions avec les configurations existantes, et certains détecteurs d’antivirus/anti-programme malveillant voient cet emplacement comme un emplacement potentiel qui est à l’origine de la préoccupation.

### <a name="mitigation"></a>Limitation des risques

Les recommandations actuelles sont les suivantes :

-   Quitter \\ les fichiers programme \\ WindowsApps pour stocker les applications personnalisées
-   Les fournisseurs d’antivirus et de logiciels anti-programme malveillant doivent mettre à jour leurs heuristiques afin qu’ils n’identifient pas cet emplacement comme un emplacement malveillant

 

 




