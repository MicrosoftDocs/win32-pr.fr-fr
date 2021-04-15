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
# <a name="incremental-serialization"></a><span data-ttu-id="a5431-103">Sérialisation incrémentielle</span><span class="sxs-lookup"><span data-stu-id="a5431-103">Incremental Serialization</span></span>

<span data-ttu-id="a5431-104">Lorsque vous utilisez la sérialisation de style incrémentiel, vous fournissez trois routines pour manipuler la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a5431-104">When using the incremental style serialization, you supply three routines to manipulate the buffer.</span></span> <span data-ttu-id="a5431-105">Ces routines sont les suivantes : Alloc, Read et Write.</span><span class="sxs-lookup"><span data-stu-id="a5431-105">These routines are: Alloc, Read, and Write.</span></span> <span data-ttu-id="a5431-106">La routine Alloc alloue une mémoire tampon de la taille requise.</span><span class="sxs-lookup"><span data-stu-id="a5431-106">The Alloc routine allocates a buffer of the required size.</span></span> <span data-ttu-id="a5431-107">La routine d’écriture écrit les données dans la mémoire tampon, et la routine de lecture récupère une mémoire tampon qui contient des données marshalées.</span><span class="sxs-lookup"><span data-stu-id="a5431-107">The Write routine writes the data into the buffer, and the Read routine retrieves a buffer that contains marshaled data.</span></span> <span data-ttu-id="a5431-108">Un seul appel de sérialisation peut effectuer plusieurs appels à ces routines.</span><span class="sxs-lookup"><span data-stu-id="a5431-108">A single serialization call can make several calls to these routines.</span></span>

<span data-ttu-id="a5431-109">Le style incrémentiel de la sérialisation utilise les routines suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5431-109">The incremental style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="a5431-110">**MesEncodeIncrementalHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="a5431-110">**MesEncodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [<span data-ttu-id="a5431-111">**MesDecodeIncrementalHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="a5431-111">**MesDecodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [<span data-ttu-id="a5431-112">**MesIncrementalHandleReset**</span><span class="sxs-lookup"><span data-stu-id="a5431-112">**MesIncrementalHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [<span data-ttu-id="a5431-113">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="a5431-113">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="a5431-114">Les prototypes des fonctions Alloc, Read et Write que vous devez fournir sont illustrés ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a5431-114">The prototypes for the Alloc, Read, and Write functions that you must provide are shown below:</span></span>

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

<span data-ttu-id="a5431-115">L’entrée d’État un paramètre pour les trois fonctions est le pointeur défini par l’application qui a été associé au descripteur des services d’encodage.</span><span class="sxs-lookup"><span data-stu-id="a5431-115">The State input a parameter for all three functions is the application-defined pointer that was associated with the encoding services handle.</span></span> <span data-ttu-id="a5431-116">L’application peut utiliser ce pointeur pour accéder à la structure contenant des informations spécifiques à l’application, telles qu’un handle de fichier ou un pointeur de flux.</span><span class="sxs-lookup"><span data-stu-id="a5431-116">The application can use this pointer to access the structure containing application-specific information, such as a file handle or stream pointer.</span></span> <span data-ttu-id="a5431-117">Notez que les stubs ne modifient pas le pointeur d’État autre que pour le passer aux fonctions Alloc, Read et Write.</span><span class="sxs-lookup"><span data-stu-id="a5431-117">Note that the stubs do not modify the State pointer other than to pass it to the Alloc, Read, and Write functions.</span></span> <span data-ttu-id="a5431-118">Lors de l’encodage, Alloc est appelé pour obtenir une mémoire tampon dans laquelle les données sont sérialisées.</span><span class="sxs-lookup"><span data-stu-id="a5431-118">During encoding, Alloc is called to obtain a buffer into which the data is serialized.</span></span> <span data-ttu-id="a5431-119">Ensuite, l’appel d’écriture est appelé pour permettre à l’application de contrôler le moment et l’emplacement de stockage des données sérialisées.</span><span class="sxs-lookup"><span data-stu-id="a5431-119">Then, Write is called to enable the application to control when and where the serialized data is stored.</span></span> <span data-ttu-id="a5431-120">Pendant le décodage, la lecture est appelée pour retourner le nombre d’octets demandé de données sérialisées à partir duquel l’application l’a stocké.</span><span class="sxs-lookup"><span data-stu-id="a5431-120">During decoding, Read is called to return the requested number of bytes of serialized data from where the application stored it.</span></span>

