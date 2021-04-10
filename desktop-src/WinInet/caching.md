---
title: Mise en cache (Windows Internet)
description: Les fonctions WinINet disposent d’une prise en charge de la mise en cache intégrée simple, mais flexible.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102680"
---
# <a name="caching-windows-internet"></a>Mise en cache (Windows Internet)

Les fonctions WinINet disposent d’une prise en charge de la mise en cache intégrée simple, mais flexible. Toutes les données récupérées à partir du réseau sont mises en cache sur le disque dur et récupérées pour les demandes suivantes. L’application peut contrôler la mise en cache à chaque requête. Pour les requêtes http provenant du serveur, la plupart des en-têtes reçus sont également mis en cache. Quand une requête HTTP est satisfaite à partir du cache, les en-têtes mis en cache sont également retournés à l’appelant. Cela rend le téléchargement des données transparent, que les données proviennent du cache ou du réseau.

Les applications doivent allouer correctement un tampon afin d’obtenir les résultats souhaités lors de l’utilisation des fonctions de mise en cache des URL persistantes. Pour plus d’informations, consultez [utilisation de mémoires tampons](appendix-b-using-buffers.md).

## <a name="cache-behavior-during-response-processing"></a>Comportement du cache pendant le traitement de la réponse

Le cache WinINet est conforme aux directives de contrôle de cache HTTP décrites dans le document RFC 2616. Les directives de contrôle de cache et les indicateurs de jeu d’applications déterminent ce qui peut être mis en cache ; Toutefois, WinINet détermine ce qui est réellement mis en cache en fonction du critère suivant :

