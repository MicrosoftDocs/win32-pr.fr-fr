---
title: Définition de canaux dans des fichiers IDL
description: Lorsqu’un canal est défini dans un fichier IDL, le compilateur MIDL génère une structure de contrôle de canal dont les membres sont des pointeurs vers des procédures push, pull et Alloc, ainsi qu’une variable d’État qui coordonne ces procédures.
ms.assetid: f6c282e4-3056-48c4-bd12-dfcae6d238d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115be7fc5d00458d13df102afebe9ba5b55de070
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382325"
---
# <a name="defining-pipes-in-idl-files"></a><span data-ttu-id="c59e7-103">Définition de canaux dans des fichiers IDL</span><span class="sxs-lookup"><span data-stu-id="c59e7-103">Defining Pipes in IDL Files</span></span>

<span data-ttu-id="c59e7-104">Lorsqu’un canal est défini dans un fichier IDL, le compilateur MIDL génère une structure de contrôle de canal dont les membres sont des pointeurs vers des procédures push, pull et Alloc, ainsi qu’une variable d’État qui coordonne ces procédures.</span><span class="sxs-lookup"><span data-stu-id="c59e7-104">When a pipe is defined in an IDL file, the MIDL compiler generates a pipe control structure whose members are pointers to push, pull, and alloc procedures as well as a state variable that coordinates these procedures.</span></span> <span data-ttu-id="c59e7-105">L’application cliente initialise les champs de la structure de contrôle du canal, conserve sa variable d’État et gère le transfert de données avec ses propres fonctions push, pull et Alloc.</span><span class="sxs-lookup"><span data-stu-id="c59e7-105">The client application initializes the fields in the pipe control structure, maintains its state variable, and manages the data transfer with its own push, pull, and alloc functions.</span></span> <span data-ttu-id="c59e7-106">Le code stub du client appelle ces fonctions d’application dans des boucles pendant le transfert de données.</span><span class="sxs-lookup"><span data-stu-id="c59e7-106">The client stub code calls these application functions in loops during data transfer.</span></span> <span data-ttu-id="c59e7-107">Pour un canal d’entrée, le stub client marshale les données de transfert et les transmet au stub serveur.</span><span class="sxs-lookup"><span data-stu-id="c59e7-107">For an input pipe, the client stub marshals the transfer data and transmits it to the server stub.</span></span> <span data-ttu-id="c59e7-108">Pour un canal de sortie, le stub client démarshale les données dans une mémoire tampon et transmet un pointeur vers cette mémoire tampon à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="c59e7-108">For an output pipe, the client stub unmarshals the data into a buffer and passes a pointer to that buffer back to the client application.</span></span>

<span data-ttu-id="c59e7-109">Le code stub du serveur initialise les champs de la structure de contrôle de canal à une variable d’État, ainsi que les pointeurs vers les routines push et pull.</span><span class="sxs-lookup"><span data-stu-id="c59e7-109">The server stub code initializes the fields of the pipe control structure to a state variable, as well as pointers to push and pull routines.</span></span> <span data-ttu-id="c59e7-110">Le stub serveur conserve l’État et gère son stockage privé pour les données de transfert.</span><span class="sxs-lookup"><span data-stu-id="c59e7-110">The server stub maintains the state and manages its private storage for the transfer data.</span></span> <span data-ttu-id="c59e7-111">L’application serveur appelle les routines push et push dans des boucles pendant l’appel de procédure distante lorsqu’elle reçoit et démarshale les données du stub client, ou marshale et transmet des données au stub client.</span><span class="sxs-lookup"><span data-stu-id="c59e7-111">The server application calls the pull and push routines in loops during the remote procedure call as it receives and unmarshals data from the client stub, or marshals and transmits data to the client stub.</span></span>

<span data-ttu-id="c59e7-112">L’exemple de fichier IDL suivant définit un canal de type LONG \_ , dont la taille d’élément est définie sur **long**.</span><span class="sxs-lookup"><span data-stu-id="c59e7-112">The following example IDL file defines a pipe type LONG\_PIPE, whose element size is defined as **long**.</span></span> <span data-ttu-id="c59e7-113">Elle déclare également des prototypes de fonction pour les appels de procédure distante et les appels de procédure distante et d’envoi, pour envoyer et recevoir des données, respectivement.</span><span class="sxs-lookup"><span data-stu-id="c59e7-113">It also declares function prototypes for the remote procedure calls InPipe and OutPipe, to send and receive data, respectively.</span></span> <span data-ttu-id="c59e7-114">Lorsque le compilateur MIDL traite le fichier IDL, il génère le fichier d’en-tête indiqué dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c59e7-114">When the MIDL compiler processes the IDL file, it generates the header file shown in the example.</span></span>

## <a name="example"></a><span data-ttu-id="c59e7-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="c59e7-115">Example</span></span>

``` syntax
// File: pipedemo.idl
typedef pipe long LONG_PIPE;
void InPipe( [in] LONG_PIPE pipe_data );
void OutPipe( [out] LONG_PIPE *pipe_data ); 
//end pipedemo.idl
 
// File: pipedemo.h (fragment)
// Generated by the MIDL compiler from pipedemo.idl
typedef struct pipe_LONG_PIPE
{
    void (__RPC_FAR * pull) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long esize,
        unsigned long __RPC_FAR * ecount );
    void (__RPC_FAR * push) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long ecount );
    void (__RPC_FAR * alloc) (
        char __RPC_FAR * state,
        unsigned long bsize,
        long __RPC_FAR * __RPC_FAR * buf,
        unsigned long __RPC_FAR * bcount );
    char __RPC_FAR * state;
} LONG_PIPE;
 
void InPipe( 
    /* [in] */ LONG_PIPE pipe_data);
void OutPipe( 
    /* [out] */ LONG_PIPE __RPC_FAR *pipe_data);
//end pipedemo.h
```

## <a name="related-topics"></a><span data-ttu-id="c59e7-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c59e7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c59e7-117">canal</span><span class="sxs-lookup"><span data-stu-id="c59e7-117">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="c59e7-118">**/OI**</span><span class="sxs-lookup"><span data-stu-id="c59e7-118">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 