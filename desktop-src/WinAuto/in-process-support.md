---
title: Support In-Process
description: L’implémentation actuelle de l’annotation dynamique est entièrement in-process et, par conséquent, autorise uniquement les éléments d’interface utilisateur à être annotés par le processus qui possède ces éléments d’interface utilisateur.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d82deaa2edd9a5df9fd36bed745d1c07a5542e12837cd3fc97c3ac0bdeab098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614739"
---
# <a name="in-process-support"></a>Support In-Process

L’implémentation actuelle de l’annotation dynamique est entièrement in-process et, par conséquent, autorise uniquement les éléments d’interface utilisateur à être annotés par le processus qui possède ces éléments d’interface utilisateur. Il n’est pas possible pour un processus d’annoter les éléments d’interface utilisateur d’un autre processus.

Notez que cela affecte uniquement l’acte de définition d’une annotation. Il n’interfère pas avec la capacité des clients à accéder aux propriétés (annotées ou autres) des éléments d’interface utilisateur dans d’autres processus.

 

 




