---
title: Gestion des localisateurs de ressources uniformes
description: Une Uniform Resource Locator (URL) est une représentation compacte de l’emplacement et de la méthode d’accès d’une ressource située sur Internet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08157738d99e78ff4d458a3bdd1b1e2e661ce538
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104550437"
---
# <a name="handling-uniform-resource-locators"></a><span data-ttu-id="cce1e-103">Gestion des localisateurs de ressources uniformes</span><span class="sxs-lookup"><span data-stu-id="cce1e-103">Handling Uniform Resource Locators</span></span>

<span data-ttu-id="cce1e-104">Une Uniform Resource Locator (URL) est une représentation compacte de l’emplacement et de la méthode d’accès d’une ressource située sur Internet.</span><span class="sxs-lookup"><span data-stu-id="cce1e-104">A Uniform Resource Locator (URL) is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="cce1e-105">Chaque URL se compose d’un schéma (HTTP, HTTPs ou FTP) et d’une chaîne spécifique au schéma.</span><span class="sxs-lookup"><span data-stu-id="cce1e-105">Each URL consists of a scheme (HTTP, HTTPS, or FTP) and a scheme-specific string.</span></span> <span data-ttu-id="cce1e-106">Cette chaîne peut également inclure une combinaison d’un chemin d’accès de répertoire, d’une chaîne de recherche ou d’un nom de ressource.</span><span class="sxs-lookup"><span data-stu-id="cce1e-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="cce1e-107">Les fonctions WinINet offrent la possibilité de créer, combiner, décomposer et canonicaliser des URL.</span><span class="sxs-lookup"><span data-stu-id="cce1e-107">The WinINet functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="cce1e-108">Pour plus d’informations sur les URL, consultez [RFC-1738 sur les](https://www.ietf.org/rfc/rfc1738.txt) URL (Uniform Resource Locators).</span><span class="sxs-lookup"><span data-stu-id="cce1e-108">For more information on URLs, see [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) on Uniform Resource Locators (URL).</span></span>

