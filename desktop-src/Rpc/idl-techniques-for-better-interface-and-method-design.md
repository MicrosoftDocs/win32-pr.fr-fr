---
title: Techniques IDL pour une meilleure conception d’interface et de méthode
description: Envisagez d’utiliser les techniques spécifiques IDL suivantes pour améliorer la sécurité et les performances lorsque vous développez des interfaces et des méthodes RPC qui gèrent des données conformes et variants.
ms.assetid: 651bdb5c-ad56-4526-9b7d-7165141e7ceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b897d8d1f2f5e1c11a5328fb095341871e3689e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379861"
---
# <a name="idl-techniques-for-better-interface-and-method-design"></a><span data-ttu-id="89488-103">Techniques IDL pour une meilleure conception d’interface et de méthode</span><span class="sxs-lookup"><span data-stu-id="89488-103">IDL Techniques for Better Interface and Method Design</span></span>

<span data-ttu-id="89488-104">Envisagez d’utiliser les techniques spécifiques IDL suivantes pour améliorer la sécurité et les performances lorsque vous développez des interfaces et des méthodes RPC qui gèrent des données conformes et variants.</span><span class="sxs-lookup"><span data-stu-id="89488-104">Consider using the following IDL-specific techniques to improve security and performance when you are developing RPC interfaces and methods that handle both conformant and variant data.</span></span> <span data-ttu-id="89488-105">Les attributs référencés dans cette rubrique sont les attributs IDL définis sur les paramètres de méthode qui gèrent les données conformes (par exemple, les \[ attributs **size \_ is** \] et \[ **Max \_ is** \] ) ou des données variant (par exemple, la \[ **longueur \_ est** \] et les attributs de \[ **chaîne** \] ).</span><span class="sxs-lookup"><span data-stu-id="89488-105">The attributes referred to in this topic are the IDL attributes set on method parameters that handle either conformant data (for example, the \[**size\_is**\] and \[**max\_is**\] attributes) or variant data (for example, the \[**length\_is**\] and \[**string**\] attributes).</span></span>

## <a name="using-the-range-attribute-with-conformant-data-parameters"></a><span data-ttu-id="89488-106">Utilisation de \[ l' \] attribut Range avec des paramètres de données conformes</span><span class="sxs-lookup"><span data-stu-id="89488-106">Using the \[range\] Attribute with Conformant Data Parameters</span></span>

<span data-ttu-id="89488-107">L' \[  \] attribut Range indique au runtime RPC d’effectuer une validation de taille supplémentaire pendant le processus d’démarshaling de données.</span><span class="sxs-lookup"><span data-stu-id="89488-107">The \[**range**\] attribute instructs the RPC run-time to perform additional size validation during the data unmarshaling process.</span></span> <span data-ttu-id="89488-108">En particulier, il vérifie que la taille fournie des données passées en tant que paramètre associé est comprise dans la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89488-108">Specifically, it verifies that the supplied size of the data passed as the associated parameter is within the specified range.</span></span>

<span data-ttu-id="89488-109">L' \[ attribut de **plage** \] n’affecte pas le format de câble.</span><span class="sxs-lookup"><span data-stu-id="89488-109">The \[**range**\] attribute does not affect wire format.</span></span>

<span data-ttu-id="89488-110">Si la valeur du câble est en dehors de la plage autorisée, RPC lève une \_ exception RPC x \_ non valide \_ ou une exception de données de \_ \_ stub incorrecte \_ \_ RPC x.</span><span class="sxs-lookup"><span data-stu-id="89488-110">If the value on wire is outside of the allowed range, RPC will throw an RPC\_X\_INVALID\_BOUND or RPC\_X\_BAD\_STUB\_DATA exception.</span></span> <span data-ttu-id="89488-111">Cela fournit un niveau supplémentaire de validation des données et peut aider à éviter des erreurs de sécurité courantes telles que les dépassements de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="89488-111">This provides an additional level of data validation, and can help prevent common security errors like buffer overruns.</span></span> <span data-ttu-id="89488-112">De même, l’utilisation \[  \] de Range peut améliorer les performances de l’application, car les données conformes marquées avec elle ont des contraintes clairement définies à prendre en compte par le service RPC.</span><span class="sxs-lookup"><span data-stu-id="89488-112">Likewise, using \[**range**\] can improve application performance, since conformant data marked with it has clearly-defined constraints available for consideration by the RPC service.</span></span>

## <a name="rpc-server-stub-memory-management-rules"></a><span data-ttu-id="89488-113">Règles de gestion de la mémoire stub du serveur RPC</span><span class="sxs-lookup"><span data-stu-id="89488-113">RPC Server Stub Memory Management Rules</span></span>

