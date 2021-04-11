---
title: Utilisation des services de sérialisation
description: MIDL génère un stub de sérialisation pour la procédure avec les attributs \ encode \ et \ Decode \.
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- Appel de procédure distante RPC, tâches, utilisation des services de sérialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317156a2da954e001b687cca12eb0c6df23ef4ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031812"
---
# <a name="using-serialization-services"></a><span data-ttu-id="7999d-104">Utilisation des services de sérialisation</span><span class="sxs-lookup"><span data-stu-id="7999d-104">Using Serialization Services</span></span>

<span data-ttu-id="7999d-105">MIDL génère un stub de sérialisation pour la procédure avec les attributs \[ [**Encoder**](/windows/desktop/Midl/encode) \] et \[ [**décoder**](/windows/desktop/Midl/decode) \] .</span><span class="sxs-lookup"><span data-stu-id="7999d-105">MIDL generates a serialization stub for the procedure with the attributes \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\].</span></span> <span data-ttu-id="7999d-106">Lorsque vous appelez cette routine, vous exécutez un appel de sérialisation au lieu d’un appel distant.</span><span class="sxs-lookup"><span data-stu-id="7999d-106">When you call this routine, you execute a serialization call instead of a remote call.</span></span> <span data-ttu-id="7999d-107">Les arguments de procédure sont marshalés ou démarshalés à partir d’une mémoire tampon de la manière habituelle.</span><span class="sxs-lookup"><span data-stu-id="7999d-107">The procedure arguments are marshaled to or unmarshaled from a buffer in the usual way.</span></span> <span data-ttu-id="7999d-108">Vous avez ensuite le contrôle total des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="7999d-108">You then have complete control of the buffers.</span></span>

<span data-ttu-id="7999d-109">En revanche, lorsque votre programme effectue une sérialisation de type (un type est étiqueté avec des attributs de sérialisation), MIDL génère des routines pour dimensionner, encoder et décoder les objets de ce type.</span><span class="sxs-lookup"><span data-stu-id="7999d-109">In contrast, when your program performs type serialization (a type is labeled with serialization attributes), MIDL generates routines to size, encode, and decode objects of that type.</span></span> <span data-ttu-id="7999d-110">Pour sérialiser des données, vous devez appeler ces routines de la manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="7999d-110">To serialize data, you must call these routines in the appropriate way.</span></span> <span data-ttu-id="7999d-111">La sérialisation de type est une extension Microsoft et, par conséquent, n’est pas disponible quand vous compilez en mode compatible DCE ([**/OSF**](/windows/desktop/Midl/-osf)).</span><span class="sxs-lookup"><span data-stu-id="7999d-111">Type serialization is a Microsoft extension and, as such, is not available when you compile in DCE-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="7999d-112">En utilisant les \[ attributs [**encode**](/windows/desktop/Midl/encode) \] et \[ [**Decode**](/windows/desktop/Midl/decode) \] comme attributs d’interface, RPC applique l’encodage à tous les types et routines définis dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="7999d-112">By using the \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\] attributes as interface attributes, RPC applies encoding to all the types and routines defined in the IDL file.</span></span>

<span data-ttu-id="7999d-113">Vous devez fournir des mémoires tampons correctement alignées lors de l’utilisation des services de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="7999d-113">You must supply adequately aligned buffers when using serialization services.</span></span> <span data-ttu-id="7999d-114">Le début de la mémoire tampon doit être aligné sur une adresse qui est un multiple de 8, ou aligné sur 8 octets.</span><span class="sxs-lookup"><span data-stu-id="7999d-114">The beginning of the buffer must be aligned at an address that is a multiple of 8, or 8-byte aligned.</span></span> <span data-ttu-id="7999d-115">Pour la sérialisation de procédure, chaque appel de procédure doit marshaler dans ou démarshaler une position de mémoire tampon qui est alignée sur 8 octets.</span><span class="sxs-lookup"><span data-stu-id="7999d-115">For procedure serialization, each procedure call must marshal into or unmarshal from a buffer position that is 8-byte aligned.</span></span> <span data-ttu-id="7999d-116">Pour la sérialisation de type, le dimensionnement, l’encodage et le décodage doivent commencer à une position qui est alignée sur 8 octets.</span><span class="sxs-lookup"><span data-stu-id="7999d-116">For type serialization, sizing, encoding, and decoding must start at a position that is 8-byte aligned.</span></span>

<span data-ttu-id="7999d-117">L’une des méthodes pour votre application de s’assurer que ses mémoires tampons sont alignées consiste à écrire la fonction [**\_ \_ allocate de l’utilisateur MIDL**](/windows/desktop/Midl/midl-user-allocate-1) de manière à créer des mémoires tampons alignées.</span><span class="sxs-lookup"><span data-stu-id="7999d-117">One way for your application to ensure that its buffers are aligned is to write the [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) function such that it creates aligned buffers.</span></span> <span data-ttu-id="7999d-118">L’exemple de code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="7999d-118">The following code sample demonstrates how this can be done.</span></span>


```C++
#include <windows.h>

#define ALIGN_TO8(p)   (char *)((unsigned long)((char *)p + 7) & ~7)

void __RPC_FAR *__RPC_USER  MIDL_user_allocate(size_t sizeInBytes)
{
    unsigned char *pcAllocated;
    unsigned char *pcUserPtr;

    pcAllocated = (unsigned char *) malloc( sizeInBytes + 15 );
    pcUserPtr =  ALIGN_TO8( pcAllocated );
    if ( pcUserPtr == pcAllocated )
        pcUserPtr = pcAllocated + 8;

    *(pcUserPtr - 1) = pcUserPtr - pcAllocated;

    return( pcUserPtr );
}
```



<span data-ttu-id="7999d-119">L’exemple suivant illustre la fonction de l' [**\_ \_ utilisateur MIDL**](/windows/desktop/Midl/midl-user-free-1) correspondante.</span><span class="sxs-lookup"><span data-stu-id="7999d-119">The following example shows the corresponding [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) function.</span></span>


```C++
void __RPC_USER  MIDL_user_free(void __RPC_FAR *f)
{
    unsigned char * pcAllocated;
    unsigned char * pcUserPtr;

    pcUserPtr = (unsigned char *) f;
    pcAllocated = pcUserPtr - *(pcUserPtr - 1);

    free( pcAllocated );
}
```



 

 