---
description: Les objets nommés offrent un moyen simple pour les processus de partager des handles d’objets.
ms.assetid: 00a00227-45fc-49a1-8ff5-aeccb172d16a
title: Noms d'objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee746150a41f335a4073cb4b5ba282d17ad706f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541887"
---
# <a name="object-names"></a>Noms d'objets

Les objets nommés offrent un moyen simple pour les processus de partager des handles d’objets. Une fois qu’un processus a créé un objet nommé Event, mutex, Semaphore ou Timer, les autres processus peuvent utiliser le nom pour appeler la fonction appropriée ( [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)ou [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw)) afin d’ouvrir un handle vers l’objet. La comparaison des noms respecte la casse.

Les noms de l’événement, du sémaphore, du mutex, du minuteur d’attente, du mappage de fichiers et des objets de travail partagent le même espace de noms. Si vous essayez de créer un objet à l’aide d’un nom qui est utilisé par un objet d’un autre type, la fonction échoue et [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ handle non valide**. Par conséquent, lors de la création d’objets nommés, utilisez des noms uniques et veillez à vérifier les valeurs de retour de fonction pour les erreurs de nom en double.

Si vous essayez de créer un objet à l’aide d’un nom qui est utilisé par un objet du même type, la fonction est exécutée, retourne un handle à l’objet existant et [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ déjà \_** existante. Par exemple, si le nom spécifié dans un appel à la fonction [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) correspond au nom d’un objet mutex existant, la fonction retourne un handle vers l’objet existant. Dans ce cas, l’appel à **CreateMutex** est équivalent à un appel à la fonction [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) . Le fait d’avoir plusieurs processus utilisant **CreateMutex** pour le même Mutex revient donc à avoir un processus qui appelle **CreateMutex** alors que les autres processus appellent **OpenMutex**, à ceci près qu’il élimine la nécessité de s’assurer que le processus de création est démarré en premier. Toutefois, lors de l’utilisation de cette technique pour les objets mutex, aucun des processus appelant ne doit demander immédiatement la propriété du mutex. Si plusieurs processus demandent la propriété immédiate, il peut être difficile de prédire quel processus obtient réellement la propriété initiale.

Un environnement de services Terminal Server dispose d’un espace de noms global pour les événements, les sémaphores, les mutex, les minuteries, les objets de mappage de fichiers et les objets de traitement. En outre, chaque session cliente des services Terminal Server a son propre espace de noms distinct pour ces objets. Les processus clients des services Terminal Server peuvent utiliser des noms d’objets avec un \\ préfixe « global » ou « local \\ » pour créer explicitement un objet dans l’espace de noms global ou de session. Pour plus d’informations, consultez [espaces de noms d’objets noyau](../termserv/kernel-object-namespaces.md). Le changement rapide d’utilisateur est implémenté à l’aide de sessions des services Terminal Server (chaque utilisateur se connecte à une autre session). Les noms d’objets de noyau doivent respecter les instructions indiquées pour les services Terminal Server afin que les applications puissent prendre en charge plusieurs utilisateurs.

Les objets de synchronisation peuvent être créés dans un espace de noms privé. Pour plus d’informations, consultez [espaces de noms d’objets](object-namespaces.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’objets nommés](using-named-objects.md)
</dt> </dl>

 

 
