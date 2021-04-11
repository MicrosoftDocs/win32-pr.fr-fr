---
description: Une URL est une représentation compacte de l’emplacement et de la méthode d’accès d’une ressource située sur Internet.
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: URL (Uniform Resource Locators) dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ed3b17e2cf205f6ac815e87617a84e0ccc4cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034316"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a><span data-ttu-id="7c8d2-103">URL (Uniform Resource Locators) dans WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7c8d2-103">Uniform Resource Locators (URLs) in WinHTTP</span></span>

<span data-ttu-id="7c8d2-104">Une URL est une représentation compacte de l’emplacement et de la méthode d’accès d’une ressource située sur Internet.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-104">A URL is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="7c8d2-105">Chaque URL se compose d’un schéma (HTTP, HTTPs, FTP ou Gopher) et d’une chaîne spécifique au schéma.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-105">Each URL consists of a scheme (HTTP, HTTPS, FTP, or Gopher) and a scheme-specific string.</span></span> <span data-ttu-id="7c8d2-106">Cette chaîne peut également inclure une combinaison d’un chemin d’accès de répertoire, d’une chaîne de recherche ou d’un nom de ressource.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="7c8d2-107">Les fonctions des services HTTP Microsoft Windows (WinHTTP) offrent la possibilité de créer, combiner, décomposer et rendre canoniques les URL.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-107">The Microsoft Windows HTTP Services (WinHTTP) functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="7c8d2-108">Pour plus d’informations, consultez [rfc 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) et [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (Uri) : Generic Syntax](https://www.ietf.org/rfc/rfc1738.txt).</span><span class="sxs-lookup"><span data-stu-id="7c8d2-108">For more information, see [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) and [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (URI): Generic Syntax](https://www.ietf.org/rfc/rfc1738.txt).</span></span>

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="7c8d2-109">Qu’est-ce qu’une URL canonique ?</span><span class="sxs-lookup"><span data-stu-id="7c8d2-109">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="7c8d2-110">La syntaxe et la sémantique des URL spécifiées laissent de l’espace pour la variation et l’erreur.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-110">The specified syntax and semantics of URLs leaves room for variation and error.</span></span> <span data-ttu-id="7c8d2-111">La canonicalisation est le processus qui consiste à normaliser une URL réelle dans un format correct, standard, « canonique ».</span><span class="sxs-lookup"><span data-stu-id="7c8d2-111">Canonicalization is the process of normalizing an actual URL into a correct, standard, "canonical" form.</span></span>

<span data-ttu-id="7c8d2-112">Cela implique de coder certains caractères comme des « séquences d’échappement ».</span><span class="sxs-lookup"><span data-stu-id="7c8d2-112">This involves coding some characters as "escape sequences."</span></span> <span data-ttu-id="7c8d2-113">Les caractères alphanumériques US-ASCII n’ont pas besoin d’être encodés (les chiffres 0-9, les lettres majuscules A-Z et les lettres minuscules de a à z).</span><span class="sxs-lookup"><span data-stu-id="7c8d2-113">Alphanumeric US-ASCII characters need not be encoded (the digits 0-9, the capital letters A-Z, and the lowercase letters a-z).</span></span> <span data-ttu-id="7c8d2-114">La plupart des autres caractères doivent être placés dans une séquence d’échappement, y compris les caractères de contrôle, l’espace, le signe de pourcentage, les « caractères non sécurisés » (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] et') et tous les caractères avec un point de code supérieur à 127.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-114">Most other characters must be escaped, including control characters, the space character, the percent sign, "unsafe characters" ( <, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ' ), and all characters with a code point above 127.</span></span>

## <a name="using-the-winhttp-functions-to-handle-urls"></a><span data-ttu-id="7c8d2-115">Utilisation des fonctions WinHTTP pour gérer les URL</span><span class="sxs-lookup"><span data-stu-id="7c8d2-115">Using the WinHTTP Functions to Handle URLs</span></span>

<span data-ttu-id="7c8d2-116">WinHTTP fournit deux fonctions pour la gestion des URL.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-116">WinHTTP provides two functions for handling URLs.</span></span> <span data-ttu-id="7c8d2-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) sépare une URL en ses composants et [**WINHTTPCREATEURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) crée une URL à partir de composants.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separates a URL into its component parts, and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) creates a URL from components.</span></span>

### <a name="separating-urls"></a><span data-ttu-id="7c8d2-118">Séparation des URL</span><span class="sxs-lookup"><span data-stu-id="7c8d2-118">Separating URLs</span></span>

<span data-ttu-id="7c8d2-119">La fonction [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) sépare une URL en ses composants et retourne les composants indiqués par la structure [**de \_ composants URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) qui est transmise à la fonction.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-119">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure that is passed to the function.</span></span>

