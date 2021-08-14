---
title: Développement de serveurs à l’aide de handles de contexte
description: Du point de vue du développement de programme serveur, un handle de contexte est un pointeur non typé. Les programmes serveur initialisent les handles de contexte en les faisant pointer vers des données en mémoire ou sur une autre forme de stockage (par exemple, des fichiers sur des disques).
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db05441f7314fba628d1ec07db5f99266c595c84e672ada976b38f7576ab5d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925335"
---
# <a name="server-development-using-context-handles"></a>Développement de serveurs à l’aide de handles de contexte

Du point de vue du développement de programme serveur, un handle de contexte est un pointeur non typé. Les programmes serveur initialisent les handles de contexte en les faisant pointer vers des données en mémoire ou sur une autre forme de stockage (par exemple, des fichiers sur des disques).

Par exemple, supposons qu’un client utilise un handle de contexte pour demander une série de mises à jour à un enregistrement dans une base de données. Le client appelle une procédure distante sur le serveur et lui transmet une clé de recherche. Le programme serveur recherche la clé de recherche dans la base de données et obtient le numéro d’enregistrement entier de l’enregistrement correspondant. Le serveur peut ensuite pointer un pointeur vers void à un emplacement de mémoire contenant le numéro d’enregistrement. Lorsqu’elle retourne, la procédure distante doit retourner le pointeur en tant que handle de contexte par le biais de sa valeur de retour ou de sa liste de paramètres. Le client doit passer le pointeur au serveur chaque fois qu’il appelle des procédures distantes pour mettre à jour l’enregistrement. Au cours de chacune de ces opérations de mise à jour, le serveur effectue un cast du pointeur void en pointeur vers un entier.

Une fois que le programme serveur a fait pointer le handle de contexte au niveau des données de contexte, le handle est considéré comme ouvert. Les handles contenant une valeur **null** sont fermés. Le serveur maintient un handle de contexte ouvert jusqu’à ce que le client appelle une procédure distante qui le ferme. Si la session cliente se termine alors que le descripteur est ouvert, le runtime RPC appelle la routine d’exécution de serveur pour libérer le handle.

Le fragment de code suivant montre comment un serveur peut implémenter un handle de contexte. Dans cet exemple, le serveur gère un fichier de données écrit par le client à l’aide de procédures distantes. Les informations de contexte sont un handle de fichier qui effectue le suivi de l’emplacement actuel dans le fichier où le serveur écrira les données. Le descripteur de fichier est empaqueté en tant que handle de contexte dans la liste de paramètres pour les appels de procédure distante. Une structure contient le nom de fichier et le descripteur de fichier. La définition d’interface pour cet exemple est indiquée dans [développement d’interface à l’aide de handles de contexte](interface-development-using-context-handles.md).


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



La fonction RemoteOpen ouvre un fichier sur le serveur :


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



La fonction RemoteRead lit un fichier sur le serveur.


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



La fonction RemoteClose ferme un fichier sur le serveur. Notez que l’application serveur doit assigner la **valeur null** au handle de contexte dans le cadre de la fonction de fermeture. Cela communique avec le stub serveur et la bibliothèque Runtime RPC que le handle de contexte a été supprimé. Dans le cas contraire, la connexion est maintenue ouverte et une exécution de contexte est finalement effectuée.


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
> Bien qu’il soit attendu, le client passe un handle de contexte valide à un appel avec \[ in, out \] Attributes, RPC ne rejette pas les handles de contexte **null** pour cette combinaison d’attributs directionnels. Le descripteur de contexte **null** est passé au serveur en tant que pointeur **null** . Le code serveur pour les appels contenant un \[ handle de contexte in, out \] doit être écrit pour éviter une violation d’accès lors de la réception d’un pointeur **null** .

 

 

 




