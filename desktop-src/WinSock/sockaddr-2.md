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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520245"
---
# <a name="sockaddr"></a>sockaddr

La structure sockaddr varie selon le protocole sélectionné. À l’exception du paramètre *Sin \* \_ Family* , le contenu sockaddr est exprimé dans l’ordre des octets du réseau.

Les fonctions Winsock utilisant sockaddr ne sont pas strictement interprétées comme des pointeurs vers une structure sockaddr. La structure est interprétée différemment dans le contexte de différentes familles d’adresses. La seule exigence est que le premier **u \_ short** soit la famille d’adresses et que la taille totale de la mémoire tampon en octets soit *namelen*.

La structure de [**\_ stockage sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) stocke également les informations d’adresse de socket et la structure est suffisamment volumineuse pour stocker les informations d’adresse IPv4 ou IPv6. L’utilisation de la structure de **\_ stockage sockaddr** favorise l’indépendance des versions de protocole et de la famille de protocoles, et simplifie le développement. Il est recommandé d’utiliser la structure de **\_ stockage sockaddr** à la place de la structure sockaddr. la structure de **\_ stockage SOCKADDR** est prise en charge sur Windows Server 2003 et versions ultérieures.

La structure sockaddr et sockaddr \_ dans les structures ci-dessous sont utilisés avec IPv4. D’autres protocoles utilisent des structures similaires.

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

Les \_ structures sockaddr in6 et sockaddr \_ in6 \_ anciennes ci-dessous sont utilisées avec IPv6.

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

dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, **SOCKADDR** et **SOCKADDR \_ dans** les balises typedef sont définis pour SOCKADDR et SOCKADDR \_ dans les structures comme suit :

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

sur l’SDK Windows publiée pour Windows Vista et versions ultérieures, l’organisation des fichiers d’en-tête a changé et les structures sockaddr et sockaddr \_ sont définies dans le fichier d’en-tête *Ws2def. h* , et non dans le fichier d’en-tête *Winsock2. h* . Le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans le fichier d’en-tête *Winsock2. h* . La \_ structure sockaddr in6 est définie dans le fichier d’en-tête *Ws2ipdef. h* , et non dans le fichier d’en-tête *Ws2tcpip. h* . Le fichier d’en-tête *Ws2ipdef. h* est automatiquement inclus dans le fichier d’en-tête *Ws2tcpip. h* . Les fichiers d’en-tête *Ws2def. h* et *Ws2ipdef. h* ne doivent jamais être utilisés directement.

## <a name="example-code"></a>Exemple de code

L’exemple suivant illustre l’utilisation de la structure **sockaddr** .


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



## <a name="see-also"></a>Voir aussi

[**\_stockage sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))


 

 