-   WinINet met uniquement en cache les réponses HTTP et FTP.
-   Seules les réponses bien comportent peuvent être stockées par un cache et utilisées dans une réponse à une demande ultérieure. Les réponses correctes sont définies comme des réponses qui renvoient correctement.
-   Par défaut, WinINet met en cache les réponses réussies, sauf si une directive Cache-Control du serveur ou un indicateur défini par l’application indique spécifiquement que la réponse ne peut pas être mise en cache.
-   En général, les réponses au verbe obtenir sont mises en cache si les spécifications répertoriées ci-dessus sont remplies. Les réponses aux verbes PUT et POSTCONNEXION ne sont en aucun cas mises en cache.
-   Les éléments sont mis en cache même lorsque le cache est saturé. Si un élément ajouté met le cache sur la limite de taille, le nettoyage du cache est planifié. Par défaut, il n’est pas garanti que les éléments restent dans le cache plus de 10 minutes. Pour plus d’informations, consultez la section [cache de nettoyage](#cache-scavenger) ci-dessous.
-   HTTPS est mis en cache par défaut. Cela est géré par un paramètre global qui ne peut pas être substitué par les directives de cache définies par l’application. Pour remplacer le paramètre global, sélectionnez l’applet options Internet dans le panneau de configuration, puis accédez à l’onglet Avancé. Cochez la case « ne pas enregistrer les pages chiffrées sur le disque » sous la section « sécurité ».

## <a name="cache-scavenger"></a>Nettoyage du cache

Le nettoyage du cache nettoie régulièrement les éléments du cache. Si un élément est ajouté au cache et que le cache est plein, l’élément est ajouté au cache et le nettoyage du cache est planifié. Si le nettoyage du cache termine un nettoyage et que le cache n’a pas atteint la limite du cache, le nettoyage est planifié pour un autre arrondi lorsqu’un autre élément est ajouté au cache. En général, le nettoyage est planifié lorsqu’un élément ajouté place le cache au-dessus de sa taille limite. Par défaut, la durée de vie minimale du cache est définie à 10 minutes, sauf indication contraire dans une directive Cache-Control. Lorsque le nettoyage du cache est initié, il n’y a aucune garantie que les éléments les plus anciens sont les premiers à être supprimés du cache.

Le cache est partagé entre toutes les applications WinINet sur l’ordinateur pour le même utilisateur. À compter de Windows Vista et de Windows Server 2008, la taille du cache est définie à 1/32e la taille du disque, avec une taille minimale de 8 Mo et une taille maximale de 50 Mo.

## <a name="using-flags-to-control-caching"></a>Utilisation d’indicateurs pour contrôler la mise en cache

Les indicateurs de mise en cache permettent à une application de contrôler le moment et la façon dont elle utilise le cache. Ces indicateurs peuvent être utilisés seuls ou en association avec le paramètre *dwFlags* dans des fonctions qui accèdent à des informations ou à des ressources sur Internet. Par défaut, les fonctions stockent toutes les données téléchargées à partir d’Internet.

Les indicateurs suivants peuvent être utilisés pour contrôler la mise en cache.



| Valeur                                                                                                                                                  | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_cache d’indicateur Internet \_ \_ asynchrone**](api-flags.md)                                                                            | Cet indicateur est sans effet.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**INTERNET \_ Flag \_ cache en \_ cas d' \_ \_ échec net**](api-flags.md)                                                              | Retourne la ressource à partir du cache en cas d’échec de la demande réseau de la ressource en raison d’une [erreur de \_ \_ \_ réinitialisation de la connexion Internet](wininet-errors.md) ou d’une erreur [ \_ Internet \_ ne peut pas \_ se connecter](wininet-errors.md) . Cet indicateur est utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                                                                              |
| [**\_cache sans indicateur Internet \_ \_**](api-flags.md)                                                                              | Ne met pas en cache les données, localement ou dans les passerelles. Identique à la valeur par défaut [**, \_ indicateur \_ Internet \_ sans \_ écriture**](api-flags.md)dans le cache.                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | Indique qu’il s’agit d’une soumission de formulaires.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Internet \_ indicateur \_ du \_ cache**](api-flags.md)[**Internet \_ Flag \_ Forms \_ Submit**](api-flags.md) | N’effectue pas de demandes réseau. Toutes les entités sont retournées à partir du cache. Si l’élément demandé n’est pas dans le cache, une erreur appropriée, telle qu’un fichier d’erreur \_ \_ \_ introuvable, est retournée. Seule la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) utilise cet indicateur.                                                                                                                                                                                                       |
| [**\_indicateur de \_ \_ retour sur Internet**](api-flags.md)                                                                                  | Indique que la fonction doit utiliser la copie de la ressource qui se trouve actuellement dans le cache Internet. La date d’expiration et les autres informations relatives à la ressource ne sont pas vérifiées. Si l’élément demandé est introuvable dans le cache Internet, le système tente de localiser la ressource sur le réseau. Cette valeur a été introduite dans Microsoft Internet Explorer 5 et est associée aux opérations de bouton **suivant** et **précédent** d’Internet Explorer. |
| [**\_ \_ lien hypertexte indicateur Internet**](api-flags.md)                                                                                 | Force l’application à recharger une ressource si aucune heure d’expiration et aucune heure de dernière modification n’ont été retournées lorsque la ressource a été stockée dans le cache.                                                                                                                                                                                                                                                                                                                  |
| [**\_indicateur Internet \_ rendre \_ persistant**](api-flags.md)                                                                    | N'est plus pris en charge.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**l' \_ indicateur Internet \_ doit mettre \_ en cache la \_ demande**](api-flags.md)                                                             | Entraîne la création d’un fichier temporaire si le fichier ne peut pas être mis en cache. Cela est identique à la valeur par défaut, le [**\_ \_ \_ fichier indicateur Internet requis**](api-flags.md).                                                                                                                                                                                                                                                                            |
| [**fichier de l' \_ indicateur Internet \_ requis \_**](api-flags.md)                                                                                | Entraîne la création d’un fichier temporaire si le fichier ne peut pas être mis en cache.                                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_indicateur Internet \_ sans \_ \_ écriture dans le cache**](api-flags.md)                                                                     | Rejette toute tentative par la fonction de stocker des données téléchargées à partir d’Internet dans le cache. Cet indicateur est nécessaire si l’application ne souhaite pas que les ressources téléchargées soient stockées localement.                                                                                                                                                                                                                                                               |
| [**\_indicateur Internet \_ sans \_ interface utilisateur**](api-flags.md)                                                                                        | Désactive la boîte de dialogue cookie. Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (requêtes http uniquement).                                                                                                                                                                                                                                                                                          |
| [**\_indicateur Internet \_ hors connexion**](api-flags.md)                                                                                     | Empêche l’application d’envoyer des demandes au réseau. Toutes les requêtes sont résolues à l’aide des ressources stockées dans le cache. Si la ressource ne se trouve pas dans le cache, une erreur appropriée, telle qu’un fichier d’erreur \_ \_ \_ introuvable, est retournée.                                                                                                                                                                                                                            |
| [**\_indicateur Internet \_ pragma \_ NoCache**](api-flags.md)                                                                      | Force la résolution de la demande par le serveur d’origine, même si une copie mise en cache existe sur le proxy. La fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (sur les requêtes HTTP et HTTPS uniquement) et la fonction [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) utilisent cet indicateur.                                                                                                                                                                                               |
| [**\_REchargement des indicateurs Internet \_**](api-flags.md)                                                                                       | Force la fonction à récupérer la ressource demandée directement à partir d’Internet. Les informations téléchargées sont stockées dans le cache.                                                                                                                                                                                                                                                                                                                     |
| [**resynchronisation des \_ indicateurs Internet \_**](api-flags.md)                                                                         | Fait en sorte qu’une application effectue un téléchargement conditionnel de la ressource à partir d’Internet. Si la version stockée dans le cache est à jour, les informations sont téléchargées à partir du cache. Dans le cas contraire, les informations sont rechargées à partir du serveur.                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a>Fonctions de mise en cache persistantes

Les clients qui ont besoin de services de mise en cache persistants utilisent les fonctions de mise en cache permanentes pour permettre à leurs applications d’enregistrer des données dans le système de fichiers local pour une utilisation ultérieure, par exemple dans les situations où une liaison à faible bande passante limite l’accès aux données, ou si l’accès n’est pas disponible.

Les fonctions de cache fournissent une mise en cache persistante et une navigation hors connexion. À moins que l’indicateur d' [**\_ écriture de \_ \_ cache \_ Internet ne**](api-flags.md) spécifie explicitement aucune mise en cache, les fonctions cachent toutes les données téléchargées à partir du réseau. Les réponses aux données publiées ne sont pas mises en cache.

## <a name="using-the-persistent-url-cache-functions"></a>Utilisation des fonctions de cache des URL persistantes

Les fonctions de cache d’URL persistantes suivantes permettent à une application d’accéder à des informations stockées dans le cache et de les manipuler.



| Fonction                                                           | Description                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitUrlCacheEntryA**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | Met en cache les données du fichier spécifié dans le stockage du cache et les associe à l’URL donnée.                                                                  |
| [**CommitUrlCacheEntryW**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | Met en cache les données du fichier spécifié dans le stockage du cache et les associe à l’URL donnée.                                                                  |
| [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | Alloue le stockage de cache demandé et crée un nom de fichier local pour enregistrer l’entrée de cache qui correspond au nom de la source.                           |
| [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | Génère une identification du groupe de caches.                                                                                                                       |
| [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | Supprime le fichier associé au nom de la source du cache, si ce fichier existe.                                                                          |
| [**DeleteUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | Libère un **GROUPID** et tout état associé dans le fichier d’index du cache.                                                                                      |
| [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | Ferme le handle d’énumération spécifié.                                                                                                                      |
| [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | Commence l’énumération du cache.                                                                                                                          |
| [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | Commence une énumération filtrée du cache.                                                                                                                   |
| [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | Récupère l’entrée suivante dans le cache.                                                                                                                        |
| [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | Récupère l’entrée suivante dans une énumération de cache filtrée.                                                                                                     |
| [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | Récupère des informations sur une entrée du cache.                                                                                                                    |
| [**GetUrlCacheEntryInfoEx**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | Recherche l’URL après avoir traduit toutes les redirections mises en cache qui seraient appliquées en mode hors connexion par [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).           |
| [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | Lit les données mises en cache à partir d’un flux qui a été ouvert à l’aide de [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).                            |
| [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | Récupère une entrée de cache du cache sous la forme d’un fichier.                                                                                                 |
| [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | Offre le moyen le plus efficace et indépendant de l’implémentation d’accéder aux données du cache.                                                                   |
| [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | Ajoute ou supprime des entrées d’un groupe de cache.                                                                                                                   |
| [**SetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | Définit les membres spécifiés de la structure d' [**\_ \_ \_ informations d’entrée du cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .                                                |
| [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | Déverrouille l’entrée de cache qui a été verrouillée lors de la récupération du fichier pour une utilisation à partir du cache par [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea). |
| [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | Ferme le flux qui a été récupéré à l’aide de [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).                                           |



 

### <a name="enumerating-the-cache"></a>Énumération du cache

Les fonctions [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) et [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) énumèrent les informations stockées dans le cache. [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) démarre l’énumération en adoptant un modèle de recherche, une mémoire tampon et une taille de mémoire tampon pour créer un handle et retourner la première entrée du cache. [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) prend le handle créé par [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), une mémoire tampon et une taille de mémoire tampon pour retourner la prochaine entrée de cache.

Les deux fonctions stockent une structure d' [**\_ informations d' \_ entrée \_ de cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) dans la mémoire tampon. La taille de cette structure varie pour chaque entrée. Si la taille de la mémoire tampon passée à l’une ou l’autre des fonctions est insuffisante, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ mémoire tampon insuffisante \_ . La variable de taille de la mémoire tampon contient la taille de la mémoire tampon nécessaire pour récupérer cette entrée de cache. Une mémoire tampon de la taille indiquée par la variable de taille de mémoire tampon doit être allouée, et la fonction doit être appelée à nouveau avec la nouvelle mémoire tampon.

La structure des informations d' [**\_ entrée du cache \_ \_ Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) contient la taille de la structure, l’URL des informations mises en cache, le nom du fichier local, le type d’entrée du cache, le nombre d’utilisations, le taux d’accès, la taille, l’heure de la dernière modification, l’expiration, l’heure de la dernière synchronisation, les informations d’en-tête et l’extension de nom

La fonction [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) prend un modèle de recherche, une mémoire tampon qui stocke la structure d’informations d' [**entrée du \_ cache \_ \_ Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) et la taille de la mémoire tampon. Actuellement, seul le modèle de recherche par défaut, qui retourne toutes les entrées de cache, est implémenté.

Une fois le cache énuméré, l’application doit appeler [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) pour fermer le descripteur d’énumération du cache.

L’exemple suivant affiche l’URL de chaque entrée de cache dans une zone de liste, **IDC \_ CacheList**. Elle utilise \_ \_ \_ la taille maximale des informations d’entrée du cache \_ pour allouer initialement une mémoire tampon, puisque les versions antérieures de l’API WinInet n’énumèrent pas correctement le cache. Les versions ultérieures énumèrent le cache correctement et il n’y a aucune limite de taille de cache. Toutes les applications qui s’exécutent sur des ordinateurs avec la version de l’API WinINet d’Internet Explorer 4,0 doivent allouer une mémoire tampon de la taille requise. Pour plus d’informations, consultez [utilisation de mémoires tampons](appendix-b-using-buffers.md).


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a>Récupération des informations d’entrée du cache

La fonction [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) vous permet de récupérer la structure d’informations d' [**entrée du \_ cache \_ \_ Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) pour l’URL spécifiée. Cette structure contient la taille de la structure, l’URL des informations mises en cache, le nom du fichier local, le type d’entrée du cache, le nombre d’utilisations, le taux d’accès, la taille, l’heure de la dernière modification, l’expiration, l’heure de la dernière synchronisation, les informations d’en-tête, la taille des informations d’en-tête et l’extension

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accepte une URL, une mémoire tampon pour une structure d' [**\_ \_ \_ informations d’entrée du cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) et la taille de la mémoire tampon. Si l’URL est trouvée, les informations sont copiées dans la mémoire tampon. Dans le cas contraire, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le fichier d’erreur \_ \_ \_ introuvable. Si la taille de la mémoire tampon est insuffisante pour stocker les informations d’entrée du cache, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur de \_ mémoire tampon insuffisante \_ . La taille requise pour récupérer les informations est stockée dans la variable de taille de la mémoire tampon.

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) n’effectue aucune analyse d’URL ; par conséquent, une URL qui contient une ancre ( \# ) ne se trouve pas dans le cache, même si la ressource est mise en cache. Par exemple, si l’URL « https://example.com/example.htm\#sample » est passée, la fonction retourne le \_ fichier \_ \_ d’erreur introuvable même si « https://example.com/example.htm » se trouve dans le cache.

L’exemple suivant récupère les informations d’entrée de cache pour l’URL spécifiée. La fonction affiche ensuite les informations d’en-tête dans la zone d’édition **IDC \_ CacheDump** .


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a>Création d’une entrée de cache

Une application utilise les fonctions [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) et [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) pour créer une entrée de cache.

[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accepte l’URL, la taille de fichier attendue et l’extension de nom de fichier. La fonction crée ensuite un nom de fichier local pour enregistrer l’entrée de cache qui correspond à l’URL et à l’extension de nom de fichier.

À l’aide du nom de fichier local, écrivez les données dans le fichier local. Une fois que les données ont été écrites dans le fichier local, l’application doit appeler [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).

[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accepte l’URL, le nom de fichier local, l’expiration, l’heure de dernière modification, le type d’entrée du cache, les informations d’en-tête, la taille des informations d’en-tête et l’extension de nom de fichier. La fonction met ensuite en cache les données dans le fichier spécifié dans le stockage du cache et les associe à l’URL donnée.

L’exemple suivant utilise le nom de fichier local, créé par un appel précédent à [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), stocké dans la zone de texte, par **IDC \_ fichier_local**, pour stocker le texte de la zone de texte, **IDC \_ CacheDump**, dans l’entrée de cache. Une fois que les données ont été écrites dans le fichier à l’aide de **fopen**, **fprintf** et **fclose**, l’entrée est validée à l’aide de [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a>Suppression d’une entrée de cache

La fonction [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) prend une URL et supprime le fichier cache qui lui est associé. Si le fichier cache n’existe pas, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le \_ fichier d’erreur \_ \_ introuvable. Si le fichier cache est actuellement verrouillé ou en cours d’utilisation, la fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ accès \_ refusé. Le fichier est supprimé lorsqu’il est déverrouillé.

### <a name="retrieving-cache-entry-files"></a>Récupération des fichiers d’entrée du cache

Pour les applications qui requièrent le nom de fichier d’une ressource, utilisez les fonctions [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) et [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) . Les applications qui n’ont pas besoin du nom de fichier doivent utiliser les fonctions [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)et [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) pour récupérer les informations dans le cache.

[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) n’effectue aucune analyse d’URL ; par conséquent, une URL qui contient une ancre ( \# ) ne se trouve pas dans le cache, même si la ressource est mise en cache. Par exemple, si l’URL « https://example.com/example.htm\#sample » est passée, la fonction retourne le \_ fichier \_ \_ d’erreur introuvable même si « https://example.com/example.htm » se trouve dans le cache.

[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accepte une URL, une mémoire tampon qui stocke la structure des [**\_ informations d' \_ entrée \_ du cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) et la taille de la mémoire tampon. La fonction est récupérée et verrouillée pour l’appelant.

Une fois que les informations du fichier ont été utilisées, l’application doit appeler [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) pour déverrouiller le fichier.

### <a name="cache-groups"></a>Groupes de cache

Pour créer un groupe de caches, la fonction [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) doit être appelée pour générer un **GROUPID** pour le groupe de cache. Les entrées peuvent être ajoutées au groupe de cache en fournissant l’URL de l’entrée du cache et \_ l' \_ indicateur ajouter du groupe de cache Internet \_ à la fonction [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) . Pour supprimer une entrée de cache d’un groupe, transmettez l’URL de l’entrée de cache et l' \_ \_ indicateur de suppression du groupe de cache Internet \_ à [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).

Les fonctions [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) et [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) peuvent être utilisées pour énumérer les entrées dans un groupe de caches spécifié. Une fois l’énumération terminée, la fonction doit appeler [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).

## <a name="handling-structures-with-variable-size-information"></a>Gestion des structures avec des informations sur la taille des variables

Le cache peut contenir des informations sur la taille des variables pour chaque URL stockée. Cela se répercute dans la structure des [**\_ \_ \_ informations d’entrée du cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) . Lorsque les fonctions de cache retournent cette structure, elles créent une mémoire tampon qui correspond toujours à la taille des informations d' [**\_ entrée de cache \_ \_ Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) plus toute information de taille de variable. Si un membre pointeur n’a pas la **valeur null**, il pointe vers la zone mémoire immédiatement après la structure. Lors de la copie de la mémoire tampon retournée par une fonction dans une autre mémoire tampon, les membres du pointeur doivent être corrigés pour pointer vers l’emplacement approprié dans la nouvelle mémoire tampon, comme le montre l’exemple suivant.

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

Certaines fonctions de cache échouent avec le message d’erreur erreur de \_ mémoire tampon insuffisante \_ si vous spécifiez une mémoire tampon qui est trop petite pour contenir les informations d’entrée de cache récupérées par la fonction. Dans ce cas, la fonction retourne également la taille requise de la mémoire tampon. Vous pouvez ensuite allouer une mémoire tampon de la taille appropriée et appeler à nouveau la fonction.

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
