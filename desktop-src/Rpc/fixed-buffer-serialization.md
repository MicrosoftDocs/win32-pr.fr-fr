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
# <a name="fixed-buffer-serialization"></a><span data-ttu-id="5c2b2-103">Sérialisation de mémoire tampon fixe</span><span class="sxs-lookup"><span data-stu-id="5c2b2-103">Fixed Buffer Serialization</span></span>

<span data-ttu-id="5c2b2-104">Quand vous utilisez le style de mémoire tampon fixe, spécifiez une mémoire tampon suffisamment grande pour prendre en charge les opérations d’encodage (marshaling) effectuées avec le descripteur.</span><span class="sxs-lookup"><span data-stu-id="5c2b2-104">When using the fixed buffer style, specify a buffer that is large enough to accommodate the encoding (marshalling) operations performed with the handle.</span></span> <span data-ttu-id="5c2b2-105">Lors du démarshaling, vous fournissez la mémoire tampon qui contient toutes les données à décoder.</span><span class="sxs-lookup"><span data-stu-id="5c2b2-105">When unmarshaling, you provide the buffer that contains all of the data to decode.</span></span>

<span data-ttu-id="5c2b2-106">Le style de mémoire tampon fixe de la sérialisation utilise les routines suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c2b2-106">The fixed buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="5c2b2-107">**MesEncodeFixedBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="5c2b2-107">**MesEncodeFixedBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [<span data-ttu-id="5c2b2-108">**MesDecodeBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="5c2b2-108">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="5c2b2-109">**MesBufferHandleReset**</span><span class="sxs-lookup"><span data-stu-id="5c2b2-109">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="5c2b2-110">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="5c2b2-110">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="5c2b2-111">La fonction **MesEncodeFixedBufferHandleCreate** alloue la mémoire nécessaire pour le handle d’encodage, puis l’initialise.</span><span class="sxs-lookup"><span data-stu-id="5c2b2-111">The **MesEncodeFixedBufferHandleCreate** function allocates the memory needed for the encoding handle, and then initializes it.</span></span> <span data-ttu-id="5c2b2-112">L’application peut appeler [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) pour réinitialiser le descripteur, ou elle peut appeler [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) pour libérer la mémoire du handle.</span><span class="sxs-lookup"><span data-stu-id="5c2b2-112">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle, or it can call [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="5c2b2-113">Pour créer un descripteur de décodage correspondant au handle de codage de style fixe, vous devez utiliser [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="5c2b2-113">To create a decoding handle corresponding to the fixed style–encoding handle, you must use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

<span data-ttu-id="5c2b2-114">L’application appelle [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) pour libérer le descripteur de tampon d’encodage ou de décodage.</span><span class="sxs-lookup"><span data-stu-id="5c2b2-114">The application calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the encoding or decoding buffer handle.</span></span>

## <a name="examples-of-fixed-buffer-encoding"></a><span data-ttu-id="5c2b2-115">Exemples d’encodage de mémoire tampon fixe</span><span class="sxs-lookup"><span data-stu-id="5c2b2-115">Examples of Fixed Buffer Encoding</span></span>

<span data-ttu-id="5c2b2-116">La section suivante fournit un exemple de la façon d’utiliser un descripteur de style de mémoire tampon fixe pour l’encodage de procédure.</span><span class="sxs-lookup"><span data-stu-id="5c2b2-116">The following section provides an example of how to use a fixed buffer style–serializing handle for procedure encoding.</span></span>

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

<span data-ttu-id="5c2b2-117">L’extrait suivant représente une partie d’une application.</span><span class="sxs-lookup"><span data-stu-id="5c2b2-117">The following excerpt represents a part of an application.</span></span>

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

<span data-ttu-id="5c2b2-118">La section suivante fournit un exemple d’utilisation d’un descripteur de style de mémoire tampon fixe pour l’encodage de type.</span><span class="sxs-lookup"><span data-stu-id="5c2b2-118">The following section provides an example of how to use a fixed buffer style–serializing handle for type encoding.</span></span>

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

<span data-ttu-id="5c2b2-119">L’extrait suivant représente les fragments d’application pertinents.</span><span class="sxs-lookup"><span data-stu-id="5c2b2-119">The following excerpt represents the relevant application fragments.</span></span>


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



 

 