<span data-ttu-id="89488-114">Il est important de comprendre les règles de gestion de mémoire stub du serveur RPC lors de la création des fichiers IDL pour une application prenant en charge RPC.</span><span class="sxs-lookup"><span data-stu-id="89488-114">It is important to understand RPC server stub memory management rules when creating the IDL files for an RPC-enabled application.</span></span> <span data-ttu-id="89488-115">Les applications peuvent améliorer l’utilisation des ressources du serveur à l’aide \[  \] de Range conjointement avec les données conformes comme indiqué ci-dessus, et éviter délibérément l’application d’attributs d’IDL de données de longueur variable tels que la longueur comme les \[ **\_** \] données conformes.</span><span class="sxs-lookup"><span data-stu-id="89488-115">Applications can improve server resource utilization by using \[**range**\] in conjunction with conformant data as indicated above, as well as deliberately avoiding the application of variable-length data IDL attributes like like \[**length\_is**\] to conformant data.</span></span>

<span data-ttu-id="89488-116">L’application de la \[ **longueur \_** \] à des champs de structure de données définis dans un fichier IDL n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="89488-116">The application of \[**length\_is**\] to data structure fields defined in an IDL file is not recommended.</span></span>

## <a name="best-practices-for-variable-length-data-parameters"></a><span data-ttu-id="89488-117">Meilleures pratiques pour les paramètres de données de longueur variable</span><span class="sxs-lookup"><span data-stu-id="89488-117">Best Practices for Variable-length Data Parameters</span></span>

<span data-ttu-id="89488-118">Voici quelques-unes des meilleures pratiques à prendre en compte lors de la définition des attributs IDL pour les structures de données de taille variable, les paramètres de méthode et les champs.</span><span class="sxs-lookup"><span data-stu-id="89488-118">The following are several best practices to consider when defining the IDL attributes for variable-sized data structures, method parameters and fields.</span></span>

-   <span data-ttu-id="89488-119">Utilisez la corrélation précoce.</span><span class="sxs-lookup"><span data-stu-id="89488-119">Use early correlation.</span></span> <span data-ttu-id="89488-120">Il est généralement préférable de définir le champ ou le paramètre de taille de variable de façon à ce qu’il se produise immédiatement après le type intégral de contrôle.</span><span class="sxs-lookup"><span data-stu-id="89488-120">It is generally better to define the variable size parameter or field such that it occurs immediately after the controlling integral type.</span></span>

    <span data-ttu-id="89488-121">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="89488-121">For example,</span></span>

    ``` syntax
    earlyCorr
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long size, 
    [in,size_is(size)] char *pv
    );
    ```

    <span data-ttu-id="89488-122">est mieux que</span><span class="sxs-lookup"><span data-stu-id="89488-122">is better than</span></span>

    ``` syntax
    lateCorr
    (
    [in,size_is(size)] char *pv, 
    [in, range(MIN_COUNT, MAX_COUNT)] long size)
    );
    ```

    <span data-ttu-id="89488-123">où **earlyCorr** déclare le paramètre size juste avant le paramètre de données de longueur variable, et **lateCorr** déclare le paramètre size après.</span><span class="sxs-lookup"><span data-stu-id="89488-123">wherein **earlyCorr** declares the size parameter immediately before the variable-length data parameter, and **lateCorr** declares the size parameter after it.</span></span> <span data-ttu-id="89488-124">L’utilisation de la correspondance précoce améliore globalement les performances, en particulier dans les cas où la méthode est fréquemment appelée.</span><span class="sxs-lookup"><span data-stu-id="89488-124">Using early correspondence improves performance overall, especially in cases where the method is called frequently.</span></span>

-   <span data-ttu-id="89488-125">Pour les paramètres marqués avec l’option \[ **out, la taille \_ est** un \] tuple d’attribut et où la longueur des données est connue côté client ou où le client a une limite supérieure raisonnable, la définition de la méthode doit être similaire à ce qui suit, en termes d’attribution de paramètre et de séquence :</span><span class="sxs-lookup"><span data-stu-id="89488-125">For parameters marked with the \[**out, size\_is**\] attribute tuple, and where the data length is known on the client side or where the client has a reasonable upper bound, the method definition should be similar to the following in terms of parameter attribution and sequence:</span></span>

    ``` syntax
    outKnownSize
    (
    [in,range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out,size_is(lSize)] UserDataType * pArr
    );
    ```

    <span data-ttu-id="89488-126">Dans ce cas, le client fournit une mémoire tampon de taille fixe pour *pArr*, ce qui permet au service RPC côté serveur d’allouer une mémoire tampon de taille raisonnable avec un bon niveau d’assurance.</span><span class="sxs-lookup"><span data-stu-id="89488-126">In this case, the client provides a fixed size buffer for *pArr*, allowing the server-side RPC service to allocate a reasonably-sized buffer with a good degree of assurance.</span></span> <span data-ttu-id="89488-127">Notez que dans l’exemple, les données sont reçues à partir du serveur ( \[ **out** \] ).</span><span class="sxs-lookup"><span data-stu-id="89488-127">Note that in the example the data is received from the server (\[**out**\]).</span></span> <span data-ttu-id="89488-128">La définition est similaire pour les données passées au serveur ( \[ **dans** \] ).</span><span class="sxs-lookup"><span data-stu-id="89488-128">The definition is similar for data passed to the server (\[**in**\]).</span></span>

