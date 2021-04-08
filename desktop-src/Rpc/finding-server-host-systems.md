---
title: Recherche de systèmes hôtes serveur
description: Recherche de systèmes hôtes de serveur à l’aide de liaisons de chaîne et en interrogeant une base de données de service de noms pour l’emplacement d’un programme serveur.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840182"
---
# <a name="finding-server-host-systems"></a><span data-ttu-id="5447d-103">Recherche de systèmes hôtes serveur</span><span class="sxs-lookup"><span data-stu-id="5447d-103">Finding Server Host Systems</span></span>

<span data-ttu-id="5447d-104">Un système hôte serveur est l’ordinateur qui exécute le programme serveur de l’application distribuée.</span><span class="sxs-lookup"><span data-stu-id="5447d-104">A server host system is the computer that executes the distributed application's server program.</span></span> <span data-ttu-id="5447d-105">Il peut y avoir un ou plusieurs systèmes hôtes serveur sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="5447d-105">There may be one or many server host systems on a network.</span></span> <span data-ttu-id="5447d-106">La façon dont votre programme client trouve un serveur auquel se connecter dépend des besoins de votre programme.</span><span class="sxs-lookup"><span data-stu-id="5447d-106">How your client program finds a server to connect to depends on the needs of your program.</span></span>

<span data-ttu-id="5447d-107">Il existe deux méthodes pour rechercher des systèmes hôtes serveur :</span><span class="sxs-lookup"><span data-stu-id="5447d-107">There are two methods of finding server host systems:</span></span>

-   <span data-ttu-id="5447d-108">Utilisation des informations stockées dans les chaînes du code source du client, des variables d’environnement ou des fichiers de configuration spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="5447d-108">Using information stored in strings in the client source code, environment variables, or application-specific configuration files.</span></span> <span data-ttu-id="5447d-109">Votre application cliente peut utiliser les données de la chaîne pour composer une liaison entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="5447d-109">Your client application can use the data in the string to compose a binding between the client and the server.</span></span>
-   <span data-ttu-id="5447d-110">Interrogation d’une base de données de service de noms pour l’emplacement d’un programme serveur.</span><span class="sxs-lookup"><span data-stu-id="5447d-110">Querying a name service database for the location of a server program.</span></span>

<span data-ttu-id="5447d-111">Cette section fournit des informations sur ces deux techniques dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5447d-111">This section presents information on both of these techniques in the following topics:</span></span>

