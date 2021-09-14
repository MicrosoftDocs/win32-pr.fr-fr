---
description: 'Si vous utilisez l’API COM pour WMI pour récupérer ou stocker des informations de classe localisées, spécifiez les paramètres régionaux dans le paramètre strLocale de l’interface IWbemLocator :: ConnectServer.'
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Récupération des classes modifiées à l’aide de l’API COM pour WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008211"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a>Récupération des classes modifiées à l’aide de l’API COM pour WMI

Si vous utilisez l’API COM pour WMI pour récupérer ou stocker des informations de classe localisées, spécifiez les paramètres régionaux dans le paramètre *strLocale* de l’interface [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) . Lors de la lecture ou de l’écriture de classes modifiées, indiquez que vous souhaitez utiliser les définitions de classe localisées en spécifiant \_ l’indicateur WBEM \_ utiliser \_ \_ des qualificateurs modifiés comme indicateur pour le paramètre *IFlags* .

Le tableau suivant répertorie les versions synchrones et asynchrones des méthodes qui utilisent l’indicateur WBEM \_ \_ utiliser des \_ \_ qualificateurs modifiés.



| Méthode synchrone                                                            | Méthode asynchrone                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IWbemServices :: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [**IWbemServices :: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [**IWbemServices :: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [**IWbemServices :: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [**IWbemServices :: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [**IWbemServices ::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [**IWbemServices ::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [**IWbemServices ::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [**IWbemServices ::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



