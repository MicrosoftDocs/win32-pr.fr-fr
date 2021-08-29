---
title: Définition et récupération d’options Internet
description: Cette rubrique explique comment définir et récupérer des options Internet à l’aide des fonctions InternetSetOption et InternetQueryOption.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Définition et récupération d’options Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9440af59efc763e034615f7919e94c4cfe9227
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482485"
---
# <a name="setting-and-retrieving-internet-options"></a>Définition et récupération d’options Internet

Cette rubrique explique comment définir et récupérer des options Internet à l’aide des fonctions [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) et [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .

Les options Internet peuvent être définies ou récupérées à partir d’un handle de [**HINTERNET**](appendix-a-hinternet-handles.md) spécifié ou des paramètres actuels dans Microsoft Internet Explorer.

-   [Étapes d’implémentation](#implementation-steps)
    -   [Choix des options Internet](#choosing-internet-options)
    -   [Choix du handle HINTERNET](#choosing-the-hinternet-handle)
    -   [Définition ou récupération des options](#setting-or-retrieving-the-options)
-   [Étendue du descripteur HINTERNET](#scope-of-hinternet-handle)
-   [Définition des options individuelles](#setting-individual-options)
-   [Récupération d’options individuelles](#retrieving-individual-options)
    -   [Exemple complet](#complete-sample)
-   [Définition des options de connexion](#setting-connection-options)
-   [Récupération des options de connexion](#retrieving-connection-options)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-steps"></a>Étapes d’implémentation

Pour définir ou récupérer des options Internet, procédez comme suit :

-   [Choix des options Internet](#choosing-internet-options)
-   [Choix du handle HINTERNET](#choosing-the-hinternet-handle)
-   [Définition ou récupération des options](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a>Choix des options Internet

Étant donné que de nombreuses options Internet sont disponibles, il est important de choisir les options appropriées. De nombreuses options Internet affectent le comportement des fonctions WinINet et d’Internet Explorer :

Par exemple, vous pouvez :

-   Gérez l’authentification du serveur et du proxy de base en définissant les noms d’utilisateur et les mots de passe.
-   Définissez ou récupérez la chaîne de l’agent utilisateur utilisée par les serveurs pour identifier les fonctionnalités de l’application cliente ou du navigateur.
-   Récupère le type de handle du handle [**HINTERNET**](appendix-a-hinternet-handles.md) spécifié.

Pour plus d’informations et pour obtenir la liste des options Internet, consultez [**indicateurs d’option**](option-flags.md).

Dans Internet Explorer 5 et versions ultérieures, certaines options peuvent être définies ou récupérées à partir d’une connexion Internet spécifique à l’aide de la [**\_ \_ \_ \_ liste d’options Internet par**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) connexion et des structures d' [**\_ \_ \_ option Internet par Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) . Pour plus d’informations et pour obtenir la liste des options qui peuvent être définies ou récupérées à partir d’une connexion Internet spécifique, consultez le membre **dwOptions** de la structure d' [**\_ option Internet par \_ conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .

### <a name="choosing-the-hinternet-handle"></a>Choix du handle HINTERNET

Le handle [**HINTERNET**](appendix-a-hinternet-handles.md) utilisé pour définir ou récupérer les options Internet détermine l’étendue de l’opération. Tous les descripteurs créés par le biais de ce descripteur hériteront des options définies sur ce descripteur.

Par exemple, les applications clientes qui requièrent un proxy avec l’authentification n’ont probablement pas besoin de définir le nom d’utilisateur et le mot de passe du proxy chaque fois que l’application tente d’accéder à une ressource Internet. Si toutes les demandes sur une connexion donnée sont gérées par le même proxy, la définition du nom d’utilisateur et du mot de passe du proxy sur un handle de type de connexion [**HINTERNET**](appendix-a-hinternet-handles.md) , autrement dit un handle créé par un appel à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), permettrait à tous les appels dérivés de ce handle **HINTERNET** d’utiliser le même nom d’utilisateur et mot de passe proxy. La définition du nom d’utilisateur et du mot de passe du proxy chaque fois qu’un descripteur **HINTERNET** est créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) nécessiteraient une surcharge supplémentaire et inutile. Sachez que si l’application utilise un proxy qui nécessite une authentification, elle doit définir les informations d’identification de proxy sur chaque nouvelle connexion.

### <a name="setting-or-retrieving-the-options"></a>Définition ou récupération des options

Une fois que vous avez déterminé les options Internet et le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) à utiliser, récupérez ces options Internet. Pour définir ou récupérer des options, appelez [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

## <a name="scope-of-hinternet-handle"></a>Étendue du descripteur HINTERNET

Le handle [**HINTERNET**](appendix-a-hinternet-handles.md) utilisé pour définir ou récupérer les options Internet détermine les actions pour lesquelles les options sont valides.

Ces handles ont trois niveaux :

-   Le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) racine (créé par un appel à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) contient toutes les options Internet qui affectent cette instance de wininet.
-   Handles [**HINTERNET**](appendix-a-hinternet-handles.md) qui se connectent à un serveur (créé par un appel à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))
-   [**HINTERNET**](appendix-a-hinternet-handles.md) Handles associés à une ressource ou une énumération de ressources sur un serveur particulier.

En plus des différents descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) , une application peut également utiliser la **valeur null** pour définir ou récupérer les valeurs par défaut des options Internet utilisées par Internet Explorer et les fonctions WinInet. La définition des options Internet lors de l’utilisation de **null** comme handle modifie les valeurs par défaut des options, qui sont actuellement stockées dans le registre. Les applications clientes ne doivent pas utiliser les fonctions de Registre pour modifier les valeurs par défaut des options Internet, car l’implémentation de la manière dont les options sont stockées peut être modifiée à l’avenir.

Le tableau suivant répertorie le type des descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) et l’étendue des options Internet qui leur sont associées.




| Type de handle | Étendue | 
|-------------|-------|
| <strong>NULL</strong> | Paramètres d’option par défaut pour Internet Explorer. | 
| INTERNET_HANDLE_TYPE_CONNECT_FTP | Les paramètres d’option pour cette connexion à un serveur FTP. Ces options affectent les opérations lancées à partir de ce handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , telles que les téléchargements de fichiers. | 
| INTERNET_HANDLE_TYPE_CONNECT_GOPHER | Les paramètres d’option pour cette connexion à un serveur Gopher. Ces options affectent les opérations lancées à partir de ce handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , telles que les téléchargements de fichiers.<blockquote>[!Note]<br />Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</blockquote><br /> | 
| INTERNET_HANDLE_TYPE_CONNECT_HTTP | Les paramètres d’option pour cette connexion à un serveur HTTP. Ces options affectent les opérations lancées à partir de ce handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , telles que les téléchargements de fichiers. | 
| INTERNET_HANDLE_TYPE_FILE_REQUEST | Paramètres d’option associés à cette demande de fichier. | 
| INTERNET_HANDLE_TYPE_FTP_FILE | Paramètres d’option associés à ce téléchargement de ressource FTP. | 
| INTERNET_HANDLE_TYPE_FTP_FILE_HTML | Les paramètres d’option associés à ce téléchargement de ressource FTP au format HTML. | 
| INTERNET_HANDLE_TYPE_FTP_FIND | Paramètres d’option associés à cette recherche de fichiers sur un serveur FTP. | 
| INTERNET_HANDLE_TYPE_FTP_FIND_HTML | Les paramètres d’option associés à cette recherche de fichiers sur un serveur FTP au format HTML. | 
| INTERNET_HANDLE_TYPE_GOPHER_FILE | Les paramètres d’option associés à ce téléchargement de ressource Gopher.<blockquote>[!Note]<br />Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</blockquote><br /> | 
| INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML | Paramètres d’option associés à ce téléchargement de ressources Gopher au format HTML.<blockquote>[!Note]<br />Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</blockquote><br /> | 
| INTERNET_HANDLE_TYPE_GOPHER_FIND | Paramètres d’option associés à cette recherche de fichiers sur un serveur Gopher.<blockquote>[!Note]<br />Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</blockquote><br /> | 
| INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML | Les paramètres d’option associés à cette recherche de fichiers sur un serveur Gopher au format HTML.<blockquote>[!Note]<br />Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</blockquote><br /> | 
| INTERNET_HANDLE_TYPE_HTTP_REQUEST | Paramètres d’option associés à cette requête HTTP. | 
| INTERNET_HANDLE_TYPE_INTERNET | Les paramètres d’option associés à cette instance des fonctions WinINet. | 




 

## <a name="setting-individual-options"></a>Définition des options individuelles

Après avoir déterminé les options Internet que vous souhaitez définir et l’étendue que vous souhaitez affecter par ces options, la définition des options Internet n’est pas compliquée. Il vous suffit d’appeler la fonction [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) avec le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) souhaité, l’indicateur d’option Internet et une mémoire tampon qui contient les informations que vous souhaitez définir.

L’exemple suivant montre comment définir le nom d’utilisateur et le mot de passe du proxy sur un handle [**HINTERNET**](appendix-a-hinternet-handles.md) spécifié.


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a>Récupération d’options individuelles

Les options Internet peuvent être récupérées à l’aide de la fonction [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) . Pour récupérer les options Internet :

1.  Déterminez la taille de mémoire tampon nécessaire pour récupérer les informations sur les options Internet.

    La taille de la mémoire tampon peut être déterminée à l’aide de **null** pour l’adresse de la mémoire tampon et en lui passant une taille de mémoire tampon de zéro.

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    La valeur retournée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) est la quantité de mémoire nécessaire pour récupérer les informations, en octets.

2.  Allouez une mémoire pour la mémoire tampon.
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  Récupérez les données.
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  Libérez de la mémoire.
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a>Exemple complet

Voici l’exemple complet utilisé dans la section précédente. Cet exemple montre comment récupérer la chaîne de l’agent utilisateur par défaut.


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a>Définition des options de connexion

Dans Internet Explorer 5 et versions ultérieures, les options Internet peuvent être définies pour sur une connexion spécifique. Auparavant, toutes les connexions partageaient les mêmes paramètres d’option Internet. Pour définir les options d’une connexion particulière :

1.  Créer une structure de [**\_ liste d’options Internet par \_ conn \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .
2.  Allouez la mémoire pour les options Internet individuelles que vous souhaitez définir pour la connexion.
3.  Définissez les options dans les structures d' [**\_ \_ \_ option Internet par Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .
4.  Définissez les options à l’aide de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

L’exemple de code suivant montre comment définir des données de proxy pour une connexion LAN.


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a>Récupération des options de connexion

Dans Internet Explorer 5 et versions ultérieures, les options Internet peuvent être récupérées à partir d’une connexion spécifique. Pour récupérer les options d’une connexion particulière :

1.  Créer une structure de [**\_ liste d’options Internet par \_ conn \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .
2.  Allouez la mémoire pour les options Internet individuelles à récupérer à partir de la connexion.
3.  Spécifiez les options à l’aide de structures d' [**\_ \_ \_ option Internet par Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .
4.  Récupérez les options à l’aide de [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).
5.  Utilisez les données d’option.
6.  Libérez la mémoire, allouée pour contenir les données d’option, à l’aide de la fonction [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de l’authentification](handling-authentication.md)
</dt> <dt>

[Handles HINTERNET](appendix-a-hinternet-handles.md)
</dt> </dl>

 