-   [<span data-ttu-id="5447d-112">Utilisation des liaisons de chaînes</span><span class="sxs-lookup"><span data-stu-id="5447d-112">Using String Bindings</span></span>](#using-string-bindings)
-   [<span data-ttu-id="5447d-113">Importation à partir des bases de données de service de noms</span><span class="sxs-lookup"><span data-stu-id="5447d-113">Importing from Name Service Databases</span></span>](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a><span data-ttu-id="5447d-114">Utilisation des liaisons de chaînes</span><span class="sxs-lookup"><span data-stu-id="5447d-114">Using String Bindings</span></span>

<span data-ttu-id="5447d-115">Les applications peuvent créer des liaisons à partir d’informations stockées dans des chaînes.</span><span class="sxs-lookup"><span data-stu-id="5447d-115">Applications can create bindings from information stored in strings.</span></span> <span data-ttu-id="5447d-116">Votre application cliente compose ces informations sous forme de chaîne, puis appelle la fonction [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) .</span><span class="sxs-lookup"><span data-stu-id="5447d-116">Your client application composes this information as a string, then calls the [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) function.</span></span> <span data-ttu-id="5447d-117">Le client doit fournir les informations suivantes pour identifier le serveur :</span><span class="sxs-lookup"><span data-stu-id="5447d-117">The client must supply the following information to identify the server:</span></span>

-   <span data-ttu-id="5447d-118">Nom de l’interface, identificateur global unique (GUID) de l’objet ou UUID de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5447d-118">The interface name, the globally unique identifier (GUID) of the object, or UUID of the object.</span></span> <span data-ttu-id="5447d-119">Pour plus d’informations, consultez [génération d’UUID d’interface](generating-interface-uuids.md) et de [chaîne UUID](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="5447d-119">For more information, see [Generating Interface UUIDs](generating-interface-uuids.md) and [String UUID](string-uuid.md).</span></span>
-   <span data-ttu-id="5447d-120">Type de transport sur lequel communiquer, par exemple les canaux nommés ou TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="5447d-120">The transport type to communicate over, such as named pipes or TCP/IP.</span></span> <span data-ttu-id="5447d-121">Pour plus d’informations, consultez [terminologie de liaison RPC essentielle](essential-rpc-binding-terminology.md) et [sélection d’une séquence de protocole](selecting-a-protocol-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="5447d-121">For details, see [Essential RPC Binding Terminology](essential-rpc-binding-terminology.md) and [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md).</span></span>
-   <span data-ttu-id="5447d-122">Adresse réseau ou nom de l’ordinateur hôte du serveur.</span><span class="sxs-lookup"><span data-stu-id="5447d-122">The network address or the name of the server host computer.</span></span>
-   <span data-ttu-id="5447d-123">Le point de terminaison du programme serveur sur l’ordinateur hôte du serveur.</span><span class="sxs-lookup"><span data-stu-id="5447d-123">The endpoint of the server program on the server host computer.</span></span> <span data-ttu-id="5447d-124">Pour plus d’informations, consultez [recherche de points de terminaison](finding-endpoints.md)et spécification des points de [terminaison](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="5447d-124">For more information, see [Finding Endpoints](finding-endpoints.md), and [Specifying Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="5447d-125">(L’UUID de l’objet et les informations sur le point de terminaison sont facultatifs.)</span><span class="sxs-lookup"><span data-stu-id="5447d-125">(The object UUID and the endpoint information are optional.)</span></span>

<span data-ttu-id="5447d-126">Dans les exemples suivants, le paramètre *pszNetworkAddress* et d’autres paramètres incluent des barres obliques inverses incorporées.</span><span class="sxs-lookup"><span data-stu-id="5447d-126">In the following examples, the *pszNetworkAddress* parameter and other parameters include embedded backslashes.</span></span> <span data-ttu-id="5447d-127">La barre oblique inverse est un caractère d’échappement dans le langage de programmation C.</span><span class="sxs-lookup"><span data-stu-id="5447d-127">The backslash is an escape character in the C programming language.</span></span> <span data-ttu-id="5447d-128">Deux barres obliques inverses sont nécessaires pour représenter chaque caractère barre oblique inverse d’un littéral.</span><span class="sxs-lookup"><span data-stu-id="5447d-128">Two backslashes are needed to represent each single literal backslash character.</span></span> <span data-ttu-id="5447d-129">La structure de liaison de chaîne doit contenir quatre barres obliques inverses pour représenter les deux barres obliques inverses littérales qui précèdent le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="5447d-129">The string-binding structure must contain four backslash characters to represent the two literal backslash characters that precede the server name.</span></span>

<span data-ttu-id="5447d-130">L’exemple suivant montre que le nom du serveur doit être précédé de huit barres obliques inverses afin que quatre barres obliques inverses littérales apparaissent dans la structure de données de liaison de chaîne après que la fonction **sprintf \_ s** a traité la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5447d-130">The following example shows that the server name must be preceded by eight backslashes so that four literal backslash characters will appear in the string-binding data structure after the **sprintf\_s** function processes the string.</span></span>


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



<span data-ttu-id="5447d-131">Dans l’exemple suivant, la liaison de chaîne se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="5447d-131">In the following example, the string binding appears as:</span></span>

<span data-ttu-id="5447d-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP : \\ \\ \\ \\ *nom_serveur* \[ \\ \\ canal \\ \\ *pipeName*\]</span><span class="sxs-lookup"><span data-stu-id="5447d-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np:\\\\\\\\*servername*\[\\\\pipe\\\\*pipename*\]</span></span>

<span data-ttu-id="5447d-133">Le client appelle ensuite [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) pour obtenir le handle de liaison :</span><span class="sxs-lookup"><span data-stu-id="5447d-133">The client then calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain the binding handle:</span></span>


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



<span data-ttu-id="5447d-134">Une fonction pratique, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assemble l’UUID d’objet, la séquence de protocole, l’adresse réseau et le point de terminaison dans la syntaxe correcte pour l’appel à [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span><span class="sxs-lookup"><span data-stu-id="5447d-134">A convenience function, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assembles the object UUID, protocol sequence, network address, and endpoint in the correct syntax for the call to [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span></span> <span data-ttu-id="5447d-135">Vous n’avez pas à vous soucier de l’insertion de l’esperluette, du signe deux-points et des différents composants de chaque séquence de protocole au bon endroit. il vous suffit de fournir les chaînes en tant que paramètres à la fonction.</span><span class="sxs-lookup"><span data-stu-id="5447d-135">You do not have to worry about putting the ampersand, colon, and the various components for each protocol sequence in the right place; you just supply the strings as parameters to the function.</span></span> <span data-ttu-id="5447d-136">La bibliothèque Runtime alloue même la mémoire nécessaire pour la liaison de chaîne.</span><span class="sxs-lookup"><span data-stu-id="5447d-136">The run-time library even allocates the memory needed for the string binding.</span></span>


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



<span data-ttu-id="5447d-137">Une autre fonction pratique, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), prend un handle de liaison comme entrée et génère la liaison de chaîne correspondante.</span><span class="sxs-lookup"><span data-stu-id="5447d-137">Another convenience function, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), takes a binding handle as input and produces the corresponding string binding.</span></span>

## <a name="importing-from-name-service-databases"></a><span data-ttu-id="5447d-138">Importation à partir des bases de données de service de noms</span><span class="sxs-lookup"><span data-stu-id="5447d-138">Importing from Name Service Databases</span></span>

<span data-ttu-id="5447d-139">Les bases de données de service de noms stockent, entre autres choses, des handles de liaison et des UUID.</span><span class="sxs-lookup"><span data-stu-id="5447d-139">Name service databases store, among other things, binding handles and UUIDs.</span></span> <span data-ttu-id="5447d-140">Votre application cliente peut Rechercher l’un ou l’autre ou les deux lorsqu’il doit effectuer une liaison avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="5447d-140">Your client application can search for either or both of these when it needs to bind to the server.</span></span> <span data-ttu-id="5447d-141">Pour en savoir plus sur les informations stockées par un service de noms et le format de stockage, consultez [la base de données du service de noms RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="5447d-141">For a discussion of the information that a name service stores, and the storage format, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="5447d-142">La bibliothèque RPC fournit deux ensembles de fonctions que votre programme client peut utiliser pour rechercher la base de données de service de noms.</span><span class="sxs-lookup"><span data-stu-id="5447d-142">The RPC library provides two sets of functions that your client program can use to search the name service database.</span></span> <span data-ttu-id="5447d-143">Les noms d’un jeu commencent par RpcNsBindingImport.</span><span class="sxs-lookup"><span data-stu-id="5447d-143">The names of one set begin with RpcNsBindingImport.</span></span> <span data-ttu-id="5447d-144">Les noms de l’autre jeu commencent par RpcNsBindingLookup.</span><span class="sxs-lookup"><span data-stu-id="5447d-144">The names of the other set begin with RpcNsBindingLookup.</span></span> <span data-ttu-id="5447d-145">La différence entre les deux groupes de fonctions est que les fonctions RpcNsBindingImport retournent un seul handle de liaison par appel et que les fonctions RpcNsBindingLookup retournent des groupes de handles par appel.</span><span class="sxs-lookup"><span data-stu-id="5447d-145">The difference between the two groups of functions is that the RpcNsBindingImport functions return a single binding handle per call and the RpcNsBindingLookup functions return groups of handles per call.</span></span>

<span data-ttu-id="5447d-146">Pour commencer une recherche avec les fonctions RpcNsBindingImport, appelez d’abord [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), comme indiqué dans le fragment de code suivant.</span><span class="sxs-lookup"><span data-stu-id="5447d-146">To begin a search with the RpcNsBindingImport functions, first call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), as shown in the following code fragment.</span></span>


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



<span data-ttu-id="5447d-147">Lorsque les fonctions RPC recherchent la base de données de service de noms, elles ont besoin d’un emplacement pour commencer la recherche.</span><span class="sxs-lookup"><span data-stu-id="5447d-147">When the RPC functions search the name service database, they need a place to begin the search.</span></span> <span data-ttu-id="5447d-148">Dans la terminologie RPC, il s’agit du nom de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="5447d-148">In RPC terminology, this is called the entry name.</span></span> <span data-ttu-id="5447d-149">Votre programme client transmet le nom de l’entrée en tant que deuxième paramètre à [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="5447d-149">Your client program passes the entry name as the second parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="5447d-150">Ce paramètre peut avoir la **valeur null** si vous souhaitez effectuer une recherche dans l’intégralité de la base de données du service de noms.</span><span class="sxs-lookup"><span data-stu-id="5447d-150">This parameter can be **NULL** if you want to search the entire name service database.</span></span> <span data-ttu-id="5447d-151">Vous pouvez également effectuer une recherche sur l’entrée de serveur en passant un nom d’entrée de serveur ou effectuer une recherche dans l’entrée de groupe en passant un nom d’entrée de groupe.</span><span class="sxs-lookup"><span data-stu-id="5447d-151">Alternatively, you can search the server entry by passing a server-entry name or search the group entry by passing a group-entry name.</span></span> <span data-ttu-id="5447d-152">Le passage d’un nom d’entrée restreint la recherche au contenu de cette entrée.</span><span class="sxs-lookup"><span data-stu-id="5447d-152">Passing an entry name restricts the search to the contents of that entry.</span></span>

<span data-ttu-id="5447d-153">Dans l’exemple précédent, la valeur \_ par défaut de la syntaxe RPC C \_ NS \_ \_ est passée comme premier paramètre à [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="5447d-153">In the preceding example, the value RPC\_C\_NS\_SYNTAX\_DEFAULT is passed as the first parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="5447d-154">Cela sélectionne la syntaxe du nom d’entrée par défaut.</span><span class="sxs-lookup"><span data-stu-id="5447d-154">This selects the default entry name syntax.</span></span> <span data-ttu-id="5447d-155">Actuellement, il s’agit de la seule syntaxe de nom d’entrée prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5447d-155">Currently, this is the only supported entry-name syntax.</span></span>

<span data-ttu-id="5447d-156">Votre application cliente peut rechercher un nom d’interface, un UUID ou les deux dans la base de données de service de noms.</span><span class="sxs-lookup"><span data-stu-id="5447d-156">Your client application can search the name service database for an interface name, a UUID, or both.</span></span> <span data-ttu-id="5447d-157">Si vous souhaitez qu’il recherche une interface par nom, transmettez la variable d’interface globale que le compilateur MIDL génère à partir de votre fichier IDL en tant que troisième paramètre de [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="5447d-157">If you want to have it search for an interface by name, pass the global interface variable that the MIDL compiler generates from your IDL file as the third parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="5447d-158">Vous trouverez sa déclaration dans le fichier d’en-tête généré par le compilateur MIDL lorsqu’il a généré le stub client.</span><span class="sxs-lookup"><span data-stu-id="5447d-158">You'll find its declaration in the header file that the MIDL compiler generated when it generated the client stub.</span></span> <span data-ttu-id="5447d-159">Si vous souhaitez que votre programme client recherche par UUID uniquement, définissez le troisième paramètre sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5447d-159">If you want your client program to search by UUID only, set the third parameter to **NULL**.</span></span>

<span data-ttu-id="5447d-160">Lors de la recherche d’un UUID dans la base de données de service de noms, définissez le quatrième paramètre de [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) sur l’UUID que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="5447d-160">When searching the name service database for a UUID, set the fourth parameter of [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) to the UUID that you want to search for.</span></span> <span data-ttu-id="5447d-161">Si vous ne recherchez pas d’UUID, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="5447d-161">If you are not searching for a UUID, set this parameter to **NULL**.</span></span>

<span data-ttu-id="5447d-162">La fonction [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) transmet l’adresse d’un handle de contexte de recherche de service de nom via son cinquième paramètre.</span><span class="sxs-lookup"><span data-stu-id="5447d-162">The [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) function passes the address of a name service–search context handle through its fifth parameter.</span></span> <span data-ttu-id="5447d-163">Vous transmettez ce paramètre à d’autres fonctions RpcNsBindingImport.</span><span class="sxs-lookup"><span data-stu-id="5447d-163">You pass this parameter to other RpcNsBindingImport functions.</span></span>

<span data-ttu-id="5447d-164">En particulier, la fonction suivante que votre application cliente appelle est [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span><span class="sxs-lookup"><span data-stu-id="5447d-164">In particular, the next function your client application would call is [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span> <span data-ttu-id="5447d-165">Les programmes clients utilisent cette fonction pour récupérer les descripteurs de liaison compatibles de la base de données du service de noms.</span><span class="sxs-lookup"><span data-stu-id="5447d-165">Client programs use this function to retrieve compatible binding handles from the name service database.</span></span> <span data-ttu-id="5447d-166">Le fragment de code suivant montre comment cette fonction peut être appelée :</span><span class="sxs-lookup"><span data-stu-id="5447d-166">The following code fragment demonstrates how this function might be called:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



<span data-ttu-id="5447d-167">Une fois que la fonction [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) a été appelée pour obtenir un handle de liaison, votre application cliente peut déterminer si le handle qu’elle a reçu est acceptable.</span><span class="sxs-lookup"><span data-stu-id="5447d-167">Once it has called the [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) function to obtain a binding handle, your client application can determine if the handle it received is acceptable.</span></span> <span data-ttu-id="5447d-168">Si ce n’est pas le cas, votre programme client peut exécuter une boucle et appeler à nouveau **RpcNsBindingImportNext** pour voir si le service de noms contient un handle plus approprié.</span><span class="sxs-lookup"><span data-stu-id="5447d-168">If not, your client program can execute a loop and call **RpcNsBindingImportNext** again to see if the name service contains a more appropriate handle.</span></span> <span data-ttu-id="5447d-169">Pour chaque appel à **RpcNsBindingImportNext**, il doit y avoir un appel correspondant à RpcNsBindingFree.</span><span class="sxs-lookup"><span data-stu-id="5447d-169">For each call to **RpcNsBindingImportNext**, there must be a corresponding call to RpcNsBindingFree.</span></span> <span data-ttu-id="5447d-170">Lorsque votre recherche est terminée, appelez la fonction [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) pour libérer le contexte de recherche.</span><span class="sxs-lookup"><span data-stu-id="5447d-170">When your search is complete, call the [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) function to free the lookup context.</span></span>

<span data-ttu-id="5447d-171">Une fois que votre application cliente a un handle de liaison acceptable, elle doit vérifier que l’application serveur est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5447d-171">After your client application has an acceptable binding handle, it should check to ensure that the server application is running.</span></span> <span data-ttu-id="5447d-172">Votre client peut utiliser deux méthodes pour effectuer cette vérification.</span><span class="sxs-lookup"><span data-stu-id="5447d-172">There are two methods your client can use to perform this verification.</span></span> <span data-ttu-id="5447d-173">La première consiste à appeler une fonction dans l’interface du client.</span><span class="sxs-lookup"><span data-stu-id="5447d-173">The first is to call a function in the client interface.</span></span> <span data-ttu-id="5447d-174">Si le programme serveur est en cours d’exécution, l’appel se termine.</span><span class="sxs-lookup"><span data-stu-id="5447d-174">If the server program is running, the call will complete.</span></span> <span data-ttu-id="5447d-175">Si ce n’est pas le cas, l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="5447d-175">If not, the call will fail.</span></span> <span data-ttu-id="5447d-176">Une meilleure façon de vérifier que le serveur est en cours d’exécution consiste à appeler [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), suivi d’un appel à [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span><span class="sxs-lookup"><span data-stu-id="5447d-176">A better way to verify that the server is running is to invoke [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), followed by a call to [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span></span> <span data-ttu-id="5447d-177">Pour plus d’informations sur la base de données du service de noms, consultez [la base de données du service de noms RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="5447d-177">For more information on the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

 

 




