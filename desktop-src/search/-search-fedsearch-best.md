---
description: Cette rubrique répertorie les meilleures pratiques par le biais desquelles vous pouvez créer une banque de données basée sur le Web qui peut être recherchée à l’aide de Windows Federated Search et qui intègre vos sources de données distantes avec l’Explorateur Windows sans avoir à écrire ou à déployer du code côté client Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Meilleures pratiques suivantes dans Windows Federated Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112459"
---
# <a name="following-best-practices-in-windows-federated-search"></a><span data-ttu-id="e50f5-103">Meilleures pratiques suivantes dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="e50f5-103">Following Best Practices in Windows Federated Search</span></span>

<span data-ttu-id="e50f5-104">Cette rubrique répertorie les meilleures pratiques par le biais desquelles vous pouvez créer une banque de données basée sur le Web qui peut être recherchée à l’aide de Windows Federated Search et qui intègre vos sources de données distantes avec l’Explorateur Windows sans avoir à écrire ou à déployer du code côté client Windows.</span><span class="sxs-lookup"><span data-stu-id="e50f5-104">This topic lists the best practices through which you can build a web-based data store that can be searched using Windows federated search, and integrates your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="e50f5-105">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="e50f5-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e50f5-106">Meilleures pratiques pour Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="e50f5-106">Best Practices for Windows Federated Search</span></span>](#best-practices-for-windows-federated-search)
-   [<span data-ttu-id="e50f5-107">Meilleures pratiques pour la création d’une sortie RSS</span><span class="sxs-lookup"><span data-stu-id="e50f5-107">Best Practices for Creating RSS Output</span></span>](#best-practices-for-creating-rss-output)
-   [<span data-ttu-id="e50f5-108">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e50f5-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="e50f5-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e50f5-109">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a><span data-ttu-id="e50f5-110">Meilleures pratiques pour Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="e50f5-110">Best Practices for Windows Federated Search</span></span>

<span data-ttu-id="e50f5-111">Les pratiques recommandées pour l’utilisation de [OpenSearch](https://github.com/dewitt/opensearch) dans Windows 7 sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e50f5-111">Best practices for working with [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 are as follows:</span></span>

-   <span data-ttu-id="e50f5-112">Prenez en charge les paramètres *{startIndex}* et *{Count}* , et veillez à toujours retourner le nombre d’éléments demandés, sauf si vous retournez le dernier des résultats.</span><span class="sxs-lookup"><span data-stu-id="e50f5-112">Support the *{startIndex}* and *{count}* parameters, and be sure to always return the number of items requested unless you are returning the last of the results.</span></span>
-   <span data-ttu-id="e50f5-113">Si vous connaissez l’extension de nom de fichier, mappez-la à la propriété de l’interpréteur de commandes Windows [System. FileExtension](../properties/props-system-fileextension.md) .</span><span class="sxs-lookup"><span data-stu-id="e50f5-113">If you know the file name extension, map it to the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property.</span></span> <span data-ttu-id="e50f5-114">L’utilisation des extensions de nom de fichier est un meilleur moyen d’identifier un type de fichier que le type MIME.</span><span class="sxs-lookup"><span data-stu-id="e50f5-114">Using file name extensions is a better way to identify a file type than MIME type.</span></span>
-   <span data-ttu-id="e50f5-115">Assurez-vous que le type MIME ou l’extension de nom de fichier que vous spécifiez dans le RSS correspond au nom de fichier et au type MIME renvoyés dans l’en-tête HTTP par le serveur Web qui héberge l’élément lorsque le contenu de l’élément est demandé.</span><span class="sxs-lookup"><span data-stu-id="e50f5-115">Ensure that the MIME type or file name extension that you specify in the RSS matches the file name and MIME type returned in the HTTP header by the web server that hosts the item when the item content is requested.</span></span>
-   <span data-ttu-id="e50f5-116">Si vous retournez des éléments de fichier, retournez une taille de fichier chaque fois que cela est possible.</span><span class="sxs-lookup"><span data-stu-id="e50f5-116">If you are returning file items, return a file size whenever possible.</span></span> <span data-ttu-id="e50f5-117">Cela garantit l’exactitude de la boîte de dialogue de progression du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="e50f5-117">This ensures that the download progress dialog box is accurate.</span></span>
-   <span data-ttu-id="e50f5-118">Vérifiez que les demandes d’éléments au-delà de la fin du jeu de résultats ne retournent aucun résultat.</span><span class="sxs-lookup"><span data-stu-id="e50f5-118">Verify that requests for items beyond the end of the results set return no results.</span></span>
    > [!Note]  
    > <span data-ttu-id="e50f5-119">Ne pas répéter les résultats.</span><span class="sxs-lookup"><span data-stu-id="e50f5-119">Do not repeat results.</span></span>

     

-   <span data-ttu-id="e50f5-120">Ne placez pas les balises HTML là où elles n’appartiennent pas.</span><span class="sxs-lookup"><span data-stu-id="e50f5-120">Do not put HTML tags where they don't belong.</span></span> <span data-ttu-id="e50f5-121">Conformément à la spécification RSS, elles sont valides dans le champ Description, mais pas dans le champ titre.</span><span class="sxs-lookup"><span data-stu-id="e50f5-121">Per the RSS specification, they are valid in the description field, but not in the title field.</span></span>
-   <span data-ttu-id="e50f5-122">Ne créez pas de boîtiers pour des éléments de page Web.</span><span class="sxs-lookup"><span data-stu-id="e50f5-122">Do not create enclosures for webpage items.</span></span> <span data-ttu-id="e50f5-123">Par exemple, si vous créez un boîtier et que vous mappez une extension de nom de fichier. aspx, le fichier est téléchargé par l’Explorateur Windows dans le cache Internet et exécuté à partir de là.</span><span class="sxs-lookup"><span data-stu-id="e50f5-123">For example, if you create an enclosure and map a file name extension of .aspx, the file is downloaded by Windows Explorer to the Internet cache and executed from there.</span></span> <span data-ttu-id="e50f5-124">Les navigateurs Web ne gèrent pas le type de fichier. aspx.</span><span class="sxs-lookup"><span data-stu-id="e50f5-124">Web browsers do not handle the .aspx file type.</span></span> <span data-ttu-id="e50f5-125">L’utilisateur obtient une boîte **de dialogue Ouvrir avec** , ou le fichier peut être ouvert par une application comme Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e50f5-125">The user would get an **Open with** dialog box, or the file might be opened by an application like Microsoft Visual Studio.</span></span> <span data-ttu-id="e50f5-126">Évitez cela en retournant un élément Link uniquement pour les pages Web.</span><span class="sxs-lookup"><span data-stu-id="e50f5-126">Avoid this by returning a link element only for webpages.</span></span>
-   <span data-ttu-id="e50f5-127">Fournissez une URL de restauration Web dans le fichier. fichier osdx à l’aide d’un modèle d’URL avec `format="text\html"` .</span><span class="sxs-lookup"><span data-stu-id="e50f5-127">Provide a web roll-over URL in the .osdx file using a URL template with `format="text\html"`.</span></span>
-   <span data-ttu-id="e50f5-128">Fournissez une URL vers le dossier parent, le conteneur ou la page Web en mappant une valeur d’URL d’élément personnalisée à la propriété de l’interpréteur de commandes Windows [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) .</span><span class="sxs-lookup"><span data-stu-id="e50f5-128">Provide a URL to the parent folder, container, or webpage by mapping a custom element URL value to the [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell property.</span></span>

## <a name="best-practices-for-creating-rss-output"></a><span data-ttu-id="e50f5-129">Meilleures pratiques pour la création d’une sortie RSS</span><span class="sxs-lookup"><span data-stu-id="e50f5-129">Best Practices for Creating RSS Output</span></span>

<span data-ttu-id="e50f5-130">Les meilleures pratiques pour la création de la sortie RSS sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e50f5-130">Best practices for creating RSS output are as follows:</span></span>

-   <span data-ttu-id="e50f5-131">Chaque élément doit retourner une URL `link` ou une `enclosure` valeur (ou un équivalent, tel que `media:content` )</span><span class="sxs-lookup"><span data-stu-id="e50f5-131">Each item MUST return a URL `link` or `enclosure` value (or equivalent, such as `media:content`)</span></span>
-   <span data-ttu-id="e50f5-132">N’incluez pas de balises de mise en forme HTML dans l’attribut **title** , ou ces balises apparaîtront dans le titre et seront affichées dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="e50f5-132">Do not include any HTML formatting tags in the **title** attribute, or those tags will appear in the title and be displayed in Windows Explorer.</span></span>
-   <span data-ttu-id="e50f5-133">Pour l’élément **Description** :</span><span class="sxs-lookup"><span data-stu-id="e50f5-133">For the **description** element:</span></span>
    -   <span data-ttu-id="e50f5-134">Affichez suffisamment d’informations afin que l’utilisateur sache pourquoi ce résultat peut être pertinent.</span><span class="sxs-lookup"><span data-stu-id="e50f5-134">Show enough information so that the user knows why this result might be relevant.</span></span>
    -   <span data-ttu-id="e50f5-135">N’incluez pas de mise en forme HTML.</span><span class="sxs-lookup"><span data-stu-id="e50f5-135">Do not include HTML formatting.</span></span> <span data-ttu-id="e50f5-136">Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) supprime la mise en forme, ce qui peut donner des résultats moins que souhaitables pour votre description.</span><span class="sxs-lookup"><span data-stu-id="e50f5-136">The [OpenSearch](https://github.com/dewitt/opensearch) provider removes the formatting, which might result in less than desirable results for your description.</span></span>
    -   <span data-ttu-id="e50f5-137">N’incluez pas de métadonnées déjà fournies dans d’autres éléments, telles que le nom de fichier du boîtier, la taille, la date de modification, etc., car l’Explorateur Windows affiche déjà les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e50f5-137">Do not include metadata that is already provided in other elements, such as enclosure file name, size, modified date, and so forth, because Windows Explorer already displays the metadata.</span></span> <span data-ttu-id="e50f5-138">Son affichage dans l’élément **Description** est redondant.</span><span class="sxs-lookup"><span data-stu-id="e50f5-138">Displaying it in the **description** element would be redundant.</span></span>
-   <span data-ttu-id="e50f5-139">Pour les URL de boîtier ou de contenu :</span><span class="sxs-lookup"><span data-stu-id="e50f5-139">For enclosure or content URLs:</span></span>
    -   <span data-ttu-id="e50f5-140">Spécifiez l’attribut type comme type MIME valide.</span><span class="sxs-lookup"><span data-stu-id="e50f5-140">Specify the type attribute as a valid MIME type.</span></span>
    -   <span data-ttu-id="e50f5-141">Spécifiez la taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="e50f5-141">Specify the file size in bytes.</span></span>
-   <span data-ttu-id="e50f5-142">Si vous implémentez une sortie RSS dans .NET à l’aide de `DateTime` , testez votre flux dans Microsoft Internet Explorer pour voir s’il est valide avant de le déployer dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="e50f5-142">If you are implementing RSS output in .NET using `DateTime`, test your feed in Microsoft Internet Explorer to see if it is valid before deploying it to Windows Explorer.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e50f5-143">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e50f5-143">Additional Resources</span></span>

<span data-ttu-id="e50f5-144">Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e50f5-144">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e50f5-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e50f5-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e50f5-146">Recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="e50f5-146">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="e50f5-147">Prise en main avec la recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="e50f5-147">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="e50f5-148">Connexion de votre service Web dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="e50f5-148">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="e50f5-149">Activation de votre magasin de données dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="e50f5-149">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="e50f5-150">Création d’un fichier de description OpenSearch dans Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="e50f5-150">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="e50f5-151">Déploiement de connecteurs de recherche dans la recherche fédérée Windows</span><span class="sxs-lookup"><span data-stu-id="e50f5-151">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> <dt>

[<span data-ttu-id="e50f5-152">Extension de l’index</span><span class="sxs-lookup"><span data-stu-id="e50f5-152">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