<span data-ttu-id="cce1e-109">Les fonctions d’URL fonctionnent de manière orientée tâche.</span><span class="sxs-lookup"><span data-stu-id="cce1e-109">The URL functions operate in a task-oriented manner.</span></span> <span data-ttu-id="cce1e-110">Le contenu et le format de l’URL qui est donnée à la fonction ne sont pas vérifiés.</span><span class="sxs-lookup"><span data-stu-id="cce1e-110">The content and format of the URL that is given to the function is not verified.</span></span> <span data-ttu-id="cce1e-111">L’application appelante doit suivre l’utilisation de ces fonctions pour s’assurer que les données sont au format prévu.</span><span class="sxs-lookup"><span data-stu-id="cce1e-111">The calling application should track the use of these functions to ensure that the data is in the intended format.</span></span> <span data-ttu-id="cce1e-112">Par exemple, la fonction [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) convertit le caractère « % » en séquence d’échappement « %25 » lors de l’utilisation d’aucun indicateur.</span><span class="sxs-lookup"><span data-stu-id="cce1e-112">For example, the [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function would convert the character "%" into the escape sequence "%25" when using no flags.</span></span> <span data-ttu-id="cce1e-113">Si [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) est utilisé sur l’URL canonique, la séquence d’échappement « %25 » est convertie en séquence d’échappement « %2525 », ce qui ne fonctionnerait pas correctement.</span><span class="sxs-lookup"><span data-stu-id="cce1e-113">If [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) is used on the canonicalized URL, the escape sequence "%25" would be converted into the escape sequence "%2525", which would not work properly.</span></span>

-   [<span data-ttu-id="cce1e-114">Qu’est-ce qu’une URL canonique ?</span><span class="sxs-lookup"><span data-stu-id="cce1e-114">What Is a Canonicalized URL?</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="cce1e-115">Utilisation des fonctions WinINet pour gérer les URL</span><span class="sxs-lookup"><span data-stu-id="cce1e-115">Using the WinINet Functions to Handle URLs</span></span>](#using-the-wininet-functions-to-handle-urls)
-   [<span data-ttu-id="cce1e-116">Canonicalisation des URL</span><span class="sxs-lookup"><span data-stu-id="cce1e-116">Canonicalizing URLs</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="cce1e-117">Combinaison d’URL de base et relatives</span><span class="sxs-lookup"><span data-stu-id="cce1e-117">Combining Base and Relative URLs</span></span>](#combining-base-and-relative-urls)
-   [<span data-ttu-id="cce1e-118">Piratage des URL</span><span class="sxs-lookup"><span data-stu-id="cce1e-118">Cracking URLs</span></span>](#cracking-urls)
-   [<span data-ttu-id="cce1e-119">Création d’URL</span><span class="sxs-lookup"><span data-stu-id="cce1e-119">Creating URLs</span></span>](#creating-urls)
-   [<span data-ttu-id="cce1e-120">Accès direct aux URL</span><span class="sxs-lookup"><span data-stu-id="cce1e-120">Accessing URLs Directly</span></span>](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="cce1e-121">Qu’est-ce qu’une URL canonique ?</span><span class="sxs-lookup"><span data-stu-id="cce1e-121">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="cce1e-122">Le format de toutes les URL doit respecter la syntaxe et la sémantique acceptées afin d’accéder aux ressources via Internet.</span><span class="sxs-lookup"><span data-stu-id="cce1e-122">The format of all URLs must follow the accepted syntax and semantics in order to access resources through the Internet.</span></span> <span data-ttu-id="cce1e-123">La canonicalisation est le processus de mise en forme d’une URL pour suivre cette syntaxe et cette sémantique acceptées.</span><span class="sxs-lookup"><span data-stu-id="cce1e-123">Canonicalization is the process of formatting a URL to follow this accepted syntax and semantics.</span></span>

<span data-ttu-id="cce1e-124">Les caractères qui doivent être encodés incluent tous les caractères qui n’ont aucun caractère graphique correspondant dans le jeu de caractères codés US-ASCII (hexadécimal 80-FF, qui ne sont pas utilisés dans le jeu de caractères codés US-ASCII, et les valeurs hexadécimales 00-1F et 7F, qui sont des caractères de contrôle), des espaces vides, « % » (qui est utilisé pour encoder d’autres caractères) et des caractères non sûrs (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ \]</span><span class="sxs-lookup"><span data-stu-id="cce1e-124">Characters that must be encoded include any characters that have no corresponding graphic character in the US-ASCII coded character set (hexadecimal 80-FF, which are not used in the US-ASCII coded character set, and hexadecimal 00-1F and 7F, which are control characters), blank spaces, "%" (which is used to encode other characters), and unsafe characters (<, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ').</span></span>

## <a name="using-the-wininet-functions-to-handle-urls"></a><span data-ttu-id="cce1e-125">Utilisation des fonctions WinINet pour gérer les URL</span><span class="sxs-lookup"><span data-stu-id="cce1e-125">Using the WinINet Functions to Handle URLs</span></span>

<span data-ttu-id="cce1e-126">Le tableau suivant récapitule les fonctions d’URL.</span><span class="sxs-lookup"><span data-stu-id="cce1e-126">The following table summarizes the URL functions.</span></span>



| <span data-ttu-id="cce1e-127">Fonction</span><span class="sxs-lookup"><span data-stu-id="cce1e-127">Function</span></span>                                                   | <span data-ttu-id="cce1e-128">Description</span><span class="sxs-lookup"><span data-stu-id="cce1e-128">Description</span></span>                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="cce1e-129">**InternetCanonicalizeUrl**</span><span class="sxs-lookup"><span data-stu-id="cce1e-129">**InternetCanonicalizeUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | <span data-ttu-id="cce1e-130">Canonicalizes l’URL.</span><span class="sxs-lookup"><span data-stu-id="cce1e-130">Canonicalizes the URL.</span></span>                             |
| [<span data-ttu-id="cce1e-131">**InternetCombineUrl**</span><span class="sxs-lookup"><span data-stu-id="cce1e-131">**InternetCombineUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | <span data-ttu-id="cce1e-132">Combine des URL de base et relatives.</span><span class="sxs-lookup"><span data-stu-id="cce1e-132">Combines base and relative URLs.</span></span>                   |
| [<span data-ttu-id="cce1e-133">**InternetCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="cce1e-133">**InternetCrackUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | <span data-ttu-id="cce1e-134">Analyse une chaîne d’URL en composants.</span><span class="sxs-lookup"><span data-stu-id="cce1e-134">Parses a URL string into components.</span></span>               |
| [<span data-ttu-id="cce1e-135">**InternetCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="cce1e-135">**InternetCreateUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | <span data-ttu-id="cce1e-136">Crée une chaîne d’URL à partir de composants.</span><span class="sxs-lookup"><span data-stu-id="cce1e-136">Creates a URL string from components.</span></span>              |
| [<span data-ttu-id="cce1e-137">**InternetOpenUrl**</span><span class="sxs-lookup"><span data-stu-id="cce1e-137">**InternetOpenUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | <span data-ttu-id="cce1e-138">Commence à récupérer une ressource FTP, HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="cce1e-138">Begins retrieving an FTP, HTTP, or HTTPS resource.</span></span> |



 

## <a name="canonicalizing-urls"></a><span data-ttu-id="cce1e-139">Canonicalisation des URL</span><span class="sxs-lookup"><span data-stu-id="cce1e-139">Canonicalizing URLs</span></span>

<span data-ttu-id="cce1e-140">La canonicalisation d’une URL est le processus qui convertit une URL, qui peut contenir des caractères non sécurisés tels que des espaces vides, des caractères réservés, etc., dans un format accepté.</span><span class="sxs-lookup"><span data-stu-id="cce1e-140">Canonicalizing a URL is the process that converts a URL, which might contain unsafe characters such as blank spaces, reserved characters, and so on, into an accepted format.</span></span>

<span data-ttu-id="cce1e-141">La fonction [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) peut être utilisée pour canonicaliser des URL.</span><span class="sxs-lookup"><span data-stu-id="cce1e-141">The [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function can be used to canonicalize URLs.</span></span> <span data-ttu-id="cce1e-142">Cette fonction étant très orientée tâche, l’application doit suivre son utilisation avec précaution.</span><span class="sxs-lookup"><span data-stu-id="cce1e-142">This function is very task-oriented, so the application should track its use carefully.</span></span> <span data-ttu-id="cce1e-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) ne vérifie pas que l’URL qui lui est transmise est déjà canonique et que l’URL renvoyée est valide.</span><span class="sxs-lookup"><span data-stu-id="cce1e-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) does not verify that the URL passed to it is already canonicalized and that the URL that it returns is valid.</span></span>

<span data-ttu-id="cce1e-144">Les cinq indicateurs suivants contrôlent la façon dont [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) gère une URL particulière.</span><span class="sxs-lookup"><span data-stu-id="cce1e-144">The following five flags control how [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) handles a particular URL.</span></span> <span data-ttu-id="cce1e-145">Les indicateurs peuvent être utilisés en combinaison.</span><span class="sxs-lookup"><span data-stu-id="cce1e-145">The flags can be used in combination.</span></span> <span data-ttu-id="cce1e-146">Si aucun indicateur n’est utilisé, la fonction encode l’URL par défaut.</span><span class="sxs-lookup"><span data-stu-id="cce1e-146">If no flags are used, the function encodes the URL by default.</span></span>



| <span data-ttu-id="cce1e-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="cce1e-147">Value</span></span>                     | <span data-ttu-id="cce1e-148">Signification</span><span class="sxs-lookup"><span data-stu-id="cce1e-148">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cce1e-149">\_mode navigateur \_ ICU</span><span class="sxs-lookup"><span data-stu-id="cce1e-149">ICU\_BROWSER\_MODE</span></span>        | <span data-ttu-id="cce1e-150">Ne pas encoder ou décoder les caractères après « \# » ou «  ? » et ne pas supprimer les espaces blancs de fin après «  ? ».</span><span class="sxs-lookup"><span data-stu-id="cce1e-150">Do not encode or decode characters after "\#" or "?", and do not remove trailing white space after "?".</span></span> <span data-ttu-id="cce1e-151">Si cette valeur n’est pas spécifiée, l’URL entière est encodée et l’espace blanc de fin est supprimé.</span><span class="sxs-lookup"><span data-stu-id="cce1e-151">If this value is not specified, the entire URL is encoded, and trailing white space is removed.</span></span> |
| <span data-ttu-id="cce1e-152">décodage ICU \_</span><span class="sxs-lookup"><span data-stu-id="cce1e-152">ICU\_DECODE</span></span>               | <span data-ttu-id="cce1e-153">Convertit toutes les séquences% XX en caractères, y compris les séquences d’échappement, avant l’analyse de l’URL.</span><span class="sxs-lookup"><span data-stu-id="cce1e-153">Convert all %XX sequences to characters, including escape sequences, before the URL is parsed.</span></span>                                                                                                          |
| <span data-ttu-id="cce1e-154">BIBLIOTHÈQUE de \_ codage des \_ espaces \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="cce1e-154">ICU\_ENCODE\_SPACES\_ONLY</span></span> | <span data-ttu-id="cce1e-155">Encoder les espaces uniquement.</span><span class="sxs-lookup"><span data-stu-id="cce1e-155">Encode spaces only.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="cce1e-156">ICU \_ sans \_ codage</span><span class="sxs-lookup"><span data-stu-id="cce1e-156">ICU\_NO\_ENCODE</span></span>           | <span data-ttu-id="cce1e-157">Ne convertissez pas les caractères non sécurisés en séquences d’échappement.</span><span class="sxs-lookup"><span data-stu-id="cce1e-157">Do not convert unsafe characters to escape sequences.</span></span>                                                                                                                                                   |
| <span data-ttu-id="cce1e-158">ICU \_ sans \_ méta</span><span class="sxs-lookup"><span data-stu-id="cce1e-158">ICU\_NO\_META</span></span>             | <span data-ttu-id="cce1e-159">Ne supprimez pas les séquences Meta (telles que « . » et « .. ») de l’URL.</span><span class="sxs-lookup"><span data-stu-id="cce1e-159">Do not remove meta sequences (such as "." and "..") from the URL.</span></span>                                                                                                                                       |



 

<span data-ttu-id="cce1e-160">L' \_ indicateur de décodage ICU doit être utilisé uniquement sur les URL canoniques, car il suppose que toutes les séquences% XX sont des codes d’échappement et les convertit en caractères indiqués par le code.</span><span class="sxs-lookup"><span data-stu-id="cce1e-160">The ICU\_DECODE flag should be used only on canonicalized URLs, because it assumes that all %XX sequences are escape codes and converts them into the characters indicated by the code.</span></span> <span data-ttu-id="cce1e-161">Si l’URL contient un symbole « % » qui ne fait pas partie d’un code d’échappement, ICU \_ Decode le traite toujours comme un.</span><span class="sxs-lookup"><span data-stu-id="cce1e-161">If the URL has a "%" symbol in it that is not part of an escape code, ICU\_DECODE still treats it as one.</span></span> <span data-ttu-id="cce1e-162">Cette caractéristique peut entraîner la création par [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) d’une URL non valide.</span><span class="sxs-lookup"><span data-stu-id="cce1e-162">This characteristic might cause [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to create an invalid URL.</span></span>

<span data-ttu-id="cce1e-163">Pour utiliser [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) afin de retourner une URL complètement décodée, les indicateurs de décodage ICU \_ et de bibliothèque ICU \_ ne \_ doivent pas être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="cce1e-163">To use [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to return a completely decoded URL, the ICU\_DECODE and ICU\_NO\_ENCODE flags must be specified.</span></span> <span data-ttu-id="cce1e-164">Ce programme d’installation suppose que l’URL passée à [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) a déjà été rendue canonique.</span><span class="sxs-lookup"><span data-stu-id="cce1e-164">This setup assumes that the URL being passed to [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) has been previously canonicalized.</span></span>

## <a name="combining-base-and-relative-urls"></a><span data-ttu-id="cce1e-165">Combinaison d’URL de base et relatives</span><span class="sxs-lookup"><span data-stu-id="cce1e-165">Combining Base and Relative URLs</span></span>

<span data-ttu-id="cce1e-166">Une URL relative est une représentation compacte de l’emplacement d’une ressource par rapport à une URL de base absolue.</span><span class="sxs-lookup"><span data-stu-id="cce1e-166">A relative URL is a compact representation of the location of a resource relative to an absolute base URL.</span></span> <span data-ttu-id="cce1e-167">L’URL de base doit être connue de l’analyseur et inclure généralement le schéma, l’emplacement réseau et les parties du chemin d’accès de l’URL.</span><span class="sxs-lookup"><span data-stu-id="cce1e-167">The base URL must be known to the parser and usually includes the scheme, network location, and parts of the URL path.</span></span> <span data-ttu-id="cce1e-168">Une application peut appeler [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) pour combiner l’URL relative avec son URL de base.</span><span class="sxs-lookup"><span data-stu-id="cce1e-168">An application can call [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) to combine the relative URL with its base URL.</span></span> <span data-ttu-id="cce1e-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) canonicalizes également l’URL résultante.</span><span class="sxs-lookup"><span data-stu-id="cce1e-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) also canonicalizes the resultant URL.</span></span>

## <a name="cracking-urls"></a><span data-ttu-id="cce1e-170">Piratage des URL</span><span class="sxs-lookup"><span data-stu-id="cce1e-170">Cracking URLs</span></span>

<span data-ttu-id="cce1e-171">La fonction [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) sépare une URL en ses composants et retourne les composants indiqués par la structure [**de \_ composants URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) qui est transmise à la fonction.</span><span class="sxs-lookup"><span data-stu-id="cce1e-171">The [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure that is passed to the function.</span></span>

<span data-ttu-id="cce1e-172">Les composants qui composent la structure des [**\_ composants d’URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) sont le numéro de schéma, le nom d’hôte, le numéro de port, le nom d’utilisateur, le mot de passe, le chemin d’URL et des informations supplémentaires (tels que les paramètres de recherche).</span><span class="sxs-lookup"><span data-stu-id="cce1e-172">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme number, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="cce1e-173">Chaque composant, sauf le schéma et le numéro de port, a un membre de chaîne qui contient les informations et un membre qui contient la longueur du membre de chaîne.</span><span class="sxs-lookup"><span data-stu-id="cce1e-173">Each component, except the scheme and port numbers, has a string member that holds the information, and a member that holds the length of the string member.</span></span> <span data-ttu-id="cce1e-174">Le schéma et les numéros de port ont uniquement un membre qui stocke la valeur correspondante ; elles sont toutes deux retournées sur tous les appels réussis à [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span><span class="sxs-lookup"><span data-stu-id="cce1e-174">The scheme and port numbers have only a member that stores the corresponding value; they are both returned on all successful calls to [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span></span>

<span data-ttu-id="cce1e-175">Pour obtenir la valeur d’un composant particulier dans la structure de [**\_ composants URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , le membre qui stocke la longueur de chaîne de ce composant doit être défini sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="cce1e-175">To get the value of a particular component in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="cce1e-176">Le membre de chaîne peut être l’adresse d’une mémoire tampon ou la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cce1e-176">The string member can be either the address of a buffer or **NULL**.</span></span>

<span data-ttu-id="cce1e-177">Si le membre de pointeur contient l’adresse d’une mémoire tampon, le membre de longueur de chaîne doit contenir la taille de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cce1e-177">If the pointer member contains the address of a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="cce1e-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) retourne les informations de composant sous la forme d’une chaîne dans la mémoire tampon et stocke la longueur de chaîne dans le membre de longueur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="cce1e-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="cce1e-179">Si le membre du pointeur est **null**, le membre de longueur de chaîne peut être défini sur n’importe quelle valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="cce1e-179">If the pointer member is **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="cce1e-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) stocke l’adresse du premier caractère de la chaîne d’URL qui contient les informations sur le composant et définit la longueur de chaîne sur le nombre de caractères dans la partie restante de la chaîne d’URL qui se rapporte au composant.</span><span class="sxs-lookup"><span data-stu-id="cce1e-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) stores the address of the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="cce1e-181">Tous les membres de pointeur ayant la valeur **null** avec un membre de longueur différente de zéro pointent vers le point de départ approprié dans la chaîne d’URL.</span><span class="sxs-lookup"><span data-stu-id="cce1e-181">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="cce1e-182">La longueur stockée dans le membre de longueur doit être utilisée pour déterminer la fin des informations du composant individuel.</span><span class="sxs-lookup"><span data-stu-id="cce1e-182">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="cce1e-183">Pour terminer l’initialisation de la structure des [**\_ composants URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , le membre **dwStructSize** doit être défini sur la taille de la structure des [**\_ composants URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , en octets.</span><span class="sxs-lookup"><span data-stu-id="cce1e-183">To finish initializing the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, in bytes.</span></span>

<span data-ttu-id="cce1e-184">L’exemple suivant retourne les composants de l’URL dans la zone d’édition, IDC \_ PreOpen1, et retourne les composants à la zone de liste, IDC \_ PreOpenList.</span><span class="sxs-lookup"><span data-stu-id="cce1e-184">The following example returns the components of the URL in the edit box, IDC\_PreOpen1, and returns the components to the list box, IDC\_PreOpenList.</span></span> <span data-ttu-id="cce1e-185">Pour afficher uniquement les informations relatives à un composant individuel, cette fonction copie le caractère immédiatement après les informations du composant dans la chaîne et le remplace temporairement par une **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cce1e-185">To display only the information for an individual component, this function copies the character immediately after the component's information in the string and temporarily replaces it with a **NULL**.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a><span data-ttu-id="cce1e-186">Création d’URL</span><span class="sxs-lookup"><span data-stu-id="cce1e-186">Creating URLs</span></span>

<span data-ttu-id="cce1e-187">La fonction [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) utilise les informations de la structure de [**\_ composants URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) pour créer un Uniform Resource Locator.</span><span class="sxs-lookup"><span data-stu-id="cce1e-187">The [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) function uses the information in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure to create a Uniform Resource Locator.</span></span>

<span data-ttu-id="cce1e-188">Les composants qui composent la structure des [**\_ composants d’URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) sont le schéma, le nom d’hôte, le numéro de port, le nom d’utilisateur, le mot de passe, le chemin d’URL et des informations supplémentaires (tels que les paramètres de recherche).</span><span class="sxs-lookup"><span data-stu-id="cce1e-188">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="cce1e-189">Chaque composant, à l’exception du numéro de port, a un membre de chaîne qui contient les informations et un membre qui contient la longueur du membre de chaîne.</span><span class="sxs-lookup"><span data-stu-id="cce1e-189">Each component, except the port number, has a string member that holds the information, and a member that holds the length of the string member.</span></span>

<span data-ttu-id="cce1e-190">Pour chaque composant requis, le membre du pointeur doit contenir l’adresse de la mémoire tampon contenant les informations.</span><span class="sxs-lookup"><span data-stu-id="cce1e-190">For each required component, the pointer member should contain the address of the buffer holding the information.</span></span> <span data-ttu-id="cce1e-191">Le membre de longueur doit avoir la valeur zéro si le membre pointeur contient l’adresse d’une chaîne se terminant par zéro ; le membre de longueur doit être défini sur la longueur de chaîne si le membre pointeur contient l’adresse d’une chaîne qui ne se termine pas par zéro.</span><span class="sxs-lookup"><span data-stu-id="cce1e-191">The length member should be set to zero if the pointer member contains the address of a zero-terminated string; the length member should be set to the string length if the pointer member contains the address of a string that is not zero-terminated.</span></span> <span data-ttu-id="cce1e-192">Le membre pointeur de tous les composants qui ne sont pas obligatoires doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cce1e-192">The pointer member of any components that are not required must be **NULL**.</span></span>

## <a name="accessing-urls-directly"></a><span data-ttu-id="cce1e-193">Accès direct aux URL</span><span class="sxs-lookup"><span data-stu-id="cce1e-193">Accessing URLs Directly</span></span>

<span data-ttu-id="cce1e-194">Les ressources FTP et HTTP sur Internet sont accessibles directement à l’aide des fonctions [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)et [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="cce1e-194">FTP, and HTTP resources on the Internet can be accessed directly by using the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="cce1e-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) ouvre une connexion à la ressource à l’URL transmise à la fonction.</span><span class="sxs-lookup"><span data-stu-id="cce1e-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) opens a connection to the resource at the URL passed to the function.</span></span> <span data-ttu-id="cce1e-196">Lorsque cette connexion est établie, il existe deux étapes possibles.</span><span class="sxs-lookup"><span data-stu-id="cce1e-196">When this connection is made, there are two possible steps.</span></span> <span data-ttu-id="cce1e-197">Tout d’abord, si la ressource est un fichier, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) peut la télécharger. Deuxièmement, si la ressource est un répertoire, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) peut énumérer les fichiers dans le répertoire (sauf en cas d’utilisation de proxys CERN).</span><span class="sxs-lookup"><span data-stu-id="cce1e-197">First, if the resource is a file, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can download it; second, if the resource is a directory, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) can enumerate the files within the directory (except when using CERN proxies).</span></span> <span data-ttu-id="cce1e-198">Pour plus d’informations sur [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), consultez [lecture de fichiers](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="cce1e-198">For more information on [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), see [Reading Files](common-functions.md).</span></span> <span data-ttu-id="cce1e-199">Pour plus d’informations sur [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), consultez [recherche du fichier suivant](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="cce1e-199">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="cce1e-200">Pour les applications qui doivent fonctionner via un proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) peut être utilisé pour accéder aux répertoires et aux fichiers FTP.</span><span class="sxs-lookup"><span data-stu-id="cce1e-200">For applications that need to operate through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used to access FTP directories and files.</span></span> <span data-ttu-id="cce1e-201">Les demandes FTP sont empaquetées pour apparaître comme une requête HTTP, que le proxy CERN accepterait.</span><span class="sxs-lookup"><span data-stu-id="cce1e-201">The FTP requests are packaged to appear like an HTTP request, which the CERN proxy would accept.</span></span>

<span data-ttu-id="cce1e-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilise le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) créé par la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) et l’URL de la ressource.</span><span class="sxs-lookup"><span data-stu-id="cce1e-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function and the URL of the resource.</span></span> <span data-ttu-id="cce1e-203">L’URL doit inclure le schéma (http :, FTP :, fichier : \[ pour un fichier local \] ou https : \[ pour Secure Protocol Secure \] ) et l’emplacement réseau (tel que `www.microsoft.com` ).</span><span class="sxs-lookup"><span data-stu-id="cce1e-203">The URL must include the scheme (http:, ftp:, file: \[for a local file\], or https: \[for hypertext protocol secure\]) and network location (such as `www.microsoft.com`).</span></span> <span data-ttu-id="cce1e-204">L’URL peut également inclure un chemin d’accès (par exemple,/ISAPI/gomscom.asp ? TARGET =/Windows/Feature/) et nom de la ressource (par exemple, default.htm).</span><span class="sxs-lookup"><span data-stu-id="cce1e-204">The URL can also include a path (for example, /isapi/gomscom.asp?TARGET=/windows/feature/) and resource name (for example, default.htm).</span></span> <span data-ttu-id="cce1e-205">Pour les requêtes HTTP ou HTTPs, des en-têtes supplémentaires peuvent être inclus.</span><span class="sxs-lookup"><span data-stu-id="cce1e-205">For HTTP or HTTPS requests, additional headers can be included.</span></span>

<span data-ttu-id="cce1e-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)et [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (URL http ou HTTPS uniquement) peuvent utiliser le descripteur créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pour télécharger la ressource.</span><span class="sxs-lookup"><span data-stu-id="cce1e-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only) can use the handle that is created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to download the resource.</span></span>

<span data-ttu-id="cce1e-207">Le diagramme suivant illustre les descripteurs à utiliser avec chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="cce1e-207">The following diagram illustrates which handles to use with each function.</span></span>

![Handles à utiliser avec les fonctions](images/ax-wnt02.png)

<span data-ttu-id="cce1e-209">Le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) racine créé par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) est utilisé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="cce1e-209">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) is used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span> <span data-ttu-id="cce1e-210">Le descripteur **HINTERNET** créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) peut être utilisé par [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (non illustré ici) et [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (URL http ou HTTPS uniquement).</span><span class="sxs-lookup"><span data-stu-id="cce1e-210">The **HINTERNET** handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used by [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (not shown here), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only).</span></span>

<span data-ttu-id="cce1e-211">Pour plus d’informations, consultez [**Handles HINTERNET**](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="cce1e-211">For more information, see [**HINTERNET Handles**](appendix-a-hinternet-handles.md).</span></span>

> [!Note]  
> <span data-ttu-id="cce1e-212">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="cce1e-212">WinINet does not support server implementations.</span></span> <span data-ttu-id="cce1e-213">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="cce1e-213">In addition, it should not be used from a service.</span></span> <span data-ttu-id="cce1e-214">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="cce1e-214">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 