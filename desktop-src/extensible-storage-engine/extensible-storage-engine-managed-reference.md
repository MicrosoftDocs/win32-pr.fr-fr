---
description: 'En savoir plus sur : référence gérée par le moteur de stockage extensible'
title: Référence gérée du moteur de stockage extensible
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034168"
---
# <a name="extensible-storage-engine-managed-reference"></a>Référence gérée du moteur de stockage extensible

Recherchez des informations de référence pour la bibliothèque ManagedESENT. La bibliothèque ManagedESENT fournit un accès géré à ESENT, le moteur de base de données pouvant être incorporé natif à Windows.


_**S’applique à :** Windows | Serveur Windows_

**Dans cet article**  
Comment la bibliothèque ManagedESENT est-elle différente de ESENT ?  
Configuration requise  
Dans cette section  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>Comment la bibliothèque ManagedESENT est-elle différente de ESENT ?

ESENT est un moteur de base de données transactionnelle, pouvant être incorporé, qui vous permet de créer des applications personnalisées qui nécessitent un stockage de données fiable, hautes performances et à faible charge. Le moteur ESENT peut aider à répondre à des besoins de données qui vont d’un point aussi simple qu’une table de hachage qui est trop volumineuse pour être stockée en mémoire, plus complexe, comme une application avec des tables, des colonnes et des index. Pour créer une application avec ESENT, vous utilisez la DLL esent.dll qui fait partie du système d’exploitation Windows et écrivez votre code avec C/C++. Pour plus d’informations sur ESENT, consultez informations de référence sur le [moteur de stockage extensible](./extensible-storage-engine-reference.md).

ManagedESENT s’appuie sur esent.dll, qui fait partie de Windows, il n’y a donc pas de fichiers binaires non gérés supplémentaires à télécharger et à installer. Avec la bibliothèque ManagedESENT, vous pouvez créer votre application à l’aide d’un langage managé tel que C \# au lieu de c/C++. La bibliothèque utilise les mêmes noms de types et de membres pour exposer l’API ESE. par conséquent, si vous êtes déjà familiarisé avec la structure de cette API, vous pouvez facilement passer à cette bibliothèque managée.

## <a name="requirements"></a>Configuration requise

Cette bibliothèque managée requiert les éléments suivants :

  - Un ordinateur exécutant une version de Windows à partir de Windows Vista

  - Visual Studio 2012

  - .NET Framework 4.5

## <a name="in-this-section"></a>Dans cette section

  - [Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)

  - [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [Microsoft. ISAM. esent. Interop. une](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
