---
title: Récupération des en-têtes HTTP
description: Ce didacticiel explique comment récupérer des informations d’en-tête à partir de requêtes HTTP.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b31043940b8c2127d1cfa1696d2821641d0784
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510490"
---
# <a name="retrieving-http-headers"></a><span data-ttu-id="1783c-103">Récupération des en-têtes HTTP</span><span class="sxs-lookup"><span data-stu-id="1783c-103">Retrieving HTTP Headers</span></span>

<span data-ttu-id="1783c-104">Ce didacticiel explique comment récupérer des informations d’en-tête à partir de requêtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="1783c-104">This tutorial describes how to retrieve header information from HTTP requests.</span></span>

## <a name="implementation-steps"></a><span data-ttu-id="1783c-105">Étapes d’implémentation</span><span class="sxs-lookup"><span data-stu-id="1783c-105">Implementation Steps</span></span>

<span data-ttu-id="1783c-106">Il existe deux façons de récupérer les informations d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1783c-106">There are two ways to retrieve the header information:</span></span>

-   <span data-ttu-id="1783c-107">Utilisez l’une des constantes d' [**indicateur d’informations de requête**](query-info-flags.md) associées à l’en-tête http dont votre application a besoin.</span><span class="sxs-lookup"><span data-stu-id="1783c-107">Use one of the [**Query Info Flag**](query-info-flags.md) constants associated with the HTTP header that your application needs.</span></span>
-   <span data-ttu-id="1783c-108">Utilisez l' \_ \_ indicateur d’attribut personnalisé de requête HTTP et transmettez le nom de l’en-tête http.</span><span class="sxs-lookup"><span data-stu-id="1783c-108">Use the HTTP\_QUERY\_CUSTOM attribute flag and pass the name of the HTTP header.</span></span>

<span data-ttu-id="1783c-109">L’utilisation de la constante associée à l’en-tête HTTP dont votre application a besoin est plus rapide en interne, mais il peut y avoir des en-têtes HTTP qui ne sont pas associés à une constante.</span><span class="sxs-lookup"><span data-stu-id="1783c-109">Using the constant associated with the HTTP header that your application needs is faster internally, but there might be HTTP headers that do not have a constant associated with them.</span></span> <span data-ttu-id="1783c-110">Dans ce cas, la méthode utilisant l' \_ indicateur d' \_ attribut personnalisé de requête HTTP est disponible.</span><span class="sxs-lookup"><span data-stu-id="1783c-110">For those cases, the method using the HTTP\_QUERY\_CUSTOM attribute flag is available.</span></span>

<span data-ttu-id="1783c-111">Les deux méthodes utilisent la fonction [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) .</span><span class="sxs-lookup"><span data-stu-id="1783c-111">Both methods use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function.</span></span> <span data-ttu-id="1783c-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) prend le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) sur lequel la requête HTTP a été effectuée, un attribut, une mémoire tampon, une valeur DWORD qui contient la taille de la mémoire tampon et une valeur d’index.</span><span class="sxs-lookup"><span data-stu-id="1783c-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle on which the HTTP request was made, one attribute, a buffer, a DWORD value that contains the buffer size, and an index value.</span></span> <span data-ttu-id="1783c-113">Un modificateur peut également être ajouté à l’attribut passé à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) pour indiquer dans quel format les données doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="1783c-113">A modifier can also be added to the attribute passed to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to indicate in what format the data should be returned.</span></span>

### <a name="retrieving-headers-using-a-constant"></a><span data-ttu-id="1783c-114">Récupération des en-têtes à l’aide d’une constante</span><span class="sxs-lookup"><span data-stu-id="1783c-114">Retrieving Headers Using a Constant</span></span>

<span data-ttu-id="1783c-115">Pour utiliser la fonction [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) pour récupérer un en-tête http à l’aide d’une constante, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1783c-115">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using a constant, follow these steps:</span></span>