<span data-ttu-id="7c8d2-120">Les composants qui composent la structure des [**\_ composants d’URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) sont le numéro de schéma, le nom d’hôte, le numéro de port, le nom d’utilisateur, le mot de passe, le chemin d’URL et des informations supplémentaires, telles que les paramètres de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-120">The components that make up the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure are the scheme number, host name, port number, user name, password, URL path, and additional information such as search parameters.</span></span> <span data-ttu-id="7c8d2-121">Chaque composant, sauf le schéma et le numéro de port, a un membre de chaîne qui contient les informations et un membre qui contient la longueur du membre de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-121">Each component, except the scheme and port numbers, has a string member that holds the information and a member that holds the length of the string member.</span></span> <span data-ttu-id="7c8d2-122">Le schéma et les numéros de port ont uniquement un membre qui stocke la valeur correspondante ; le schéma et le numéro de port sont tous deux renvoyés sur tous les appels réussis à [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span><span class="sxs-lookup"><span data-stu-id="7c8d2-122">The scheme and port numbers have only a member that stores the corresponding value; both the scheme and port numbers are returned on all successful calls to [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span></span>

<span data-ttu-id="7c8d2-123">Pour récupérer la valeur d’un composant particulier dans la structure de [**\_ composants d’URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , le membre qui stocke la longueur de chaîne de ce composant doit être défini sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-123">To retrieve the value of a particular component in the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="7c8d2-124">Le membre de chaîne peut être un pointeur vers une mémoire tampon ou **null**.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-124">The string member can be either a pointer to a buffer or **NULL**.</span></span>

<span data-ttu-id="7c8d2-125">Si le membre de pointeur contient un pointeur vers une mémoire tampon, le membre de longueur de chaîne doit contenir la taille de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-125">If the pointer member contains a pointer to a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="7c8d2-126">La fonction [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) retourne les informations de composant sous la forme d’une chaîne dans la mémoire tampon et stocke la longueur de chaîne dans le membre de longueur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-126">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="7c8d2-127">Si le membre de pointeur a la valeur **null**, le membre de longueur de chaîne peut être défini sur n’importe quelle valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-127">If the pointer member is set to **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="7c8d2-128">La fonction [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) stocke un pointeur vers le premier caractère de la chaîne d’URL qui contient les informations sur le composant et définit la longueur de chaîne sur le nombre de caractères dans la partie restante de la chaîne d’URL qui se rapporte au composant.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-128">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function stores a pointer to the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="7c8d2-129">Tous les membres de pointeur ayant la valeur **null** avec un membre de longueur différente de zéro pointent vers le point de départ approprié dans la chaîne d’URL.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-129">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="7c8d2-130">La longueur stockée dans le membre de longueur doit être utilisée pour déterminer la fin des informations du composant individuel.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-130">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="7c8d2-131">Pour terminer l’initialisation de la structure des [**\_ composants d’URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) correctement, le membre **dwStructSize** doit être défini sur la taille de la structure des [**\_ composants d’URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) .</span><span class="sxs-lookup"><span data-stu-id="7c8d2-131">To finish initializing the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure.</span></span>

### <a name="creating-urls"></a><span data-ttu-id="7c8d2-132">Création d’URL</span><span class="sxs-lookup"><span data-stu-id="7c8d2-132">Creating URLs</span></span>

<span data-ttu-id="7c8d2-133">La fonction [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) utilise les informations de la structure de [**\_ composants URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) décrite précédemment pour créer une URL.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-133">The [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) function uses the information in the previously described [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure to create a URL.</span></span>

<span data-ttu-id="7c8d2-134">Pour chaque composant requis, le membre pointeur doit contenir un pointeur vers la mémoire tampon qui contient les informations.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-134">For each required component, the pointer member should contain a pointer to the buffer that holds the information.</span></span> <span data-ttu-id="7c8d2-135">Le membre de longueur doit avoir la valeur zéro si le membre pointeur contient un pointeur vers une chaîne se terminant par zéro ; le membre de longueur doit être défini sur la longueur de chaîne si le membre pointeur contient un pointeur vers une chaîne qui n’est pas terminée par zéro.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-135">The length member should be set to zero if the pointer member contains a pointer to a zero-terminated string; the length member should be set to the string length if the pointer member contains a pointer to a string that is not zero-terminated.</span></span> <span data-ttu-id="7c8d2-136">Le membre pointeur de tous les composants qui ne sont pas requis doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-136">The pointer member of any components that are not required must be set to **NULL**.</span></span>

### <a name="sample-code"></a><span data-ttu-id="7c8d2-137">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="7c8d2-137">Sample code</span></span>

<span data-ttu-id="7c8d2-138">L’exemple de code suivant montre comment utiliser [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) et [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) pour désassembler une URL existante, modifier l’un de ses composants et le réassembler en une nouvelle URL.</span><span class="sxs-lookup"><span data-stu-id="7c8d2-138">The following sample code shows how to use the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) to disassemble an existing URL, modify one of its components, and reassemble it into a new URL.</span></span>


```C++
  URL_COMPONENTS urlComp;
  LPCWSTR pwszUrl1 = 
    L"https://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
  DWORD dwUrlLen = 0;

  // Initialize the URL_COMPONENTS structure.
  ZeroMemory(&urlComp, sizeof(urlComp));
  urlComp.dwStructSize = sizeof(urlComp);

  // Set required component lengths to non-zero so that they are cracked.
  urlComp.dwSchemeLength    = (DWORD)-1;
  urlComp.dwHostNameLength  = (DWORD)-1;
  urlComp.dwUrlPathLength   = (DWORD)-1;
  urlComp.dwExtraInfoLength = (DWORD)-1;

  // Crack the URL.
  if( !WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &urlComp ) )
      printf( "Error %u in WinHttpCrackUrl.\n", GetLastError( ) );
  else
  {
    // Change the search information.  New info is the same length.
    urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

    // Obtain the size of the new URL and allocate memory.
    WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen );
    LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

    // Create a new URL.
    if( !WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen ) )
      printf( "Error %u in WinHttpCreateUrl.\n", GetLastError( ) );
    else
    {
      // Show both URLs.
      printf( "Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2 );
    }

    // Free allocated memory.
    delete [] pwszUrl2;
  }
```



 

 



