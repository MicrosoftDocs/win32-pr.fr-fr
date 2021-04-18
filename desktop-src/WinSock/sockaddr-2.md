---
description: La structure sockaddr varie selon le protocole sélectionné.
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
title: sockaddr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sockaddr
api_type:
- NA
api_location: ''
ms.openlocfilehash: ccd4b98efc987630ab625e5c9788f0be16018e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519841"
---
# <a name="sockaddr"></a><span data-ttu-id="4f03f-103">sockaddr</span><span class="sxs-lookup"><span data-stu-id="4f03f-103">sockaddr</span></span>

<span data-ttu-id="4f03f-104">La structure sockaddr varie selon le protocole sélectionné.</span><span class="sxs-lookup"><span data-stu-id="4f03f-104">The sockaddr structure varies depending on the protocol selected.</span></span> <span data-ttu-id="4f03f-105">À l’exception du paramètre *Sin \* \_ Family* , le contenu sockaddr est exprimé dans l’ordre des octets du réseau.</span><span class="sxs-lookup"><span data-stu-id="4f03f-105">Except for the *sin\*\_family* parameter, sockaddr contents are expressed in network byte order.</span></span>

<span data-ttu-id="4f03f-106">Les fonctions Winsock utilisant sockaddr ne sont pas strictement interprétées comme des pointeurs vers une structure sockaddr.</span><span class="sxs-lookup"><span data-stu-id="4f03f-106">Winsock functions using sockaddr are not strictly interpreted to be pointers to a sockaddr structure.</span></span> <span data-ttu-id="4f03f-107">La structure est interprétée différemment dans le contexte de différentes familles d’adresses.</span><span class="sxs-lookup"><span data-stu-id="4f03f-107">The structure is interpreted differently in the context of different address families.</span></span> <span data-ttu-id="4f03f-108">La seule exigence est que le premier **u \_ short** soit la famille d’adresses et que la taille totale de la mémoire tampon en octets soit *namelen*.</span><span class="sxs-lookup"><span data-stu-id="4f03f-108">The only requirements are that the first **u\_short** is the address family and the total size of the memory buffer in bytes is *namelen*.</span></span>

<span data-ttu-id="4f03f-109">La structure de [**\_ stockage sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) stocke également les informations d’adresse de socket et la structure est suffisamment volumineuse pour stocker les informations d’adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="4f03f-109">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure also stores socket address information and the structure is sufficiently large to store IPv4 or IPv6 address information.</span></span> <span data-ttu-id="4f03f-110">L’utilisation de la structure de **\_ stockage sockaddr** favorise l’indépendance des versions de protocole et de la famille de protocoles, et simplifie le développement.</span><span class="sxs-lookup"><span data-stu-id="4f03f-110">The use of the **SOCKADDR\_STORAGE** structure promotes protocol-family and protocol-version independence, and simplifies development.</span></span> <span data-ttu-id="4f03f-111">Il est recommandé d’utiliser la structure de **\_ stockage sockaddr** à la place de la structure sockaddr.</span><span class="sxs-lookup"><span data-stu-id="4f03f-111">It is recommended that the **SOCKADDR\_STORAGE** structure be used in place of the sockaddr structure.</span></span> <span data-ttu-id="4f03f-112">La structure de **\_ stockage sockaddr** est prise en charge sur Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4f03f-112">The **SOCKADDR\_STORAGE** structure is supported on Windows Server 2003 and later.</span></span>

<span data-ttu-id="4f03f-113">La structure sockaddr et sockaddr \_ dans les structures ci-dessous sont utilisés avec IPv4.</span><span class="sxs-lookup"><span data-stu-id="4f03f-113">The sockaddr structure and sockaddr\_in structures below are used with IPv4.</span></span> <span data-ttu-id="4f03f-114">D’autres protocoles utilisent des structures similaires.</span><span class="sxs-lookup"><span data-stu-id="4f03f-114">Other protocols use similar structures.</span></span>

``` syntax
struct sockaddr {
        ushort  sa_family;
        char    sa_data[14];
};

struct sockaddr_in {
        short   sin_family;
        u_short sin_port;
        struct  in_addr sin_addr;
        char    sin_zero[8];
};
```

<span data-ttu-id="4f03f-115">Les \_ structures sockaddr in6 et sockaddr \_ in6 \_ anciennes ci-dessous sont utilisées avec IPv6.</span><span class="sxs-lookup"><span data-stu-id="4f03f-115">The sockaddr\_in6 and sockaddr\_in6\_old structures below are used with IPv6.</span></span>

