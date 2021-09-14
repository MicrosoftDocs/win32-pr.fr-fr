---
description: Les fonctions globales et locales sont prises en charge pour le portage à partir de code 16 bits ou pour la gestion de la compatibilité du code source avec les Windows 16 bits.
ms.assetid: 97707ce7-4c65-4d0e-ba69-47fdaee73a9b
title: Fonctions globales et locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf356647f92f0e7d82e914a91020c438363ff082
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094138"
---
# <a name="global-and-local-functions"></a>Fonctions globales et locales

Les fonctions globales et locales sont prises en charge pour le portage à partir de code 16 bits ou pour la gestion de la compatibilité du code source avec les Windows 16 bits. à partir de la Windows 32 bits, les fonctions globales et locales sont implémentées en tant que fonctions wrapper qui appellent les [fonctions de tas](heap-functions.md) correspondantes à l’aide d’un handle vers le tas par défaut du processus. Par conséquent, les fonctions globales et locales ont une surcharge supérieure à celle des autres fonctions de gestion de la mémoire.

Les [fonctions de tas](heap-functions.md) offrent plus de fonctionnalités et de contrôle que les fonctions globales et locales. Les nouvelles applications doivent utiliser les fonctions de tas, sauf si la documentation stipule spécifiquement qu’une fonction globale ou locale doit être utilisée. par exemple, certaines fonctions Windows allouez de la mémoire qui doit être libérée avec [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree), et les fonctions globales sont toujours utilisées avec échange dynamique de données (DDE), les fonctions du presse-papiers et les objets de données OLE. Pour obtenir la liste complète des fonctions locales et globales, consultez le tableau dans [fonctions de gestion](memory-management-functions.md)de la mémoire.

la gestion de la mémoire Windows ne fournit pas de segment de mémoire local et de tas global distincts, comme le fait la Windows 16 bits. Par conséquent, les familles de fonctions globales et locales sont équivalentes et le choix entre elles est une question de préférence personnelle. Notez que le changement d’un modèle de mémoire segmentée 16 bits à un modèle de mémoire virtuelle 32 bits a rendu les fonctions globales et locales associées et leurs options inutiles ou non significatives. Par exemple, il n’y a plus de pointeurs near et Far, car les allocations locales et globales retournent des adresses virtuelles de 32 bits.

Les objets mémoire alloués par [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) et [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) se trouvent dans des pages privées et validées avec un accès en lecture/écriture qui ne sont pas accessibles par d’autres processus. La mémoire allouée à l’aide de **GlobalAlloc** avec **GMEM \_ DDESHARE** n’est pas en fait partagée globalement, car elle est en Windows 16 bits. Cette valeur n’a aucun effet et n’est disponible que pour la compatibilité. Les applications nécessitant une mémoire partagée à d’autres fins doivent utiliser des objets de mappage de fichiers. Plusieurs processus peuvent mapper une vue du même objet de mappage de fichiers pour fournir la mémoire partagée nommée. Pour plus d’informations, consultez [mappage de fichiers](file-mapping.md).

Les allocations de mémoire sont limitées uniquement par la mémoire physique disponible, y compris le stockage dans le fichier d’échange sur le disque. Lorsque vous allouez de la mémoire fixe, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) et [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) retournent un pointeur que le processus appelant peut utiliser immédiatement pour accéder à la mémoire. Lorsque vous allouez de la mémoire mobile, la valeur de retour est un handle. Pour obtenir un pointeur vers un objet mémoire mobile, utilisez les fonctions [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock) et [**LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) .

La taille réelle de la mémoire allouée peut être supérieure à la taille demandée. Pour déterminer le nombre réel d’octets alloués, utilisez la fonction [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize) ou [**LocalSize**](/windows/desktop/api/WinBase/nf-winbase-localsize) . Si la quantité allouée est supérieure à la quantité demandée, le processus peut utiliser la totalité du montant.

Les fonctions [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc) et [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) modifient la taille ou les attributs d’un objet mémoire alloué par [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) et [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc). La taille peut augmenter ou diminuer.

Les fonctions [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree) et [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) libèrent la mémoire allouée par [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)ou [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc). Pour ignorer l’objet mémoire spécifié sans invalider le handle, utilisez la fonction [**GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) ou [**LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) . Le descripteur peut être utilisé ultérieurement par **GlobalReAlloc** ou **LocalReAlloc** pour allouer un nouveau bloc de mémoire associé au même handle.

Pour retourner des informations sur un objet mémoire spécifié, utilisez la fonction [**GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags) ou [**LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) . Les informations incluent le nombre de verrous de l’objet et indiquent si l’objet est supprimé ou a déjà été ignoré. Pour retourner un handle à l’objet mémoire associé à un pointeur spécifié, utilisez la fonction [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) ou [**LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comparaison des méthodes d’allocation de mémoire](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 
