---
title: InprocServer32
description: Inscrit un serveur in-process 32 bits et spécifie le modèle de thread du cloisonnement sur lequel le serveur peut s’exécuter.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- Clé de Registre InprocServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998894"
---
# <a name="inprocserver32"></a>InprocServer32

Inscrit un serveur in-process 32 bits et spécifie le modèle de thread du cloisonnement sur lequel le serveur peut s’exécuter.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a>Notes

**ThreadingModel** est une valeur de **reg \_ SZ** qui spécifie le modèle de thread. Les valeurs possibles sont indiquées dans le tableau suivant.



| Valeur     | Description                                |
|-----------|--------------------------------------------|
| STA | Cloisonnement à thread unique                  |
| Les deux      | Cloisonnement monothread ou multithread |
| Gratuit      | Multithread cloisonné                    |
| Neutre   | Cloisonnement neutre                          |



 

Vous devez utiliser la même valeur pour chaque objet fourni par le serveur in-process.

Si **ThreadingModel** n’est pas présent ou n’est pas défini sur une valeur, le serveur est chargé dans le premier cloisonnement qui a été initialisé dans le processus. Ce cloisonnement est parfois appelé STA (Single-Threaded Apartment). Si le premier STA d’un processus est initialisé par COM, plutôt que par un appel explicite à [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), il est appelé STA de l’hôte. Par exemple, COM crée un STA hôte si un serveur in-process à charger requiert un STA, mais qu’il n’existe actuellement aucun STA dans le processus.

Dans la mesure du possible, le serveur in-process est chargé dans le même cloisonnement que le client qui le charge. Si le modèle de thread de l’Apartment client n’est pas compatible avec le modèle spécifié, le serveur est chargé comme indiqué dans le tableau suivant.



| Modèle de thread du serveur | Serveur cloisonné en cours d’exécution |
|---------------------------|----------------------------|
| <not specified>     | STA principal                   |
| Les deux                      | Même cloisonnement que le client   |
| Gratuit                      | Multithread cloisonné    |
| Neutre                   | Cloisonnement neutre          |



 

Si le modèle de thread du serveur est cloisonné, le cloisonnement dans lequel le serveur est chargé dépend de l’appartement dans lequel le client s’exécute, comme indiqué dans le tableau suivant.



| Le client Apartment est exécuté dans | Serveur cloisonné en cours d’exécution |
|----------------------------|----------------------------|
| Multithread              | STA hôte                   |
| Neutral (sur thread STA)    | Même cloisonnement que le client   |
| Neutral (sur thread MTA)    | STA hôte                   |



 

COM peut également créer un hôte multithread cloisonné (MTA). Si un client d’un cloisonnement à thread unique demande un serveur in-process dont le modèle de thread est libre en l’absence de MTA dans le processus, COM crée un MTA hôte et y charge le serveur.

Pour un serveur in-process 32 bits, les clés [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32** et [**Insertable**](insertable.md) doivent être inscrites. L’entrée **InprocServer** est nécessaire uniquement pour la compatibilité descendante. Si elle est manquante, la classe fonctionne toujours, mais elle ne peut pas être chargée dans des applications 16 bits.

Si un conteneur recherche un serveur in-process dans le registre, la version 16 bits a la priorité sur un conteneur de 16 bits et la version 32 bits a la priorité sur un conteneur 32 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**InprocServer**](inprocserver.md)
</dt> </dl>

 

 




