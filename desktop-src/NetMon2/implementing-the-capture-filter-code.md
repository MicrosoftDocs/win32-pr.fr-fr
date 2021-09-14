---
description: Une fois que vous avez déterminé comment organiser votre filtre à l’aide d’une structure CAPTUREFILTER, vous devez allouer et remplir la structure, qui est ensuite transmise au pilote Moniteur réseau via un objet BLOB de configuration.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Implémentation du code de filtre de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119250"
---
# <a name="implementing-the-capture-filter-code"></a>Implémentation du code de filtre de capture

Une fois que vous avez déterminé comment organiser votre filtre à l’aide d’une structure [**capturefilter**](capturefilter.md) , vous devez allouer et remplir la structure, qui est ensuite transmise au pilote Moniteur réseau via un objet blob de configuration.

les utilisateurs du NPP Direct ajoutent le filtre de capture à l’objet BLOB de configuration qui est transmis à **Connecter**, à la [**configuration**](configure.md), ou aux deux. Pour obtenir la liste des interfaces COM que vous pouvez utiliser pour communiquer avec le NPP, consultez [interfaces NPP](npp-interfaces.md).

 

 



