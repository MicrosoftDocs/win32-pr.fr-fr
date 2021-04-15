---
title: Sérialisation incrémentielle
description: Lorsque vous utilisez la sérialisation de style incrémentiel, vous fournissez trois routines pour manipuler la mémoire tampon.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409f8da0881719ec9273f4dd12cc99e3d36c35a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507402"
---
# <a name="incremental-serialization"></a>Sérialisation incrémentielle

Lorsque vous utilisez la sérialisation de style incrémentiel, vous fournissez trois routines pour manipuler la mémoire tampon. Ces routines sont les suivantes : Alloc, Read et Write. La routine Alloc alloue une mémoire tampon de la taille requise. La routine d’écriture écrit les données dans la mémoire tampon, et la routine de lecture récupère une mémoire tampon qui contient des données marshalées. Un seul appel de sérialisation peut effectuer plusieurs appels à ces routines.

Le style incrémentiel de la sérialisation utilise les routines suivantes :

-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Les prototypes des fonctions Alloc, Read et Write que vous devez fournir sont illustrés ci-dessous :

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

L’entrée d’État un paramètre pour les trois fonctions est le pointeur défini par l’application qui a été associé au descripteur des services d’encodage. L’application peut utiliser ce pointeur pour accéder à la structure contenant des informations spécifiques à l’application, telles qu’un handle de fichier ou un pointeur de flux. Notez que les stubs ne modifient pas le pointeur d’État autre que pour le passer aux fonctions Alloc, Read et Write. Lors de l’encodage, Alloc est appelé pour obtenir une mémoire tampon dans laquelle les données sont sérialisées. Ensuite, l’appel d’écriture est appelé pour permettre à l’application de contrôler le moment et l’emplacement de stockage des données sérialisées. Pendant le décodage, la lecture est appelée pour retourner le nombre d’octets demandé de données sérialisées à partir duquel l’application l’a stocké.

Une fonctionnalité importante du style incrémentiel est que la poignée conserve le pointeur d’État pour vous. Ce pointeur gère l’État et n’est jamais touché par les fonctions RPC, sauf lors du passage du pointeur à la fonction Alloc, Write ou Read. Le handle gère également un état interne qui permet d’encoder et de décoder plusieurs instances de type dans la même mémoire tampon en ajoutant le remplissage requis pour l’alignement. La fonction [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) réinitialise un handle à son état initial pour permettre la lecture ou l’écriture à partir du début de la mémoire tampon.

Les fonctions Alloc et Write, ainsi qu’un pointeur défini par l’application, sont associées à un handle Encoding-services par un appel à la fonction [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) . **MesEncodeIncrementalHandleCreate** alloue la mémoire nécessaire pour le handle, puis l’initialise.

L’application peut appeler [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) pour créer un descripteur de décodage, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) pour réinitialiser le handle ou [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) pour libérer la mémoire du handle. La fonction Read, avec un paramètre défini par l’application, est associée à un handle de décodage par un appel à la routine **MesDecodeIncrementalHandleCreate** . La fonction crée le handle et l’initialise.

Les paramètres UserState, Alloc, Write et Read de [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) peuvent avoir la **valeur null** pour indiquer qu’aucune modification n’est apportée.

 

 




