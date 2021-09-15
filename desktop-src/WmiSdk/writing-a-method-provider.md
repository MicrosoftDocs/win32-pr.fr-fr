---
description: Un fournisseur de méthode autorise l’accès WMI aux méthodes d’une classe. Par exemple, une classe qui représente une application peut avoir une méthode qui termine l’application.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Écriture d’un fournisseur de méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520525"
---
# <a name="writing-a-method-provider"></a>Écriture d’un fournisseur de méthode

Un fournisseur de méthode autorise l’accès WMI aux méthodes d’une classe. Par exemple, une classe qui représente une application peut avoir une méthode qui termine l’application.

La modification de l’ordre des paramètres d’entrée et de sortie de la méthode lors de la mise à jour d’un fournisseur de méthodes existant peut provoquer un échec pour les applications qui appellent la méthode. L’ordre des paramètres d’entrée ou de sortie est établi par la valeur du qualificateur d' [**ID**](standard-wmi-qualifiers.md) sur chaque paramètre. Le premier paramètre a une valeur d' **ID** égale à zéro. Ajoutez de nouveaux paramètres d’entrée à la fin des paramètres existants au lieu de les insérer dans la séquence déjà établie.

La procédure suivante décrit comment implémenter un fournisseur de méthodes.

**Pour implémenter un fournisseur de méthode**

1.  Concevez et inscrivez votre fournisseur de classes avec WMI.

    Les fournisseurs de classes s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) . Pour plus d’informations, consultez [inscription d’un fournisseur de méthodes](registering-a-method-provider.md).

2.  Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.

    > [!Note]  
    > Les fournisseurs de méthode sont fortement encouragés à utiliser le modèle de multithreading « both ».

     

3.  Implémentez la méthode [**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) pour votre fournisseur.

    L’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) est l’interface principale d’un fournisseur de méthode. Pour plus d’informations, consultez [implémentation de l’interface principale pour un fournisseur de méthodes](implementing-the-primary-interface-for-a-method-provider.md).

4.  Ajoutez tout code supplémentaire nécessaire pour votre fournisseur.

    Lorsque vous concevez votre fournisseur, vous devrez probablement appeler des interfaces WMI. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md) et [maintenance des niveaux de sécurité dans un fournisseur](impersonating-a-client.md).

    Lorsque vous récupérez des informations pour un client, vous devrez peut-être accéder aux niveaux de sécurité de ce client. Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).

5.  Remplacez le fournisseur préexistant par votre nouveau code.

    Vous n’avez pas besoin d’effectuer cette étape si vous n’avez pas de fournisseur préexistant à copier. Pour plus d’informations, consultez [mise à jour d’un fournisseur](updating-a-provider.md).

 

 



