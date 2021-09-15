---
title: Support In-Process
description: L’implémentation actuelle de l’annotation dynamique est entièrement in-process et, par conséquent, autorise uniquement les éléments d’interface utilisateur à être annotés par le processus qui possède ces éléments d’interface utilisateur.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518280"
---
# <a name="in-process-support"></a>Support In-Process

L’implémentation actuelle de l’annotation dynamique est entièrement in-process et, par conséquent, autorise uniquement les éléments d’interface utilisateur à être annotés par le processus qui possède ces éléments d’interface utilisateur. Il n’est pas possible pour un processus d’annoter les éléments d’interface utilisateur d’un autre processus.

Notez que cela affecte uniquement l’acte de définition d’une annotation. Il n’interfère pas avec la capacité des clients à accéder aux propriétés (annotées ou autres) des éléments d’interface utilisateur dans d’autres processus.

 

 




