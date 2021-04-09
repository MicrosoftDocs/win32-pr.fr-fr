---
title: Définition et récupération d’options Internet
description: Cette rubrique explique comment définir et récupérer des options Internet à l’aide des fonctions InternetSetOption et InternetQueryOption.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Définition et récupération d’options Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842602"
---
# <a name="setting-and-retrieving-internet-options"></a><span data-ttu-id="231a5-104">Définition et récupération d’options Internet</span><span class="sxs-lookup"><span data-stu-id="231a5-104">Setting and Retrieving Internet Options</span></span>

<span data-ttu-id="231a5-105">Cette rubrique explique comment définir et récupérer des options Internet à l’aide des fonctions [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) et [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .</span><span class="sxs-lookup"><span data-stu-id="231a5-105">This topic describes how to set and retrieve Internet options using the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) functions.</span></span>

<span data-ttu-id="231a5-106">Les options Internet peuvent être définies ou récupérées à partir d’un handle de [**HINTERNET**](appendix-a-hinternet-handles.md) spécifié ou des paramètres actuels dans Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="231a5-106">Internet options can be set on, or retrieved from, a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle or the current settings in Microsoft Internet Explorer.</span></span>

-   [<span data-ttu-id="231a5-107">Étapes d’implémentation</span><span class="sxs-lookup"><span data-stu-id="231a5-107">Implementation Steps</span></span>](#implementation-steps)
    -   [<span data-ttu-id="231a5-108">Choix des options Internet</span><span class="sxs-lookup"><span data-stu-id="231a5-108">Choosing Internet Options</span></span>](#choosing-internet-options)
    -   [<span data-ttu-id="231a5-109">Choix du handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="231a5-109">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
    -   [<span data-ttu-id="231a5-110">Définition ou récupération des options</span><span class="sxs-lookup"><span data-stu-id="231a5-110">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)
-   [<span data-ttu-id="231a5-111">Étendue du descripteur HINTERNET</span><span class="sxs-lookup"><span data-stu-id="231a5-111">Scope of HINTERNET Handle</span></span>](#scope-of-hinternet-handle)
-   [<span data-ttu-id="231a5-112">Définition des options individuelles</span><span class="sxs-lookup"><span data-stu-id="231a5-112">Setting Individual Options</span></span>](#setting-individual-options)
-   [<span data-ttu-id="231a5-113">Récupération d’options individuelles</span><span class="sxs-lookup"><span data-stu-id="231a5-113">Retrieving Individual Options</span></span>](#retrieving-individual-options)
    -   [<span data-ttu-id="231a5-114">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="231a5-114">Complete Sample</span></span>](#complete-sample)
-   [<span data-ttu-id="231a5-115">Définition des options de connexion</span><span class="sxs-lookup"><span data-stu-id="231a5-115">Setting Connection Options</span></span>](#setting-connection-options)
-   [<span data-ttu-id="231a5-116">Récupération des options de connexion</span><span class="sxs-lookup"><span data-stu-id="231a5-116">Retrieving Connection Options</span></span>](#retrieving-connection-options)
-   [<span data-ttu-id="231a5-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="231a5-117">Related topics</span></span>](#related-topics)

## <a name="implementation-steps"></a><span data-ttu-id="231a5-118">Étapes d’implémentation</span><span class="sxs-lookup"><span data-stu-id="231a5-118">Implementation Steps</span></span>

<span data-ttu-id="231a5-119">Pour définir ou récupérer des options Internet, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="231a5-119">To set or retrieve Internet options complete the following:</span></span>

-   [<span data-ttu-id="231a5-120">Choix des options Internet</span><span class="sxs-lookup"><span data-stu-id="231a5-120">Choosing Internet Options</span></span>](#choosing-internet-options)
-   [<span data-ttu-id="231a5-121">Choix du handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="231a5-121">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
-   [<span data-ttu-id="231a5-122">Définition ou récupération des options</span><span class="sxs-lookup"><span data-stu-id="231a5-122">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a><span data-ttu-id="231a5-123">Choix des options Internet</span><span class="sxs-lookup"><span data-stu-id="231a5-123">Choosing Internet Options</span></span>

<span data-ttu-id="231a5-124">Étant donné que de nombreuses options Internet sont disponibles, il est important de choisir les options appropriées.</span><span class="sxs-lookup"><span data-stu-id="231a5-124">Because there are so many Internet options, choosing the right options is important.</span></span> <span data-ttu-id="231a5-125">De nombreuses options Internet affectent le comportement des fonctions WinINet et d’Internet Explorer :</span><span class="sxs-lookup"><span data-stu-id="231a5-125">Many Internet options affect the behavior of the WinINet functions and Internet Explorer:</span></span>

<span data-ttu-id="231a5-126">Par exemple, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="231a5-126">For example, you can:</span></span>

-   <span data-ttu-id="231a5-127">Gérez l’authentification du serveur et du proxy de base en définissant les noms d’utilisateur et les mots de passe.</span><span class="sxs-lookup"><span data-stu-id="231a5-127">Handle basic server and proxy authentication by setting user names and passwords.</span></span>
-   <span data-ttu-id="231a5-128">Définissez ou récupérez la chaîne de l’agent utilisateur utilisée par les serveurs pour identifier les fonctionnalités de l’application cliente ou du navigateur.</span><span class="sxs-lookup"><span data-stu-id="231a5-128">Set or retrieve the user agent string used by servers to identify the features of the client application or browser.</span></span>
-   <span data-ttu-id="231a5-129">Récupère le type de handle du handle [**HINTERNET**](appendix-a-hinternet-handles.md) spécifié.</span><span class="sxs-lookup"><span data-stu-id="231a5-129">Retrieve the handle type of the specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="231a5-130">Pour plus d’informations et pour obtenir la liste des options Internet, consultez [**indicateurs d’option**](option-flags.md).</span><span class="sxs-lookup"><span data-stu-id="231a5-130">For more information and a list of the Internet options, see [**Option Flags**](option-flags.md).</span></span>

<span data-ttu-id="231a5-131">Dans Internet Explorer 5 et versions ultérieures, certaines options peuvent être définies ou récupérées à partir d’une connexion Internet spécifique à l’aide de la [**\_ \_ \_ \_ liste d’options Internet par**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) connexion et des structures d' [**\_ \_ \_ option Internet par Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="231a5-131">In Internet Explorer 5 and later, some options can be set or retrieved from a specific Internet connection using the [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) and [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span> <span data-ttu-id="231a5-132">Pour plus d’informations et pour obtenir la liste des options qui peuvent être définies ou récupérées à partir d’une connexion Internet spécifique, consultez le membre **dwOptions** de la structure d' [**\_ option Internet par \_ conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="231a5-132">For more information and a list of options that can be set or retrieved from a specific Internet connection, see the **dwOptions** member of the [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structure.</span></span>

### <a name="choosing-the-hinternet-handle"></a><span data-ttu-id="231a5-133">Choix du handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="231a5-133">Choosing the HINTERNET Handle</span></span>

<span data-ttu-id="231a5-134">Le handle [**HINTERNET**](appendix-a-hinternet-handles.md) utilisé pour définir ou récupérer les options Internet détermine l’étendue de l’opération.</span><span class="sxs-lookup"><span data-stu-id="231a5-134">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the scope of the operation.</span></span> <span data-ttu-id="231a5-135">Tous les descripteurs créés par le biais de ce descripteur hériteront des options définies sur ce descripteur.</span><span class="sxs-lookup"><span data-stu-id="231a5-135">All the handles created through this handle will inherit the options set on this handle.</span></span>

<span data-ttu-id="231a5-136">Par exemple, les applications clientes qui requièrent un proxy avec l’authentification n’ont probablement pas besoin de définir le nom d’utilisateur et le mot de passe du proxy chaque fois que l’application tente d’accéder à une ressource Internet.</span><span class="sxs-lookup"><span data-stu-id="231a5-136">For example, client applications that require a proxy with authentication, probably do not require setting the proxy user name and password every time the application attempts to access an Internet resource.</span></span> <span data-ttu-id="231a5-137">Si toutes les demandes sur une connexion donnée sont gérées par le même proxy, la définition du nom d’utilisateur et du mot de passe du proxy sur un handle de type de connexion [**HINTERNET**](appendix-a-hinternet-handles.md) , autrement dit un handle créé par un appel à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), permettrait à tous les appels dérivés de ce handle **HINTERNET** d’utiliser le même nom d’utilisateur et mot de passe proxy.</span><span class="sxs-lookup"><span data-stu-id="231a5-137">If all requests on a given connection are handled by the same proxy, setting the proxy user name and password on a connection type [**HINTERNET**](appendix-a-hinternet-handles.md) handle, that is, a handle created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), would allow any calls derived from this **HINTERNET** handle to use the same proxy user name and password.</span></span> <span data-ttu-id="231a5-138">La définition du nom d’utilisateur et du mot de passe du proxy chaque fois qu’un descripteur **HINTERNET** est créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) nécessiteraient une surcharge supplémentaire et inutile.</span><span class="sxs-lookup"><span data-stu-id="231a5-138">Setting the proxy user name and password every time an **HINTERNET** handle is created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) would require extra and unnecessary overhead.</span></span> <span data-ttu-id="231a5-139">Sachez que si l’application utilise un proxy qui nécessite une authentification, elle doit définir les informations d’identification de proxy sur chaque nouvelle connexion.</span><span class="sxs-lookup"><span data-stu-id="231a5-139">Be aware that if the application uses a proxy that requires authentication, it should set the proxy credentials on every new connection.</span></span>

### <a name="setting-or-retrieving-the-options"></a><span data-ttu-id="231a5-140">Définition ou récupération des options</span><span class="sxs-lookup"><span data-stu-id="231a5-140">Setting or Retrieving the Options</span></span>

<span data-ttu-id="231a5-141">Une fois que vous avez déterminé les options Internet et le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) à utiliser, récupérez ces options Internet.</span><span class="sxs-lookup"><span data-stu-id="231a5-141">When you have determined what Internet options and [**HINTERNET**](appendix-a-hinternet-handles.md) handle to use, retrieve those Internet options.</span></span> <span data-ttu-id="231a5-142">Pour définir ou récupérer des options, appelez [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="231a5-142">To set or retrieve options, call either [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

## <a name="scope-of-hinternet-handle"></a><span data-ttu-id="231a5-143">Étendue du descripteur HINTERNET</span><span class="sxs-lookup"><span data-stu-id="231a5-143">Scope of HINTERNET Handle</span></span>

<span data-ttu-id="231a5-144">Le handle [**HINTERNET**](appendix-a-hinternet-handles.md) utilisé pour définir ou récupérer les options Internet détermine les actions pour lesquelles les options sont valides.</span><span class="sxs-lookup"><span data-stu-id="231a5-144">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the actions for which the options are valid.</span></span>

<span data-ttu-id="231a5-145">Ces handles ont trois niveaux :</span><span class="sxs-lookup"><span data-stu-id="231a5-145">These handles have three levels:</span></span>

-   <span data-ttu-id="231a5-146">Le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) racine (créé par un appel à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) contient toutes les options Internet qui affectent cette instance de wininet.</span><span class="sxs-lookup"><span data-stu-id="231a5-146">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle (created by a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) would contain all the Internet options that affect this instance of WinINet.</span></span>
-   <span data-ttu-id="231a5-147">Handles [**HINTERNET**](appendix-a-hinternet-handles.md) qui se connectent à un serveur (créé par un appel à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span><span class="sxs-lookup"><span data-stu-id="231a5-147">[**HINTERNET**](appendix-a-hinternet-handles.md) handles that connect to a server (created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span></span>
-   <span data-ttu-id="231a5-148">[**HINTERNET**](appendix-a-hinternet-handles.md) Handles associés à une ressource ou une énumération de ressources sur un serveur particulier.</span><span class="sxs-lookup"><span data-stu-id="231a5-148">[**HINTERNET**](appendix-a-hinternet-handles.md) handles associated with a resource or enumeration of resources on a particular server.</span></span>

<span data-ttu-id="231a5-149">En plus des différents descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) , une application peut également utiliser la **valeur null** pour définir ou récupérer les valeurs par défaut des options Internet utilisées par Internet Explorer et les fonctions WinInet.</span><span class="sxs-lookup"><span data-stu-id="231a5-149">In addition to the various [**HINTERNET**](appendix-a-hinternet-handles.md) handles, an application can also use **NULL** to set or retrieve the default values of the Internet options used by Internet Explorer and the WinINet functions.</span></span> <span data-ttu-id="231a5-150">La définition des options Internet lors de l’utilisation de **null** comme handle modifie les valeurs par défaut des options, qui sont actuellement stockées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="231a5-150">Setting Internet options when using **NULL** as the handle changes the default values of the options, which are currently stored in the registry.</span></span> <span data-ttu-id="231a5-151">Les applications clientes ne doivent pas utiliser les fonctions de Registre pour modifier les valeurs par défaut des options Internet, car l’implémentation de la manière dont les options sont stockées peut être modifiée à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="231a5-151">Client applications should not use registry functions to change the default values of the Internet options, because the implementation of how the options are stored can be altered in the future.</span></span>

<span data-ttu-id="231a5-152">Le tableau suivant répertorie le type des descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) et l’étendue des options Internet qui leur sont associées.</span><span class="sxs-lookup"><span data-stu-id="231a5-152">The following table lists the type of [**HINTERNET**](appendix-a-hinternet-handles.md) handles and the scope of the Internet options associated with them.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="231a5-153">Type de handle</span><span class="sxs-lookup"><span data-stu-id="231a5-153">Handle Type</span></span></th>
<th><span data-ttu-id="231a5-154">Étendue</span><span class="sxs-lookup"><span data-stu-id="231a5-154">Scope</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="231a5-155"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="231a5-155"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="231a5-156">Paramètres d’option par défaut pour Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="231a5-156">The default option settings for Internet Explorer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="231a5-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span><span class="sxs-lookup"><span data-stu-id="231a5-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span></span></td>
<td><span data-ttu-id="231a5-158">Les paramètres d’option pour cette connexion à un serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="231a5-158">The option settings for this connection to an FTP server.</span></span> <span data-ttu-id="231a5-159">Ces options affectent les opérations lancées à partir de ce handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , telles que les téléchargements de fichiers.</span><span class="sxs-lookup"><span data-stu-id="231a5-159">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="231a5-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span><span class="sxs-lookup"><span data-stu-id="231a5-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span></span></td>
<td><span data-ttu-id="231a5-161">Les paramètres d’option pour cette connexion à un serveur Gopher.</span><span class="sxs-lookup"><span data-stu-id="231a5-161">The option settings for this connection to a Gopher server.</span></span> <span data-ttu-id="231a5-162">Ces options affectent les opérations lancées à partir de ce handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , telles que les téléchargements de fichiers.</span><span class="sxs-lookup"><span data-stu-id="231a5-162">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="231a5-163">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="231a5-163">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="231a5-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span><span class="sxs-lookup"><span data-stu-id="231a5-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span></span></td>
<td><span data-ttu-id="231a5-165">Les paramètres d’option pour cette connexion à un serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="231a5-165">The option settings for this connection to an HTTP server.</span></span> <span data-ttu-id="231a5-166">Ces options affectent les opérations lancées à partir de ce handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , telles que les téléchargements de fichiers.</span><span class="sxs-lookup"><span data-stu-id="231a5-166">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="231a5-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span><span class="sxs-lookup"><span data-stu-id="231a5-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span></span></td>
<td><span data-ttu-id="231a5-168">Paramètres d’option associés à cette demande de fichier.</span><span class="sxs-lookup"><span data-stu-id="231a5-168">The option settings associated with this file request.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="231a5-169">INTERNET_HANDLE_TYPE_FTP_FILE</span><span class="sxs-lookup"><span data-stu-id="231a5-169">INTERNET_HANDLE_TYPE_FTP_FILE</span></span></td>
<td><span data-ttu-id="231a5-170">Paramètres d’option associés à ce téléchargement de ressource FTP.</span><span class="sxs-lookup"><span data-stu-id="231a5-170">The option settings associated with this FTP resource download.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="231a5-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="231a5-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span></span></td>
<td><span data-ttu-id="231a5-172">Les paramètres d’option associés à ce téléchargement de ressource FTP au format HTML.</span><span class="sxs-lookup"><span data-stu-id="231a5-172">The option settings associated with this FTP resource download formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="231a5-173">INTERNET_HANDLE_TYPE_FTP_FIND</span><span class="sxs-lookup"><span data-stu-id="231a5-173">INTERNET_HANDLE_TYPE_FTP_FIND</span></span></td>
<td><span data-ttu-id="231a5-174">Paramètres d’option associés à cette recherche de fichiers sur un serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="231a5-174">The option settings associated with this search of files on an FTP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="231a5-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="231a5-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span></span></td>
<td><span data-ttu-id="231a5-176">Les paramètres d’option associés à cette recherche de fichiers sur un serveur FTP au format HTML.</span><span class="sxs-lookup"><span data-stu-id="231a5-176">The option settings associated with this search of files on an FTP server formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="231a5-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span><span class="sxs-lookup"><span data-stu-id="231a5-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span></span></td>
<td><span data-ttu-id="231a5-178">Les paramètres d’option associés à ce téléchargement de ressource Gopher.</span><span class="sxs-lookup"><span data-stu-id="231a5-178">The option settings associated with this Gopher resource download.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="231a5-179">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="231a5-179">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="231a5-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="231a5-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span></span></td>
<td><span data-ttu-id="231a5-181">Paramètres d’option associés à ce téléchargement de ressources Gopher au format HTML.</span><span class="sxs-lookup"><span data-stu-id="231a5-181">The option settings associated with this Gopher resource download formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="231a5-182">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="231a5-182">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="231a5-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span><span class="sxs-lookup"><span data-stu-id="231a5-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span></span></td>
<td><span data-ttu-id="231a5-184">Paramètres d’option associés à cette recherche de fichiers sur un serveur Gopher.</span><span class="sxs-lookup"><span data-stu-id="231a5-184">The option settings associated with this search of files on an Gopher server.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="231a5-185">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="231a5-185">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="231a5-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="231a5-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span></span></td>
<td><span data-ttu-id="231a5-187">Les paramètres d’option associés à cette recherche de fichiers sur un serveur Gopher au format HTML.</span><span class="sxs-lookup"><span data-stu-id="231a5-187">The option settings associated with this search of files on an Gopher server formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="231a5-188">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="231a5-188">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="231a5-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="231a5-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span></span></td>
<td><span data-ttu-id="231a5-190">Paramètres d’option associés à cette requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="231a5-190">The option settings associated with this HTTP request.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="231a5-191">INTERNET_HANDLE_TYPE_INTERNET</span><span class="sxs-lookup"><span data-stu-id="231a5-191">INTERNET_HANDLE_TYPE_INTERNET</span></span></td>
<td><span data-ttu-id="231a5-192">Les paramètres d’option associés à cette instance des fonctions WinINet.</span><span class="sxs-lookup"><span data-stu-id="231a5-192">The option settings associated with this instance of the WinINet functions.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a><span data-ttu-id="231a5-193">Définition des options individuelles</span><span class="sxs-lookup"><span data-stu-id="231a5-193">Setting Individual Options</span></span>

<span data-ttu-id="231a5-194">Après avoir déterminé les options Internet que vous souhaitez définir et l’étendue que vous souhaitez affecter par ces options, la définition des options Internet n’est pas compliquée.</span><span class="sxs-lookup"><span data-stu-id="231a5-194">After determining the Internet options you want to set and the scope you want affected by these options, setting Internet options is not complicated.</span></span> <span data-ttu-id="231a5-195">Il vous suffit d’appeler la fonction [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) avec le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) souhaité, l’indicateur d’option Internet et une mémoire tampon qui contient les informations que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="231a5-195">All you would need to do is call the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function with desired [**HINTERNET**](appendix-a-hinternet-handles.md) handle, Internet option flag, and a buffer that contains the information you want set.</span></span>

<span data-ttu-id="231a5-196">L’exemple suivant montre comment définir le nom d’utilisateur et le mot de passe du proxy sur un handle [**HINTERNET**](appendix-a-hinternet-handles.md) spécifié.</span><span class="sxs-lookup"><span data-stu-id="231a5-196">The following example shows how to set the proxy user name and password on a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>


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



## <a name="retrieving-individual-options"></a><span data-ttu-id="231a5-197">Récupération d’options individuelles</span><span class="sxs-lookup"><span data-stu-id="231a5-197">Retrieving Individual Options</span></span>

<span data-ttu-id="231a5-198">Les options Internet peuvent être récupérées à l’aide de la fonction [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .</span><span class="sxs-lookup"><span data-stu-id="231a5-198">Internet options can be retrieved using the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) function.</span></span> <span data-ttu-id="231a5-199">Pour récupérer les options Internet :</span><span class="sxs-lookup"><span data-stu-id="231a5-199">To retrieve Internet options:</span></span>

1.  <span data-ttu-id="231a5-200">Déterminez la taille de mémoire tampon nécessaire pour récupérer les informations sur les options Internet.</span><span class="sxs-lookup"><span data-stu-id="231a5-200">Determine the buffer size necessary to retrieve the Internet option information.</span></span>

    <span data-ttu-id="231a5-201">La taille de la mémoire tampon peut être déterminée à l’aide de **null** pour l’adresse de la mémoire tampon et en lui passant une taille de mémoire tampon de zéro.</span><span class="sxs-lookup"><span data-stu-id="231a5-201">The buffer size can be determined by using **NULL** for the address of the buffer and passing it a buffer size of zero.</span></span>

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    <span data-ttu-id="231a5-202">La valeur retournée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) est la quantité de mémoire nécessaire pour récupérer les informations, en octets.</span><span class="sxs-lookup"><span data-stu-id="231a5-202">The value returned by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) is the amount of memory required to retrieve the information, in bytes.</span></span>

2.  <span data-ttu-id="231a5-203">Allouez une mémoire pour la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="231a5-203">Allocate a memory for the buffer.</span></span>
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  <span data-ttu-id="231a5-204">Récupérez les données.</span><span class="sxs-lookup"><span data-stu-id="231a5-204">Retrieve the data.</span></span>
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  <span data-ttu-id="231a5-205">Libérez de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="231a5-205">Free the memory.</span></span>
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a><span data-ttu-id="231a5-206">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="231a5-206">Complete Sample</span></span>

<span data-ttu-id="231a5-207">Voici l’exemple complet utilisé dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="231a5-207">The following is the complete sample used in the previous section.</span></span> <span data-ttu-id="231a5-208">Cet exemple montre comment récupérer la chaîne de l’agent utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="231a5-208">This sample shows how to retrieve the default user agent string.</span></span>


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



## <a name="setting-connection-options"></a><span data-ttu-id="231a5-209">Définition des options de connexion</span><span class="sxs-lookup"><span data-stu-id="231a5-209">Setting Connection Options</span></span>

<span data-ttu-id="231a5-210">Dans Internet Explorer 5 et versions ultérieures, les options Internet peuvent être définies pour sur une connexion spécifique.</span><span class="sxs-lookup"><span data-stu-id="231a5-210">In Internet Explorer 5 and later, Internet options can be set for on a specific connection.</span></span> <span data-ttu-id="231a5-211">Auparavant, toutes les connexions partageaient les mêmes paramètres d’option Internet.</span><span class="sxs-lookup"><span data-stu-id="231a5-211">Previously, all connections shared the same Internet option settings.</span></span> <span data-ttu-id="231a5-212">Pour définir les options d’une connexion particulière :</span><span class="sxs-lookup"><span data-stu-id="231a5-212">To set options for a particular connection:</span></span>

1.  <span data-ttu-id="231a5-213">Créer une structure de [**\_ liste d’options Internet par \_ conn \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .</span><span class="sxs-lookup"><span data-stu-id="231a5-213">Create an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="231a5-214">Allouez la mémoire pour les options Internet individuelles que vous souhaitez définir pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="231a5-214">Allocate the memory for the individual Internet options that you want to set for the connection.</span></span>
3.  <span data-ttu-id="231a5-215">Définissez les options dans les structures d' [**\_ \_ \_ option Internet par Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="231a5-215">Set the options in [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="231a5-216">Définissez les options à l’aide de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="231a5-216">Set the options using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="231a5-217">L’exemple de code suivant montre comment définir des données de proxy pour une connexion LAN.</span><span class="sxs-lookup"><span data-stu-id="231a5-217">The following code example shows how to set proxy data for a LAN connection.</span></span>


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



## <a name="retrieving-connection-options"></a><span data-ttu-id="231a5-218">Récupération des options de connexion</span><span class="sxs-lookup"><span data-stu-id="231a5-218">Retrieving Connection Options</span></span>

<span data-ttu-id="231a5-219">Dans Internet Explorer 5 et versions ultérieures, les options Internet peuvent être récupérées à partir d’une connexion spécifique.</span><span class="sxs-lookup"><span data-stu-id="231a5-219">In Internet Explorer 5 and later, Internet options can be retrieved from a specific connection.</span></span> <span data-ttu-id="231a5-220">Pour récupérer les options d’une connexion particulière :</span><span class="sxs-lookup"><span data-stu-id="231a5-220">To retrieve options from a particular connection:</span></span>

1.  <span data-ttu-id="231a5-221">Créer une structure de [**\_ liste d’options Internet par \_ conn \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .</span><span class="sxs-lookup"><span data-stu-id="231a5-221">Create a [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="231a5-222">Allouez la mémoire pour les options Internet individuelles à récupérer à partir de la connexion.</span><span class="sxs-lookup"><span data-stu-id="231a5-222">Allocate the memory for the individual Internet options to retrieve from the connection.</span></span>
3.  <span data-ttu-id="231a5-223">Spécifiez les options à l’aide de structures d' [**\_ \_ \_ option Internet par Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="231a5-223">Specify the options using [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="231a5-224">Récupérez les options à l’aide de [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="231a5-224">Retrieve the options using [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>
5.  <span data-ttu-id="231a5-225">Utilisez les données d’option.</span><span class="sxs-lookup"><span data-stu-id="231a5-225">Utilize the option data.</span></span>
6.  <span data-ttu-id="231a5-226">Libérez la mémoire, allouée pour contenir les données d’option, à l’aide de la fonction [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="231a5-226">Free the memory, allocated to hold the option data, using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="231a5-227">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="231a5-227">WinINet does not support server implementations.</span></span> <span data-ttu-id="231a5-228">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="231a5-228">In addition, it should not be used from a service.</span></span> <span data-ttu-id="231a5-229">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="231a5-229">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="231a5-230">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="231a5-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="231a5-231">Gestion de l’authentification</span><span class="sxs-lookup"><span data-stu-id="231a5-231">Handling Authentication</span></span>](handling-authentication.md)
</dt> <dt>

[<span data-ttu-id="231a5-232">Handles HINTERNET</span><span class="sxs-lookup"><span data-stu-id="231a5-232">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
</dt> </dl>

 

