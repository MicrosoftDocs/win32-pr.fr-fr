---
title: Récupération des en-têtes HTTP
description: Ce didacticiel explique comment récupérer des informations d’en-tête à partir de requêtes HTTP.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba9c1dbae3447d5ae44c8d348394f2dc802ed9d7b4af7d99fde19d0b5d2c3d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955509"
---
# <a name="retrieving-http-headers"></a>Récupération des en-têtes HTTP

Ce didacticiel explique comment récupérer des informations d’en-tête à partir de requêtes HTTP.

## <a name="implementation-steps"></a>Étapes d’implémentation

Il existe deux façons de récupérer les informations d’en-tête :

-   Utilisez l’une des constantes d' [**indicateur d’informations de requête**](query-info-flags.md) associées à l’en-tête http dont votre application a besoin.
-   Utilisez l' \_ \_ indicateur d’attribut personnalisé de requête HTTP et transmettez le nom de l’en-tête http.

L’utilisation de la constante associée à l’en-tête HTTP dont votre application a besoin est plus rapide en interne, mais il peut y avoir des en-têtes HTTP qui ne sont pas associés à une constante. Dans ce cas, la méthode utilisant l' \_ indicateur d' \_ attribut personnalisé de requête HTTP est disponible.

Les deux méthodes utilisent la fonction [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) . [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) prend le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) sur lequel la requête HTTP a été effectuée, un attribut, une mémoire tampon, une valeur DWORD qui contient la taille de la mémoire tampon et une valeur d’index. Un modificateur peut également être ajouté à l’attribut passé à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) pour indiquer dans quel format les données doivent être retournées.

### <a name="retrieving-headers-using-a-constant"></a>Récupération des en-têtes à l’aide d’une constante

Pour utiliser la fonction [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) pour récupérer un en-tête http à l’aide d’une constante, procédez comme suit :

1.  Appelez [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) avec une constante de la liste d' [**attributs**](query-info-flags.md) , une mémoire tampon **null** et la variable qui contient la taille de la mémoire tampon définie à zéro. En outre, si votre application a besoin des données dans un format particulier, vous pouvez ajouter une constante à partir de la liste des [**modificateurs**](query-info-flags.md) .
2.  Si l’en-tête HTTP demandé existe, l’appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) doit échouer, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) doit retourner une erreur de \_ mémoire tampon insuffisante \_ et la variable transmise pour le paramètre *lpdwBufferLength* doit être définie sur le nombre d’octets requis.
3.  Allouez une mémoire tampon avec le nombre d’octets requis.
4.  Réessayez l’appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

L’exemple suivant illustre un appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) à l’aide de la \_ \_ constante d’en-têtes bruts de requête HTTP \_ \_ CRLF, qui est une valeur spéciale qui demande tous les en-têtes http retournés.


```C++
// Retrieving Headers Using a Constant
BOOL SampleCodeOne(HINTERNET hHttp)
{
   LPVOID lpOutBuffer=NULL;
   DWORD dwSize = 0;

retry:

   // This call will fail on the first pass, because
   // no buffer is allocated.
   if(!HttpQueryInfo(hHttp,HTTP_QUERY_RAW_HEADERS_CRLF,
      (LPVOID)lpOutBuffer,&dwSize,NULL))
   {
      if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
      {
         // Code to handle the case where the header isn't available.
         return TRUE;
      }
      else
      {
        // Check for an insufficient buffer.
        if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
        {
            // Allocate the necessary buffer.
            lpOutBuffer = new char[dwSize];

            // Retry the call.
            goto retry;
        }
        else
        {
            // Error handling code.
            if (lpOutBuffer)
            {
               delete [] lpOutBuffer;
            }
            return FALSE;
        }
      }
   }

   if (lpOutBuffer)
   {
      delete [] lpOutBuffer;
   }

   return TRUE;
}
```



### <a name="retrieving-headers-using-http_query_custom"></a>Récupération des en-têtes à l’aide d’une \_ requête HTTP \_ personnalisée

Pour utiliser la fonction [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) pour récupérer un en-tête http à l’aide d’une \_ requête HTTP \_ personnalisée, procédez comme suit :

1.  Allouez une mémoire tampon suffisamment grande pour contenir le nom de chaîne de l’en-tête HTTP.
2.  Écrivez le nom de chaîne de l’en-tête HTTP dans la mémoire tampon.
3.  Appelez [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) avec une \_ requête HTTP \_ personnalisée, la mémoire tampon qui contient le nom de chaîne de l’en-tête http et la variable qui contient la taille de la mémoire tampon. En outre, si votre application a besoin des données dans un format particulier, vous pouvez ajouter une constante à partir de la liste des [**modificateurs**](query-info-flags.md) .
4.  Si l’appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) échoue et que [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne \_ une erreur de mémoire tampon insuffisante \_ , réaffectez une mémoire tampon avec le nombre d’octets requis.
5.  Réécrivez le nom de la chaîne de l’en-tête HTTP dans la mémoire tampon.
6.  Réessayez l’appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

L’exemple suivant illustre un appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) à l’aide de la \_ \_ constante personnalisée de requête HTTP pour demander l’en-tête HTTP Content-type.


```C++
// Retrieving Headers Using HTTP_QUERY_CUSTOM
BOOL SampleCodeTwo(HINTERNET hHttp)
{
    DWORD dwSize = 20;
    LPVOID lpOutBuffer = new char[dwSize];

    StringCchPrintfA((LPSTR)lpOutBuffer,dwSize,"Content-Type");

retry:

    if(!HttpQueryInfo(hHttp,HTTP_QUERY_CUSTOM,
        (LPVOID)lpOutBuffer,&dwSize,NULL))
    {
        if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
        {
            // Code to handle the case where the header isn't available.
            delete [] lpOutBuffer;
            return TRUE;
        }
        else
        {
            // Check for an insufficient buffer.
            if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
            {
                // Allocate the necessary buffer.
                delete [] lpOutBuffer;
                lpOutBuffer = new char[dwSize];

                // Rewrite the header name in the buffer.
                StringCchPrintfA((LPSTR)lpOutBuffer,
                                 dwSize,"Content-Type");

                // Retry the call.
                goto retry;
            }
            else
            {
                // Error handling code.
                delete [] lpOutBuffer;
                return FALSE;
            }
        }
    }

   return TRUE;
}
```



> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 