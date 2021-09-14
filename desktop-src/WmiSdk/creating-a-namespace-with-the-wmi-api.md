---
description: Une autre façon de créer un espace de noms consiste à utiliser l’API WMI pour créer l’espace de noms par programme.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Création d’un espace de noms avec l’API WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520216"
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

 

 



