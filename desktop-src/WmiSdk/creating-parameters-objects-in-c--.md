---
description: 'Les méthodes IWbemServices :: ExecMethod ou ExecMethodAsync requièrent la \_ \_ classe système Parameters en tant que conteneur dans pInParams si la méthode qu’elles exécutent possède des arguments d’entrée.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Création d’objets de paramètres en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202297"
---
# <a name="creating-parameters-objects-in-c"></a>Création d’objets de paramètres en C++

Les méthodes [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) requièrent la classe système [**\_ \_ Parameters**](--parameters.md) en tant que conteneur dans *pInParams* si la méthode qu’elles exécutent possède des arguments d’entrée.

La procédure suivante décrit comment créer une instance de la classe système [**\_ \_ Parameters**](--parameters.md) pour contenir les informations sur les paramètres.

**Pour créer une instance de \_ \_ paramètres**

1.  Déterminez le chemin d’accès de la classe contenant la définition de la méthode.
2.  En utilisant le chemin de classe et le pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) transmis à partir de [**IWbemProviderInit :: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), appelez [**IWbemClassObject :: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) pour récupérer les classes de paramètres d’entrée et de sortie.

    La méthode [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) retourne un pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pour accéder à chacune de ces classes.

3.  À l’aide du pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pour la classe de sortie, appelez [**IWbemClassObject :: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) pour créer une instance de la classe.
4.  Remplissez l’instance de classe en définissant les propriétés qui correspondent aux valeurs de sortie et, s’il existe une valeur de retour pour la méthode, la propriété [returnValue](creating-a-method.md) .
5.  Transmettez l’instance de [**\_ \_ paramètres**](--parameters.md) à l’appelant par le biais de la méthode [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

Une fois que le fournisseur de méthode a déterminé que les paramètres d’entrée sont corrects, la méthode vers laquelle pointe *strMethodName* peut toujours réussir ou échouer. Certains fournisseurs de méthode génèrent un deuxième thread pour implémenter la méthode afin que la réussite ou l’échec réel de la méthode finit par être signalé à l’appelant via [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Notez que **IWbemObjectSink :: SetStatus** ne reçoit pas le code de retour de la méthode du fournisseur. Toutefois, elle reçoit le code de retour du mécanisme réel de retour d’appel et est utile uniquement pour vérifier que l’appel s’est produit ou qu’il a échoué pour des raisons mécaniques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> <dt>

[**IWbemCallResult::GetResultObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