-   <span data-ttu-id="89488-129">Dans les situations où le composant côté serveur d’une application RPC détermine la longueur des données, la définition de la méthode doit ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="89488-129">For situations where the server-side component of an RPC application decides the data length, the method definition should be similar to the following:</span></span>

    ``` syntax
    typedef [range(MIN_COUNT,MAX_COUNT)] long RANGED_LONG;

    outUnknownSize
    (
    [out] RANGED_LONG *pSize,
    [out,size_is(,*pSize)] UserDataType **ppArr
    );
    ```

    <span data-ttu-id="89488-130">**Plage \_ LONG** est un type défini pour les stubs client et serveur, et d’une taille spécifiée que le client peut anticiper correctement.</span><span class="sxs-lookup"><span data-stu-id="89488-130">**RANGED\_LONG** is a type defined for both the client and server stubs, and of a specified size the client can correctly anticipate.</span></span> <span data-ttu-id="89488-131">Dans l’exemple, le client passe *ppArr* comme **null**, et le composant d’application serveur RPC alloue la quantité de mémoire correcte.</span><span class="sxs-lookup"><span data-stu-id="89488-131">In the example, the client passes *ppArr* as **NULL**, and the RPC server application component allocates the correct amount of memory.</span></span> <span data-ttu-id="89488-132">Lors du retour, le service RPC côté client alloue la mémoire pour les données retournées.</span><span class="sxs-lookup"><span data-stu-id="89488-132">Upon return, the RPC service on the client side allocates the memory for the returned data.</span></span>

-   <span data-ttu-id="89488-133">Si le client souhaite envoyer un sous-ensemble d’un grand tableau conforme au serveur, l’application peut spécifier la taille du sous-ensemble, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="89488-133">If the client wants to send a subset of a large conformant array to the server, the application can specify the size of the subset as demonstrated in the following example:</span></span>

    ``` syntax
    inConformantVaryingArray
    (
    [in,range(MIN_COUNT,MAX_COUNT)] long lSize,
    [in] long lLength, 
    [in,size_is(lSize), length_is(lLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="89488-134">De cette façon, RPC transmet uniquement les éléments *lLength* du tableau sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="89488-134">This way RPC will only transmit *lLength* elements of the array across the wire.</span></span> <span data-ttu-id="89488-135">Toutefois, cette définition force le service RPC à allouer de la mémoire de taille *lSize* côté serveur.</span><span class="sxs-lookup"><span data-stu-id="89488-135">However, this definition forces the RPC service to allocate memory of size *lSize* on the server side.</span></span>

-   <span data-ttu-id="89488-136">Si le composant d’application cliente détermine la taille maximale d’un tableau que le serveur peut retourner, mais permet au serveur de transmettre un sous-ensemble de ce tableau, l’application peut spécifier un tel comportement en définissant l’IDL similaire à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="89488-136">If the client application component determines the maximum size of an array the server can return, but allows the server to transmit a subset of that array, the application can specify such a behavior by defining the IDL similar to the following example:</span></span>

    ``` syntax
    inMaxSizeOutLength
    (
    [in, range(MIN_COUNT, MAX_COUNT)] long lSize,
    [out] long *pLength,
    [out,size_is(lSize), length_is(*pLength)] UserDataType *pArr
    );
    ```

    <span data-ttu-id="89488-137">Le composant d’application cliente spécifie la taille maximale du tableau, et le serveur spécifie le nombre d’éléments qu’il transmet au client.</span><span class="sxs-lookup"><span data-stu-id="89488-137">The client application component specifies the maximum size of the array, and the server specifies how many elements it transmits back to the client.</span></span>

-   <span data-ttu-id="89488-138">Si le composant d’application serveur doit retourner une chaîne au composant d’application cliente, et si le client sait que la taille maximale doit être retournée à partir du serveur, l’application peut utiliser un type de chaîne conforme, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="89488-138">If the server application component needs to return a string to the client application component, and if the client knows the maximum size to be returned from the server, the application can use a conformant string type as demonstrated in the following example:</span></span>

    ``` syntax
    outStringKnownSize
    (
    [in,range(MIN_COUNT, MAX_STRING)] long lSize,
    [out,size_is(lSize),string] wchar_t *pString
    );
    ```

-   <span data-ttu-id="89488-139">Si le composant de l’application cliente ne doit pas contrôler la taille de la chaîne, le service RPC peut allouer spécifiquement la mémoire, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="89488-139">If the client application component should not control the size of the string, the RPC service can specifically allocate the memory as demonstrated in the following example:</span></span>

    ``` syntax
    outStringUnknownSize
    (
    [out] LPWSTR *ppStr
    );
    ```

    <span data-ttu-id="89488-140">Le composant d’application cliente doit affecter à *ppStr* la **valeur null** lors de l’appel de la méthode RPC.</span><span class="sxs-lookup"><span data-stu-id="89488-140">The client application component must set *ppStr* to **NULL** on when calling the RPC method.</span></span>

 

 




