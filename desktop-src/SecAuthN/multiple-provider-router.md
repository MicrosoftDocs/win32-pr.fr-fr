---
description: Le routeur de fournisseur multiple gère la communication entre le système d’exploitation Windows et les fournisseurs de réseau installés. Il permet à Windows de présenter un réseau intégré à l’utilisateur.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Routeur à plusieurs fournisseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867246"
---
# <a name="multiple-provider-router"></a>Routeur à plusieurs fournisseurs

Le [*routeur de fournisseur multiple*](../secgloss/m-gly.md) gère la communication entre le système d’exploitation Windows et les fournisseurs de réseau installés. Il permet à Windows de présenter un réseau intégré à l’utilisateur.

Au démarrage de MPR, il vérifie le registre pour déterminer quels fournisseurs de réseau sont installés sur le système et l’ordre dans lequel ils doivent être recycles. Il charge toutes les dll de fournisseur réseau inscrites et les utilise pour traiter les appels WNet suivants effectués par l’interface utilisateur ou d’autres applications.

Pour plus d’informations sur les fonctions WNet, consultez [mise en réseau Windows](../wnet/windows-networking-wnet-.md).

 

 
