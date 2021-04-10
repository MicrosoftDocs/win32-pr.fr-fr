---
description: Une fois que vous avez déterminé comment organiser votre filtre à l’aide d’une structure CAPTUREFILTER, vous devez allouer et remplir la structure, qui est ensuite transmise au pilote Moniteur réseau via un objet BLOB de configuration.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Implémentation du code de filtre de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869241"
---
# <a name="implementing-the-capture-filter-code"></a>Implémentation du code de filtre de capture

Une fois que vous avez déterminé comment organiser votre filtre à l’aide d’une structure [**capturefilter**](capturefilter.md) , vous devez allouer et remplir la structure, qui est ensuite transmise au pilote Moniteur réseau via un objet blob de configuration.

Les utilisateurs du NPP direct ajoutent le filtre de capture à l’objet BLOB de configuration qui est transmis à **Connect**, à [**configure**](configure.md), ou aux deux. Pour obtenir la liste des interfaces COM que vous pouvez utiliser pour communiquer avec le NPP, consultez [interfaces NPP](npp-interfaces.md).

 

 



