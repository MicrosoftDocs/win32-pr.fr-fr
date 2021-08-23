---
description: Une autre façon de créer un espace de noms consiste à utiliser l’API WMI pour créer l’espace de noms par programme.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Création d’un espace de noms avec l’API WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192bb38b60c3d0ddefb8cc1e5cb7b5f78cb0f5ba7937d39784729e0f61f70b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612539"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Création d’un espace de noms avec l’API WMI

Une autre façon de créer un espace de noms consiste à utiliser l’API WMI pour créer l’espace de noms par programme. L’avantage de créer un espace de noms par programme est que vous pouvez créer l’espace de noms à partir d’une application. Toutefois, l’utilisation de l’API WMI est plus complexe que l’utilisation de code format MOF (MOF) et vous ne pouvez pas aussi partager facilement vos espaces de noms avec d’autres développeurs.

La procédure suivante décrit comment créer un espace de noms à l’aide de l’API WMI.

**Pour créer un espace de noms à l’aide de l’API WMI**

1.  Utilisez [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) pour récupérer un pointeur vers un objet [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) qui pointe vers la classe système d' [**\_ \_ espace de noms**](--namespace.md) .
2.  Définissez une instance de la classe système d' [**\_ \_ espace de noms**](--namespace.md) avec un appel à [**IWbemClassObject :: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).
3.  Définissez la propriété **Name** de l’instance d' [**\_ \_ espace de noms**](--namespace.md) avec un appel à [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).
4.  Créez l’espace de noms avec un appel à [**IWbemServices ::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).

    Le paramètre *Pint* de [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) doit pointer vers la nouvelle instance.

 

 



