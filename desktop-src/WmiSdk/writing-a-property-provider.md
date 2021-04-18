---
description: Un fournisseur de propriétés récupère et modifie des valeurs de propriété individuelles pour les instances d’une classe donnée qui est stockée dans le référentiel WMI.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Écriture d’un fournisseur de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519936"
---
# <a name="writing-a-property-provider"></a>Écriture d’un fournisseur de propriétés

Un fournisseur de propriétés récupère et modifie des valeurs de propriété individuelles pour les instances d’une classe donnée qui est stockée dans le référentiel WMI.

La procédure suivante décrit comment créer un fournisseur de propriétés.

**Pour créer un fournisseur de propriétés**

1.  Concevez et inscrivez votre fournisseur avec WMI.

    Les fournisseurs d’instances s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) . Pour plus d’informations, consultez [inscription d’un fournisseur de propriétés](registering-a-property-provider.md).

2.  Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.

    WMI utilise [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour charger et initialiser un fournisseur. Il s’agit d’une tâche commune à tous les fournisseurs. Pour plus d’informations, consultez [initialisation d’un fournisseur](initializing-a-provider.md).

    > [!Note]  
    > Les fournisseurs de propriétés sont fortement encouragés à utiliser le modèle de multithreading « both ».

     

3.  Implémentez l’interface [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) pour votre fournisseur.

    L’interface [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) est l’interface principale d’un fournisseur de propriétés. Les deux méthodes principales sont [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) et [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty). Pour plus d’informations, consultez [implémentation de l’interface principale pour un fournisseur de propriétés](implementing-the-primary-interface-for-a-property-provider.md).

4.  Ajoutez tout code supplémentaire nécessaire pour votre fournisseur.

    Lorsque vous concevez votre fournisseur, vous devrez probablement appeler des interfaces WMI. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md) et [maintenance des niveaux de sécurité dans un fournisseur](impersonating-a-client.md).

    Lorsque vous récupérez des informations pour un client, vous devrez peut-être accéder aux niveaux de sécurité de ce client. Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).

5.  Remplacez le fournisseur préexistant par votre nouveau code.

    Vous n’avez pas besoin d’effectuer cette étape si vous n’avez pas de fournisseur préexistant à copier. Pour plus d’informations, consultez [mise à jour d’un fournisseur](updating-a-provider.md).

 

 



