---
title: Développement de serveurs à l’aide de handles de contexte
description: Du point de vue du développement de programme serveur, un handle de contexte est un pointeur non typé. Les programmes serveur initialisent les handles de contexte en les faisant pointer vers des données en mémoire ou sur une autre forme de stockage (par exemple, des fichiers sur des disques).
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f743a4a6aa4a2aa7b6987bb54dc56e55cffbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029654"
---
# <a name="server-development-using-context-handles"></a><span data-ttu-id="cd47c-104">Développement de serveurs à l’aide de handles de contexte</span><span class="sxs-lookup"><span data-stu-id="cd47c-104">Server Development Using Context Handles</span></span>

<span data-ttu-id="cd47c-105">Du point de vue du développement de programme serveur, un handle de contexte est un pointeur non typé.</span><span class="sxs-lookup"><span data-stu-id="cd47c-105">From the perspective of server program development, a context handle is an untyped pointer.</span></span> <span data-ttu-id="cd47c-106">Les programmes serveur initialisent les handles de contexte en les faisant pointer vers des données en mémoire ou sur une autre forme de stockage (par exemple, des fichiers sur des disques).</span><span class="sxs-lookup"><span data-stu-id="cd47c-106">Server programs initialize context handles by pointing them at data in memory or on some other form of storage (such as files on disks).</span></span>

<span data-ttu-id="cd47c-107">Par exemple, supposons qu’un client utilise un handle de contexte pour demander une série de mises à jour à un enregistrement dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="cd47c-107">For instance, suppose that a client uses a context handle to request a series of updates to a record in a database.</span></span> <span data-ttu-id="cd47c-108">Le client appelle une procédure distante sur le serveur et lui transmet une clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="cd47c-108">The client calls a remote procedure on the server and passes it a search key.</span></span> <span data-ttu-id="cd47c-109">Le programme serveur recherche la clé de recherche dans la base de données et obtient le numéro d’enregistrement entier de l’enregistrement correspondant.</span><span class="sxs-lookup"><span data-stu-id="cd47c-109">The server program searches the database for the search key and obtains the integer record number of the matching record.</span></span> <span data-ttu-id="cd47c-110">Le serveur peut ensuite pointer un pointeur vers void à un emplacement de mémoire contenant le numéro d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cd47c-110">The server can then point a pointer to void at a memory location containing the record number.</span></span> <span data-ttu-id="cd47c-111">Lorsqu’elle retourne, la procédure distante doit retourner le pointeur en tant que handle de contexte par le biais de sa valeur de retour ou de sa liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="cd47c-111">When it returns, the remote procedure would need to return the pointer as a context handle through its return value or its parameter list.</span></span> <span data-ttu-id="cd47c-112">Le client doit passer le pointeur au serveur chaque fois qu’il appelle des procédures distantes pour mettre à jour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cd47c-112">The client would need to pass the pointer to the server each time it called remote procedures to update the record.</span></span> <span data-ttu-id="cd47c-113">Au cours de chacune de ces opérations de mise à jour, le serveur effectue un cast du pointeur void en pointeur vers un entier.</span><span class="sxs-lookup"><span data-stu-id="cd47c-113">During each of these update operations, the server would cast the void pointer to be a pointer to an integer.</span></span>

<span data-ttu-id="cd47c-114">Une fois que le programme serveur a fait pointer le handle de contexte au niveau des données de contexte, le handle est considéré comme ouvert.</span><span class="sxs-lookup"><span data-stu-id="cd47c-114">After the server program points the context handle at context data, the handle is considered opened.</span></span> <span data-ttu-id="cd47c-115">Les handles contenant une valeur **null** sont fermés.</span><span class="sxs-lookup"><span data-stu-id="cd47c-115">Handles containing a **NULL** value are closed.</span></span> <span data-ttu-id="cd47c-116">Le serveur maintient un handle de contexte ouvert jusqu’à ce que le client appelle une procédure distante qui le ferme.</span><span class="sxs-lookup"><span data-stu-id="cd47c-116">The server maintains an opened context handle until the client calls a remote procedure that closes it.</span></span> <span data-ttu-id="cd47c-117">Si la session cliente se termine alors que le descripteur est ouvert, le runtime RPC appelle la routine d’exécution de serveur pour libérer le handle.</span><span class="sxs-lookup"><span data-stu-id="cd47c-117">If the client session terminates while the handle is open, the RPC run time calls the server run-down routine to free the handle.</span></span>