``` syntax
struct sockaddr_in6 {
        short   sin6_family;
        u_short sin6_port;
        u_long  sin6_flowinfo;
        struct  in6_addr sin6_addr;
        u_long  sin6_scope_id;
};

typedef struct sockaddr_in6 SOCKADDR_IN6;
typedef struct sockaddr_in6 *PSOCKADDR_IN6;
typedef struct sockaddr_in6 FAR *LPSOCKADDR_IN6;


struct sockaddr_in6_old {
        short   sin6_family;        
        u_short sin6_port;          
        u_long  sin6_flowinfo;      
        struct  in6_addr sin6_addr;  
};
```

<span data-ttu-id="4f03f-116">Dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, **sockaddr** et **sockaddr \_ dans** les balises typedef sont définis pour sockaddr et sockaddr \_ dans les structures comme suit :</span><span class="sxs-lookup"><span data-stu-id="4f03f-116">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, **SOCKADDR** and **SOCKADDR\_IN** typedef tags are defined for sockaddr and sockaddr\_in structures as follows:</span></span>

``` syntax
typedef struct sockaddr {
#if (_WIN32_WINNT < 0x0600)
    u_short sa_family;
#else 
    ADDRESS_FAMILY sa_family;
#endif //(_WIN32_WINNT < 0x0600)
    CHAR sa_data[14];
} SOCKADDR, *PSOCKADDR, FAR *LPSOCKADDR;


typedef struct sockaddr_in {
#if(_WIN32_WINNT < 0x0600)
    short   sin_family;    
#else //(_WIN32_WINNT < 0x0600)
    ADDRESS_FAMILY sin_family;
#endif //(_WIN32_WINNT < 0x0600)
    USHORT sin_port;
    IN_ADDR sin_addr;
    CHAR sin_zero[8];
} SOCKADDR_IN, *PSOCKADDR_IN;
```

<span data-ttu-id="4f03f-117">Sur l’SDK Windows publiée pour Windows Vista et versions ultérieures, l’Organisation des fichiers d’en-tête a changé et les structures sockaddr et sockaddr \_ sont définies dans le fichier d’en-tête *Ws2def. h* , et non dans le fichier d’en-tête *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="4f03f-117">On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the sockaddr and sockaddr\_in structures are defined in the *Ws2def.h* header file, not the *Winsock2.h* header file.</span></span> <span data-ttu-id="4f03f-118">Le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans le fichier d’en-tête *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="4f03f-118">The *Ws2def.h* header file is automatically included by the *Winsock2.h* header file.</span></span> <span data-ttu-id="4f03f-119">La \_ structure sockaddr in6 est définie dans le fichier d’en-tête *Ws2ipdef. h* , et non dans le fichier d’en-tête *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="4f03f-119">The sockaddr\_in6 structure is defined in the *Ws2ipdef.h* header file, not the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="4f03f-120">Le fichier d’en-tête *Ws2ipdef. h* est automatiquement inclus dans le fichier d’en-tête *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="4f03f-120">The *Ws2ipdef.h* header file is automatically included by the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="4f03f-121">Les fichiers d’en-tête *Ws2def. h* et *Ws2ipdef. h* ne doivent jamais être utilisés directement.</span><span class="sxs-lookup"><span data-stu-id="4f03f-121">The *Ws2def.h* and *Ws2ipdef.h* header files should never be used directly.</span></span>

## <a name="example-code"></a><span data-ttu-id="4f03f-122">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="4f03f-122">Example Code</span></span>

<span data-ttu-id="4f03f-123">L’exemple suivant illustre l’utilisation de la structure **sockaddr** .</span><span class="sxs-lookup"><span data-stu-id="4f03f-123">The following example demonstrates the use of the **sockaddr** structure.</span></span>


```C++

// Declare variables
SOCKET ListenSocket;
struct sockaddr_in saServer;
hostent* localHost;
char* localIP;

// Create a listening socket
ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);

// Get the local host information
localHost = gethostbyname("");
localIP = inet_ntoa (*(struct in_addr *)*localHost->h_addr_list);

// Set up the sockaddr structure
saServer.sin_family = AF_INET;
saServer.sin_addr.s_addr = inet_addr(localIP);
saServer.sin_port = htons(5150);

// Bind the listening socket using the
// information in the sockaddr structure
bind( ListenSocket,(SOCKADDR*) &saServer, sizeof(saServer) );


```



## <a name="see-also"></a><span data-ttu-id="4f03f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f03f-124">See Also</span></span>

<span data-ttu-id="4f03f-125">[**\_stockage sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f03f-125">[**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span></span>


 

 
