---
description: Une alternative est une correspondance de mot potentielle pour un segment de reconnaissance. Un module de reconnaissance génère des alternatives et les base sur des correspondances acceptables de l’entrée d’encre ou audio par rapport à un dictionnaire ou un Factoid.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Alternatives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76faf27b82a6bfc064fddbad3d2d4ca6c2dddc098d56bca340b677cea17a319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119337039"
---
# <a name="alternates"></a>Alternatives

Une alternative est une correspondance de mot potentielle pour un segment de reconnaissance. Un module de reconnaissance génère des alternatives et les base sur des correspondances acceptables de l’entrée d’encre ou audio par rapport à un dictionnaire ou un Factoid.

> [!Note]  
> La version d’évaluation de la confiance est actuellement disponible uniquement pour l’anglais Microsoft (États-Unis) et les module de reconnaissance de mouvement.

 

Parfois, l’encre peut avoir des distinctions ambiguës entre les segments. Le module de reconnaissance compare ces segments à un dictionnaire de reconnaissance pour déterminer les correspondances possibles. Lorsque le module de reconnaissance compare les segments, il gère une liste de correspondances alternatives possibles et attribue un niveau de confiance à chacun d’eux, en choisissant un niveau de confiance.

> [!Note]  
> Le module de reconnaissance ne peut pas fournir de remplacements pour une partie de l’encre inférieure à un segment de reconnaissance.

 

 

 



