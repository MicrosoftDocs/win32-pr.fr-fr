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
# <a name="using-serialization-services"></a>Utilisation des services de sérialisation

MIDL génère un stub de sérialisation pour la procédure avec les attributs \[ [**Encoder**](/windows/desktop/Midl/encode) \] et \[ [**décoder**](/windows/desktop/Midl/decode) \] . Lorsque vous appelez cette routine, vous exécutez un appel de sérialisation au lieu d’un appel distant. Les arguments de procédure sont marshalés ou démarshalés à partir d’une mémoire tampon de la manière habituelle. Vous avez ensuite le contrôle total des mémoires tampons.

En revanche, lorsque votre programme effectue une sérialisation de type (un type est étiqueté avec des attributs de sérialisation), MIDL génère des routines pour dimensionner, encoder et décoder les objets de ce type. Pour sérialiser des données, vous devez appeler ces routines de la manière appropriée. La sérialisation de type est une extension Microsoft et, par conséquent, n’est pas disponible quand vous compilez en mode compatible DCE ([**/OSF**](/windows/desktop/Midl/-osf)). En utilisant les \[ attributs [**encode**](/windows/desktop/Midl/encode) \] et \[ [**Decode**](/windows/desktop/Midl/decode) \] comme attributs d’interface, RPC applique l’encodage à tous les types et routines définis dans le fichier IDL.

Vous devez fournir des mémoires tampons correctement alignées lors de l’utilisation des services de sérialisation. Le début de la mémoire tampon doit être aligné sur une adresse qui est un multiple de 8, ou aligné sur 8 octets. Pour la sérialisation de procédure, chaque appel de procédure doit marshaler dans ou démarshaler une position de mémoire tampon qui est alignée sur 8 octets. Pour la sérialisation de type, le dimensionnement, l’encodage et le décodage doivent commencer à une position qui est alignée sur 8 octets.

L’une des méthodes pour votre application de s’assurer que ses mémoires tampons sont alignées consiste à écrire la fonction [**\_ \_ allocate de l’utilisateur MIDL**](/windows/desktop/Midl/midl-user-allocate-1) de manière à créer des mémoires tampons alignées. L’exemple de code suivant montre comment procéder.


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



L’exemple suivant illustre la fonction de l' [**\_ \_ utilisateur MIDL**](/windows/desktop/Midl/midl-user-free-1) correspondante.


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



 

 