1.  <span data-ttu-id="1783c-116">Appelez [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) avec une constante de la liste d' [**attributs**](query-info-flags.md) , une mémoire tampon **null** et la variable qui contient la taille de la mémoire tampon définie à zéro.</span><span class="sxs-lookup"><span data-stu-id="1783c-116">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with a constant from the [**Attributes**](query-info-flags.md) list, a **NULL** buffer, and the variable that holds the buffer size set to zero.</span></span> <span data-ttu-id="1783c-117">En outre, si votre application a besoin des données dans un format particulier, vous pouvez ajouter une constante à partir de la liste des [**modificateurs**](query-info-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="1783c-117">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
2.  <span data-ttu-id="1783c-118">Si l’en-tête HTTP demandé existe, l’appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) doit échouer, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) doit retourner une erreur de \_ mémoire tampon insuffisante \_ et la variable transmise pour le paramètre *lpdwBufferLength* doit être définie sur le nombre d’octets requis.</span><span class="sxs-lookup"><span data-stu-id="1783c-118">If the requested HTTP header exists, the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) should fail, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) should return ERROR\_INSUFFICIENT\_BUFFER, and the variable passed for the *lpdwBufferLength* parameter should be set to the number of bytes required.</span></span>
3.  <span data-ttu-id="1783c-119">Allouez une mémoire tampon avec le nombre d’octets requis.</span><span class="sxs-lookup"><span data-stu-id="1783c-119">Allocate a buffer with the number of bytes required.</span></span>
4.  <span data-ttu-id="1783c-120">Réessayez l’appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span><span class="sxs-lookup"><span data-stu-id="1783c-120">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="1783c-121">L’exemple suivant illustre un appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) à l’aide de la \_ \_ constante d’en-têtes bruts de requête HTTP \_ \_ CRLF, qui est une valeur spéciale qui demande tous les en-têtes http retournés.</span><span class="sxs-lookup"><span data-stu-id="1783c-121">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_RAW\_HEADERS\_CRLF constant, which is a special value that requests all of the returned HTTP headers.</span></span>


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



### <a name="retrieving-headers-using-http_query_custom"></a><span data-ttu-id="1783c-122">Récupération des en-têtes à l’aide d’une \_ requête HTTP \_ personnalisée</span><span class="sxs-lookup"><span data-stu-id="1783c-122">Retrieving Headers Using HTTP\_QUERY\_CUSTOM</span></span>

<span data-ttu-id="1783c-123">Pour utiliser la fonction [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) pour récupérer un en-tête http à l’aide d’une \_ requête HTTP \_ personnalisée, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1783c-123">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using HTTP\_QUERY\_CUSTOM, follow these steps:</span></span>

1.  <span data-ttu-id="1783c-124">Allouez une mémoire tampon suffisamment grande pour contenir le nom de chaîne de l’en-tête HTTP.</span><span class="sxs-lookup"><span data-stu-id="1783c-124">Allocate a buffer that is large enough to hold the string name of the HTTP header.</span></span>
2.  <span data-ttu-id="1783c-125">Écrivez le nom de chaîne de l’en-tête HTTP dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1783c-125">Write the string name of the HTTP header into the buffer.</span></span>
3.  <span data-ttu-id="1783c-126">Appelez [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) avec une \_ requête HTTP \_ personnalisée, la mémoire tampon qui contient le nom de chaîne de l’en-tête http et la variable qui contient la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1783c-126">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with HTTP\_QUERY\_CUSTOM, the buffer that contains the string name of the HTTP header, and the variable that holds the buffer size.</span></span> <span data-ttu-id="1783c-127">En outre, si votre application a besoin des données dans un format particulier, vous pouvez ajouter une constante à partir de la liste des [**modificateurs**](query-info-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="1783c-127">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
4.  <span data-ttu-id="1783c-128">Si l’appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) échoue et que [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne \_ une erreur de mémoire tampon insuffisante \_ , réaffectez une mémoire tampon avec le nombre d’octets requis.</span><span class="sxs-lookup"><span data-stu-id="1783c-128">If the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, reallocate a buffer with the number of bytes required.</span></span>
5.  <span data-ttu-id="1783c-129">Réécrivez le nom de la chaîne de l’en-tête HTTP dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1783c-129">Write the string name of the HTTP header into the buffer again.</span></span>
6.  <span data-ttu-id="1783c-130">Réessayez l’appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span><span class="sxs-lookup"><span data-stu-id="1783c-130">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="1783c-131">L’exemple suivant illustre un appel à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) à l’aide de la \_ \_ constante personnalisée de requête HTTP pour demander l’en-tête HTTP Content-type.</span><span class="sxs-lookup"><span data-stu-id="1783c-131">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_CUSTOM constant to request the Content-Type HTTP header.</span></span>


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
> <span data-ttu-id="1783c-132">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="1783c-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="1783c-133">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="1783c-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="1783c-134">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="1783c-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 