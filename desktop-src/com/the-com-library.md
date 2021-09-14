---
title: Bibliothèque COM
description: Bibliothèque COM
ms.assetid: 51d4db4a-ad88-4627-8140-2f7906945752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a285a89ca659907c37f92b7d00f3e3e04d0acf51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221745"
---
# <a name="the-com-library"></a>Bibliothèque COM

Tout processus qui utilise COM doit à la fois initialiser et désinitialiser la bibliothèque COM. Outre le fait qu’il s’agit d’une spécification, COM implémente également certains services importants dans cette bibliothèque. fourni sous la forme d’un ensemble de dll et de fichiers exe (principalement Ole32.dll et Rpcss.exe) dans Microsoft Windows, la bibliothèque COM comprend les éléments suivants :

-   Un petit nombre de fonctions fondamentales qui facilitent la création d’applications COM, client et serveur. Pour les clients, COM fournit des fonctions de base pour la création d’objets. Pour les serveurs, COM fournit les moyens d’exposer leurs objets.

-   Services de localisation de l’implémentation par le biais desquels COM détermine, à partir d’un identificateur de classe unique (CLSID), le serveur qui implémente cette classe et où se trouve ce serveur. Ce service prend en charge un niveau d’indirection, généralement un registre système, entre l’identité d’une classe d’objet et l’empaquetage de l’implémentation afin que les clients soient indépendants de l’empaquetage, qui peut changer à l’avenir.

-   Appels de procédure distante transparents lorsqu’un objet s’exécute sur un serveur local ou distant.

-   Mécanisme standard pour permettre à une application de contrôler la façon dont la mémoire est allouée dans son processus, en particulier la mémoire qui doit être transmise entre les objets coopérants afin qu’elle puisse être libérée correctement.

Pour utiliser les services COM de base, tous les threads COM d’exécution dans les clients et les serveurs hors processus doivent appeler la fonction [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) avant d’appeler toute autre fonction com à l’exception des appels d’allocation de mémoire. **CoInitializeEx** remplace l’autre fonction, en ajoutant un paramètre qui vous permet de spécifier le modèle de thread du thread : thread cloisonné ou thread libre. Un appel à **CoInitialize** définit simplement le modèle de thread sur thread cloisonné.

Les applications de document composé OLE appellent la fonction [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) , qui appelle [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) et effectue également une initialisation requise pour les documents composés. Par conséquent, les threads qui appellent **OleInitialize** ne peuvent pas être libres de thread. Pour plus d’informations sur les threads dans les clients et les serveurs, consultez [processus, threads et Apartments](processes--threads--and-apartments.md).

Les serveurs in-process n’appellent pas les fonctions d’initialisation, car ils sont chargés dans un processus qui l’a déjà fait. Par conséquent, les serveurs in-process doivent définir leur modèle de thread dans le Registre sous la clé [InprocServer32](inprocserver32.md) . Pour plus d’informations sur les problèmes de Threading dans les serveurs in-process, consultez [problèmes de Threading du serveur in-process](in-process-server-threading-issues.md).

Il est également important de ne pas initialiser la bibliothèque. Pour chaque appel à [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), il doit y avoir un appel correspondant à [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Pour chaque appel à [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize), il doit y avoir un appel correspondant à [**OleUninitialize**](/windows/desktop/api/Ole2/nf-ole2-oleuninitialize).

Les serveurs in-process peuvent supposer que le processus dans lequel ils sont chargés a déjà effectué ces étapes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[COM (Component Object Model)](the-component-object-model.md)
</dt> </dl>

 

 