<span data-ttu-id="a5431-121">Une fonctionnalité importante du style incrémentiel est que la poignée conserve le pointeur d’État pour vous.</span><span class="sxs-lookup"><span data-stu-id="a5431-121">An important feature of the incremental style is that the handle keeps the state pointer for you.</span></span> <span data-ttu-id="a5431-122">Ce pointeur gère l’État et n’est jamais touché par les fonctions RPC, sauf lors du passage du pointeur à la fonction Alloc, Write ou Read.</span><span class="sxs-lookup"><span data-stu-id="a5431-122">This pointer maintains the state and is never touched by the RPC functions, except when passing the pointer to Alloc, Write, or Read function.</span></span> <span data-ttu-id="a5431-123">Le handle gère également un état interne qui permet d’encoder et de décoder plusieurs instances de type dans la même mémoire tampon en ajoutant le remplissage requis pour l’alignement.</span><span class="sxs-lookup"><span data-stu-id="a5431-123">The handle also maintains an internal state that makes it possible to encode and decode several type instances to the same buffer by adding padding as needed for alignment.</span></span> <span data-ttu-id="a5431-124">La fonction [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) réinitialise un handle à son état initial pour permettre la lecture ou l’écriture à partir du début de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a5431-124">The [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) function resets a handle to its initial state to enable reading or writing from the beginning of the buffer.</span></span>

<span data-ttu-id="a5431-125">Les fonctions Alloc et Write, ainsi qu’un pointeur défini par l’application, sont associées à un handle Encoding-services par un appel à la fonction [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) .</span><span class="sxs-lookup"><span data-stu-id="a5431-125">The Alloc and Write functions, along with an application-defined pointer, are associated with an encoding-services handle by a call to the [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) function.</span></span> <span data-ttu-id="a5431-126">**MesEncodeIncrementalHandleCreate** alloue la mémoire nécessaire pour le handle, puis l’initialise.</span><span class="sxs-lookup"><span data-stu-id="a5431-126">**MesEncodeIncrementalHandleCreate** allocates the memory needed for the handle and then initializes it.</span></span>

<span data-ttu-id="a5431-127">L’application peut appeler [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) pour créer un descripteur de décodage, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) pour réinitialiser le handle ou [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) pour libérer la mémoire du handle.</span><span class="sxs-lookup"><span data-stu-id="a5431-127">The application can call [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) to create a decoding handle, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) to reinitialize the handle, or [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="a5431-128">La fonction Read, avec un paramètre défini par l’application, est associée à un handle de décodage par un appel à la routine **MesDecodeIncrementalHandleCreate** .</span><span class="sxs-lookup"><span data-stu-id="a5431-128">The Read function, along with an application-defined parameter, is associated with a decoding handle by a call to the **MesDecodeIncrementalHandleCreate** routine.</span></span> <span data-ttu-id="a5431-129">La fonction crée le handle et l’initialise.</span><span class="sxs-lookup"><span data-stu-id="a5431-129">The function creates the handle and initializes it.</span></span>

<span data-ttu-id="a5431-130">Les paramètres UserState, Alloc, Write et Read de [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) peuvent avoir la **valeur null** pour indiquer qu’aucune modification n’est apportée.</span><span class="sxs-lookup"><span data-stu-id="a5431-130">The UserState, Alloc, Write, and Read parameters of [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) can be **NULL** to indicate no change.</span></span>

 

 




