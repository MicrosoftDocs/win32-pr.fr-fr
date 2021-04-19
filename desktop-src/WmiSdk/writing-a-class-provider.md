---
description: Un fournisseur de classes gère une classe ou une série de classes pour WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Écriture d’un fournisseur de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517893"
---
# <a name="writing-a-class-provider"></a>Écriture d’un fournisseur de classe

Un fournisseur de classes gère une classe ou une série de classes pour WMI. Un fournisseur de classe peut être push ou pull ; autrement dit, il peut soit stocker ses propres données, soit autoriser WMI à stocker des données pour celui-ci dans le service de gestion Windows. Bien qu’un fournisseur de classes soit installé sur un ordinateur spécifique, il peut modifier les définitions de classe dans toute l’entreprise. Par conséquent, la plupart des développeurs ne créent pas souvent des fournisseurs de classes.

Avant de construire un fournisseur de classes, vérifiez que les classes prises en charge doivent réellement être générées dynamiquement. Dans la plupart des cas, la liste des classes est à variation lente et finie. Si c’est le cas, vous ne devez pas être obligé de créer un fournisseur de classe. Au lieu de cela, vous pouvez placer vos définitions de classe dans le référentiel WMI à l’aide de l’API WMI ou d’un fichier MOF.

La procédure suivante décrit comment implémenter un fournisseur de classes.

**Pour implémenter un fournisseur de classes**

1.  Déterminez si votre fournisseur est un fournisseur d’envoi ou d’extraction.

    Un fournisseur d’extraction fournit des données de manière dynamique en réponse à une demande de l’application, tandis que les fournisseurs de notifications push stockent leurs données une seule fois dans le référentiel WMI. Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md).

2.  Concevez et inscrivez votre fournisseur de classes avec WMI.

    Les fournisseurs de classes s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une instance [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) . Pour plus d’informations, consultez [inscription d’un fournisseur de classes](registering-a-class-provider.md).

3.  Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.

    WMI utilise [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour charger et initialiser un fournisseur. Si vous concevez un fournisseur push, **IWbemProviderInit** est la seule interface que vous allez implémenter. Pour plus d’informations, consultez [initialisation d’un fournisseur](initializing-a-provider.md).

    > [!Note]  
    > Les fournisseurs de classes sont fortement encouragés à utiliser le modèle de multithreading « both ».

     

4.  Ajoutez tout code supplémentaire nécessaire pour votre fournisseur.

    Lorsque vous concevez votre fournisseur, vous devrez probablement appeler des interfaces WMI. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md) et [maintenance des niveaux de sécurité dans un fournisseur](impersonating-a-client.md).

    Lorsque vous récupérez des informations pour un client, vous devrez peut-être accéder aux niveaux de sécurité de ce client. Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).

5.  Implémentez l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour votre fournisseur.

    L’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) est l’interface principale d’un fournisseur de classe pull. Pour plus d’informations, consultez [implémentation de l’interface principale pour un fournisseur de classes](implementing-the-primary-interface-for-a-class-provider.md).

6.  Remplacez le fournisseur préexistant par votre nouveau code.

    Vous n’avez pas besoin d’effectuer cette étape si vous n’avez pas de fournisseur préexistant à copier. Pour plus d’informations, consultez [mise à jour d’un fournisseur](updating-a-provider.md).

 

 



