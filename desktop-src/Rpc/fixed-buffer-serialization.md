---
title: Sérialisation de mémoire tampon fixe
description: Sérialisation de mémoire tampon fixe.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87e3cad0a272ccd493cf9088fedeb272f1206b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380020"
---
# <a name="fixed-buffer-serialization"></a>Sérialisation de mémoire tampon fixe

Quand vous utilisez le style de mémoire tampon fixe, spécifiez une mémoire tampon suffisamment grande pour prendre en charge les opérations d’encodage (marshaling) effectuées avec le descripteur. Lors du démarshaling, vous fournissez la mémoire tampon qui contient toutes les données à décoder.

Le style de mémoire tampon fixe de la sérialisation utilise les routines suivantes :

-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

La fonction **MesEncodeFixedBufferHandleCreate** alloue la mémoire nécessaire pour le handle d’encodage, puis l’initialise. L’application peut appeler [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) pour réinitialiser le descripteur, ou elle peut appeler [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) pour libérer la mémoire du handle. Pour créer un descripteur de décodage correspondant au handle de codage de style fixe, vous devez utiliser [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

L’application appelle [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) pour libérer le descripteur de tampon d’encodage ou de décodage.

## <a name="examples-of-fixed-buffer-encoding"></a>Exemples d’encodage de mémoire tampon fixe

La section suivante fournit un exemple de la façon d’utiliser un descripteur de style de mémoire tampon fixe pour l’encodage de procédure.

``` syntax
/*This is a fragment of the IDL file defining MooProc */

...
void __RPC_USER
MyProc( [in] handle_t Handle, [in,out] MyType * pMyObject,
        [in, out] ThisType * pThisObject);
...

/*This is an ACF file. MyProc is defined in the IDL file */

[
    explicit_handle
]
interface regress
{
    [ encode,decode ] MyProc();
}
```

L’extrait suivant représente une partie d’une application.

``` syntax
if (MesEncodeFixedBufferHandleCreate (
        Buffer, BufferSize, 
        pEncodedSize, &Handle) == RPC_S_OK)
{
    ...
    /* Manufacture a MyObject and a ThisObject */
    ...
    /* The serialization works from the beginning of the buffer because 
   the handle is in the initial state. The function MyProc does the    
   following when called with an encoding handle:
     - sizes all the parameters for marshalling,
     - marshalls into the buffer (and sets the internal state 
    appropriately) 
    */

    MyProc ( Handle, pMyObject, pThisObject );
    ...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK)
{

    /* The MooProc does the following for you when called with a decoding 
    handle:
     - unmarshalls the objects from the buffer into *pMooObject and 
       *pBarObject
*/

MyProc ( Handle, pMyObject, pThisObject);
...
MesHandleFree ( Handle );
}
```

La section suivante fournit un exemple d’utilisation d’un descripteur de style de mémoire tampon fixe pour l’encodage de type.

``` syntax
/* This is an ACF file. MyType is defined in the IDL file */

[    
    explicit_handle
]
interface regress
{
    typedef [ encode,decode ] MyType;
}
```

L’extrait suivant représente les fragments d’application pertinents.


```C++
if (MesEncodeFixedBufferHandleCreate (Buffer, BufferSize, 
    pEncodedSize, &Handle) == RPC_S_OK)
{
    //...
    /* Manufacture a MyObject and a pMyObject */
    //...
    MyType_Encode ( Handle, pMyObject );
    //...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK )
{
    MooType_Decode (Handle, pMooObject);
    //...
    MesHandleFree ( Handle );
}
```



 

 