<span data-ttu-id="cd47c-118">Le fragment de code suivant montre comment un serveur peut implémenter un handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="cd47c-118">The following code fragment demonstrates how a server might implement a context handle.</span></span> <span data-ttu-id="cd47c-119">Dans cet exemple, le serveur gère un fichier de données écrit par le client à l’aide de procédures distantes.</span><span class="sxs-lookup"><span data-stu-id="cd47c-119">In this example, the server maintains a data file that the client writes to using remote procedures.</span></span> <span data-ttu-id="cd47c-120">Les informations de contexte sont un handle de fichier qui effectue le suivi de l’emplacement actuel dans le fichier où le serveur écrira les données.</span><span class="sxs-lookup"><span data-stu-id="cd47c-120">The context information is a file handle that keeps track of the current location in the file where the server will write data.</span></span> <span data-ttu-id="cd47c-121">Le descripteur de fichier est empaqueté en tant que handle de contexte dans la liste de paramètres pour les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="cd47c-121">The file handle is packaged as a context handle in the parameter list to remote procedure calls.</span></span> <span data-ttu-id="cd47c-122">Une structure contient le nom de fichier et le descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="cd47c-122">A structure contains the file name and the file handle.</span></span> <span data-ttu-id="cd47c-123">La définition d’interface pour cet exemple est indiquée dans [développement d’interface à l’aide de handles de contexte](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="cd47c-123">The interface definition for this example is shown in [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span>


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



<span data-ttu-id="cd47c-124">La fonction RemoteOpen ouvre un fichier sur le serveur :</span><span class="sxs-lookup"><span data-stu-id="cd47c-124">The function RemoteOpen opens a file on the server:</span></span>


```C++
short RemoteOpen(
    PPCONTEXT_HANDLE_TYPE pphContext,
    unsigned char *pszFileName)
{
    FILE               *hFile;
    FILE_CONTEXT_TYPE  *pFileContext;
 
    if ((hFile = fopen(pszFileName, "r")) == NULL) 
    {
        *pphContext = (PCONTEXT_HANDLE_TYPE) NULL;
        return(-1);
    }
    else 
    {
        pFileContext = (FILE_CONTEXT_TYPE *) 
                       MIDL_user_allocate(sizeof(FILE_CONTEXT_TYPE));
        pFileContext->hFile = hFile;
        // check if pszFileName is longer than 256 and if yes, return
        // an error
        strcpy_s(pFileContext->achFile, srlen(pszFileName), pszFileName);
        *pphContext = (PCONTEXT_HANDLE_TYPE) pFileContext;
        return(0);
    }
}
```



<span data-ttu-id="cd47c-125">La fonction RemoteRead lit un fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="cd47c-125">The function RemoteRead reads a file on the server.</span></span>


```C++
short RemoteRead(
    PCONTEXT_HANDLE_TYPE phContext, 
    unsigned char *pbBuf, 
    short *pcbBuf) 
{ 
    FILE_CONTEXT_TYPE *pFileContext; 
    printf("in RemoteRead\n"); 
    pFileContext = (FILE_CONTEXT_TYPE *) phContext; 
    *pcbBuf = (short) fread(pbBuf, sizeof(char), 
                            BUFSIZE, 
                            pFileContext->hFile); 
    return(*pcbBuf); 
}
```



<span data-ttu-id="cd47c-126">La fonction RemoteClose ferme un fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="cd47c-126">The function RemoteClose closes a file on the server.</span></span> <span data-ttu-id="cd47c-127">Notez que l’application serveur doit assigner la **valeur null** au handle de contexte dans le cadre de la fonction de fermeture.</span><span class="sxs-lookup"><span data-stu-id="cd47c-127">Note that the server application has to assign **NULL** to the context handle as part of the close function.</span></span> <span data-ttu-id="cd47c-128">Cela communique avec le stub serveur et la bibliothèque Runtime RPC que le handle de contexte a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="cd47c-128">This communicates to the server stub and the RPC run-time library that the context handle has been deleted.</span></span> <span data-ttu-id="cd47c-129">Dans le cas contraire, la connexion est maintenue ouverte et une exécution de contexte est finalement effectuée.</span><span class="sxs-lookup"><span data-stu-id="cd47c-129">Otherwise, the connection will be kept open and eventually a context run-down will occur.</span></span>


```C++
void RemoteClose(PPCONTEXT_HANDLE_TYPE pphContext)
{
    FILE_CONTEXT_TYPE *pFileContext;
 
    if (*pphContext == NULL)
    {
        //Log error, client tried to close a NULL handle.
        return;
    }
    pFileContext = (FILE_CONTEXT_TYPE *)*pphContext;
    printf("File %s closed.\n", pFileContext->achFile);
    fclose(pFileConext->hFile);
    MIDL_user_free(pFileContext);
 
    // This tells the run-time, when it is marshalling the out 
    // parameters, that the context handle has been closed normally.
    *pphContext = NULL;
}
```



> [!Note]  
> <span data-ttu-id="cd47c-130">Bien qu’il soit attendu, le client passe un handle de contexte valide à un appel avec \[ in, out \] Attributes, RPC ne rejette pas les handles de contexte **null** pour cette combinaison d’attributs directionnels.</span><span class="sxs-lookup"><span data-stu-id="cd47c-130">While it is expected the client passes a valid context handle to a call with \[in, out\] directional attributes, RPC does not reject **NULL** context handles for this combination of directional attributes.</span></span> <span data-ttu-id="cd47c-131">Le descripteur de contexte **null** est passé au serveur en tant que pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="cd47c-131">The **NULL** context handle is passed to the server as a **NULL** pointer.</span></span> <span data-ttu-id="cd47c-132">Le code serveur pour les appels contenant un \[ handle de contexte in, out \] doit être écrit pour éviter une violation d’accès lors de la réception d’un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="cd47c-132">The server code for calls containing an \[in, out\] context handle should be written to avoid an access violation when a **NULL** pointer is received.</span></span>

 

 

 




