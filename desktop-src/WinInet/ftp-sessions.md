---
title: Sessions FTP
description: WinINet permet aux applications de parcourir et de manipuler des répertoires et des fichiers sur un serveur FTP. Étant donné que les proxys CERN ne prennent pas en charge FTP, les applications qui utilisent un proxy CERN doivent utiliser la fonction InternetOpenUrl.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031535"
---
# <a name="ftp-sessions"></a><span data-ttu-id="7b003-104">Sessions FTP</span><span class="sxs-lookup"><span data-stu-id="7b003-104">FTP Sessions</span></span>

<span data-ttu-id="7b003-105">WinINet permet aux applications de parcourir et de manipuler des répertoires et des fichiers sur un serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-105">WinINet enables applications to navigate and manipulate directories and files on an ftp server.</span></span> <span data-ttu-id="7b003-106">Étant donné que les proxys CERN ne prennent pas en charge FTP, les applications qui utilisent un proxy CERN doivent utiliser la fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="7b003-106">Because CERN proxies do not support FTP, applications that use a CERN proxy exclusively must use the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> <span data-ttu-id="7b003-107">Pour plus d’informations sur l’utilisation de [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), consultez [accès direct aux URL](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="7b003-107">For more information about how to use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="7b003-108">Pour démarrer une session FTP, utilisez [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) pour créer le descripteur de session.</span><span class="sxs-lookup"><span data-stu-id="7b003-108">To begin an FTP session, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to create the session handle.</span></span>

<span data-ttu-id="7b003-109">WinINet vous permet d’effectuer les actions suivantes sur un serveur FTP :</span><span class="sxs-lookup"><span data-stu-id="7b003-109">WinINet enables you to perform the following actions on an FTP server:</span></span>

-   <span data-ttu-id="7b003-110">Naviguer entre les répertoires.</span><span class="sxs-lookup"><span data-stu-id="7b003-110">Navigate between directories.</span></span>
-   <span data-ttu-id="7b003-111">Énumérer, créer, supprimer et renommer des répertoires.</span><span class="sxs-lookup"><span data-stu-id="7b003-111">Enumerate, create, remove, and rename directories.</span></span>
-   <span data-ttu-id="7b003-112">Renommez, chargez, téléchargez et supprimez des fichiers.</span><span class="sxs-lookup"><span data-stu-id="7b003-112">Rename, upload, download, and delete files.</span></span>

<span data-ttu-id="7b003-113">La navigation est assurée par les fonctions [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) et [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="7b003-113">Navigation is provided by the [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions.</span></span> <span data-ttu-id="7b003-114">Ces fonctions utilisent le descripteur de session créé par un appel précédent à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) pour déterminer le répertoire dans lequel l’application se trouve actuellement, ou pour basculer vers un autre sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="7b003-114">These functions utilize the session handle created by a previous call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to determine which directory the application is currently in, or to change to a different subdirectory.</span></span>

<span data-ttu-id="7b003-115">L’énumération des répertoires s’effectue à l’aide des fonctions [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) et [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="7b003-115">Directory enumeration is performed by using the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="7b003-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) utilise le handle de session créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) pour rechercher le premier fichier qui correspond aux critères de recherche donnés et retourne un handle pour continuer l’énumération de répertoires.</span><span class="sxs-lookup"><span data-stu-id="7b003-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to find the first file that matches the given search criteria and returns a handle to continue the directory enumeration.</span></span> <span data-ttu-id="7b003-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) utilise le handle retourné par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) pour retourner le fichier suivant qui correspond aux critères de recherche d’origine.</span><span class="sxs-lookup"><span data-stu-id="7b003-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) uses the handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) to return the next file that matches the original search criteria.</span></span> <span data-ttu-id="7b003-118">L’application doit continuer à appeler [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) jusqu’à ce qu’il n’y ait plus de fichiers restants dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="7b003-118">The application should continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until there are no more files left in the directory.</span></span>

<span data-ttu-id="7b003-119">Utilisez la fonction [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) pour créer des répertoires.</span><span class="sxs-lookup"><span data-stu-id="7b003-119">Use the [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function to create new directories.</span></span> <span data-ttu-id="7b003-120">Cette fonction utilise le handle de session créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) et crée le répertoire spécifié par la chaîne transmise à la fonction.</span><span class="sxs-lookup"><span data-stu-id="7b003-120">This function uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and creates the directory specified by the string passed to the function.</span></span> <span data-ttu-id="7b003-121">La chaîne peut contenir un nom de répertoire relatif au répertoire actif, ou un chemin d’accès complet au répertoire.</span><span class="sxs-lookup"><span data-stu-id="7b003-121">The string can contain a directory name relative to the current directory, or a fully qualified directory path.</span></span>

<span data-ttu-id="7b003-122">Pour renommer des fichiers ou des répertoires, l’application peut appeler [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span><span class="sxs-lookup"><span data-stu-id="7b003-122">To rename either files or directories, the application can call [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span></span> <span data-ttu-id="7b003-123">Cette fonction remplace le nom d’origine par le nouveau nom passé à la fonction.</span><span class="sxs-lookup"><span data-stu-id="7b003-123">This function replaces the original name with the new name passed to the function.</span></span> <span data-ttu-id="7b003-124">Le nom du fichier ou du répertoire peut être relatif au répertoire actif ou à un nom complet.</span><span class="sxs-lookup"><span data-stu-id="7b003-124">The name of the file or directory can be relative to the current directory, or a fully qualified name.</span></span>

<span data-ttu-id="7b003-125">Pour télécharger ou placer des fichiers sur un serveur FTP, l’application peut utiliser [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) ou [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (avec [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span><span class="sxs-lookup"><span data-stu-id="7b003-125">To upload or place files on an FTP server, the application can use either [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (along with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span></span> <span data-ttu-id="7b003-126">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) peut être utilisé si le fichier existe déjà localement, tandis que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) et [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) peuvent être utilisés si les données doivent être écrites dans un fichier sur le serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-126">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) can be used if the file already exists locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) can be used if data needs to be written to a file on the FTP server.</span></span>

<span data-ttu-id="7b003-127">Pour télécharger ou récupérer des fichiers, l’application peut utiliser [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) ou [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (avec [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span><span class="sxs-lookup"><span data-stu-id="7b003-127">To download or get files, the application can use either [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span></span> <span data-ttu-id="7b003-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) est utilisé pour récupérer un fichier à partir d’un serveur FTP et le stocker localement, tandis que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) et [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) peuvent être utilisés pour contrôler l’emplacement des informations téléchargées (par exemple, l’application peut afficher les informations dans une zone d’édition).</span><span class="sxs-lookup"><span data-stu-id="7b003-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) is used to retrieve a file from an FTP server and store it locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can be used to control where the downloaded information is going (for example, the application could display the information in an edit box).</span></span>

<span data-ttu-id="7b003-129">Supprimer des fichiers sur un serveur FTP à l’aide de la fonction [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) .</span><span class="sxs-lookup"><span data-stu-id="7b003-129">Delete files on an FTP server by using the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="7b003-130">Cette fonction supprime un nom de fichier relatif au répertoire actif ou à un nom de fichier complet du serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-130">This function removes a file name that is relative either to the current directory or to a fully qualified file name from the FTP server.</span></span> <span data-ttu-id="7b003-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requiert un handle de session retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requires a session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>

## <a name="ftp-function-handles"></a><span data-ttu-id="7b003-132">Handles de fonction FTP</span><span class="sxs-lookup"><span data-stu-id="7b003-132">FTP Function Handles</span></span>

<span data-ttu-id="7b003-133">Pour fonctionner correctement, les fonctions FTP nécessitent certains types de descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="7b003-133">To work properly, the FTP functions require certain types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="7b003-134">Ces handles doivent être créés dans un ordre spécifique, en commençant par le handle racine créé par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="7b003-134">These handles must be created in a specific order, starting with the root handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="7b003-135">[**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) peut ensuite créer un descripteur de session FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) can then create an FTP session handle.</span></span>

<span data-ttu-id="7b003-136">Le diagramme suivant montre les fonctions qui dépendent du descripteur de session FTP retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-136">The following diagram shows the functions that are dependent on the FTP session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="7b003-137">Les zones grisées représentent des fonctions qui retournent des handles [**HINTERNET**](appendix-a-hinternet-handles.md) , tandis que les zones simples représentent des fonctions qui utilisent le descripteur HINTERNET créé par la fonction sur laquelle ils dépendent.</span><span class="sxs-lookup"><span data-stu-id="7b003-137">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the HINTERNET handle created by the function on which they depend.</span></span>

![fonctions FTP dépendant du descripteur de session FTP retourné par internetconnect](images/ax-wnt06.png)

<span data-ttu-id="7b003-139">Le diagramme suivant montre les deux fonctions qui retournent des handles [HINTERNET](appendix-a-hinternet-handles.md) et les fonctions qui en dépendent.</span><span class="sxs-lookup"><span data-stu-id="7b003-139">The following diagram shows the two functions that return [HINTERNET](appendix-a-hinternet-handles.md) handles and the functions that are dependent on them.</span></span> <span data-ttu-id="7b003-140">Les zones grisées représentent des fonctions qui retournent des handles **HINTERNET** , tandis que les zones simples représentent des fonctions qui utilisent le descripteur **HINTERNET** créé par la fonction sur laquelle ils dépendent.</span><span class="sxs-lookup"><span data-stu-id="7b003-140">The shaded boxes represent functions that return **HINTERNET** handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![fonctions FTP qui retournent des handles HINTERNET](images/ax-wnt03.png)

<span data-ttu-id="7b003-142">Pour plus d’informations, consultez [Handles HINTERNET](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="7b003-142">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-for-ftp-sessions"></a><span data-ttu-id="7b003-143">Utilisation des fonctions WinINet pour les sessions FTP</span><span class="sxs-lookup"><span data-stu-id="7b003-143">Using the WinINet Functions for FTP Sessions</span></span>

<span data-ttu-id="7b003-144">Les fonctions suivantes sont utilisées pendant les sessions FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-144">The following functions are used during FTP sessions.</span></span> <span data-ttu-id="7b003-145">Ces fonctions ne sont pas reconnues par les proxys CERN.</span><span class="sxs-lookup"><span data-stu-id="7b003-145">These functions are not recognized by CERN proxies.</span></span> <span data-ttu-id="7b003-146">Les applications qui doivent fonctionner par le biais de proxys CERN doivent utiliser [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) et accéder directement aux ressources.</span><span class="sxs-lookup"><span data-stu-id="7b003-146">Applications that must function through CERN proxies should use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and access the resources directly.</span></span> <span data-ttu-id="7b003-147">Pour plus d’informations sur l’accès direct aux ressources, consultez [accès direct aux URL](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="7b003-147">For more information on direct resource access, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>



| <span data-ttu-id="7b003-148">Fonction</span><span class="sxs-lookup"><span data-stu-id="7b003-148">Function</span></span>                                                 | <span data-ttu-id="7b003-149">Description</span><span class="sxs-lookup"><span data-stu-id="7b003-149">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b003-150">**FtpCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="7b003-150">**FtpCreateDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | <span data-ttu-id="7b003-151">Crée un répertoire sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-151">Creates a new directory on the server.</span></span> <span data-ttu-id="7b003-152">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-152">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                  |
| [<span data-ttu-id="7b003-153">**FtpDeleteFile**</span><span class="sxs-lookup"><span data-stu-id="7b003-153">**FtpDeleteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | <span data-ttu-id="7b003-154">Supprime un fichier du serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-154">Deletes a file from the server.</span></span> <span data-ttu-id="7b003-155">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-155">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                         |
| [<span data-ttu-id="7b003-156">**FtpFindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="7b003-156">**FtpFindFirstFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | <span data-ttu-id="7b003-157">Démarre l’énumération des fichiers ou la recherche de fichiers dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="7b003-157">Starts file enumeration or file search in the current directory.</span></span> <span data-ttu-id="7b003-158">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-158">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>        |
| [<span data-ttu-id="7b003-159">**FtpGetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="7b003-159">**FtpGetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | <span data-ttu-id="7b003-160">Retourne le répertoire actuel du client sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-160">Returns the client's current directory on the server.</span></span> <span data-ttu-id="7b003-161">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-161">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="7b003-162">**FtpGetFile**</span><span class="sxs-lookup"><span data-stu-id="7b003-162">**FtpGetFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | <span data-ttu-id="7b003-163">Récupère un fichier du serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-163">Retrieves a file from the server.</span></span> <span data-ttu-id="7b003-164">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-164">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                       |
| [<span data-ttu-id="7b003-165">**FtpOpenFile**</span><span class="sxs-lookup"><span data-stu-id="7b003-165">**FtpOpenFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | <span data-ttu-id="7b003-166">Initie l’accès à un fichier sur le serveur pour la lecture ou l’écriture.</span><span class="sxs-lookup"><span data-stu-id="7b003-166">Initiates access to a file on the server for either reading or writing.</span></span> <span data-ttu-id="7b003-167">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-167">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> |
| [<span data-ttu-id="7b003-168">**FtpPutFile**</span><span class="sxs-lookup"><span data-stu-id="7b003-168">**FtpPutFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | <span data-ttu-id="7b003-169">Écrit un fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-169">Writes a file to the server.</span></span> <span data-ttu-id="7b003-170">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-170">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                            |
| [<span data-ttu-id="7b003-171">**FtpRemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="7b003-171">**FtpRemoveDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | <span data-ttu-id="7b003-172">Supprime un répertoire sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-172">Deletes a directory on the server.</span></span> <span data-ttu-id="7b003-173">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-173">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                      |
| [<span data-ttu-id="7b003-174">**FtpRenameFile**</span><span class="sxs-lookup"><span data-stu-id="7b003-174">**FtpRenameFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | <span data-ttu-id="7b003-175">Renomme un fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-175">Renames a file on the server.</span></span> <span data-ttu-id="7b003-176">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-176">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                           |
| [<span data-ttu-id="7b003-177">**FtpSetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="7b003-177">**FtpSetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | <span data-ttu-id="7b003-178">Modifie le répertoire actuel du client sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-178">Changes the client's current directory on the server.</span></span> <span data-ttu-id="7b003-179">Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-179">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="7b003-180">**InternetWriteFile**</span><span class="sxs-lookup"><span data-stu-id="7b003-180">**InternetWriteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | <span data-ttu-id="7b003-181">Écrit des données dans un fichier ouvert sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-181">Writes data to an open file on the server.</span></span> <span data-ttu-id="7b003-182">Cette fonction requiert un handle créé par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span><span class="sxs-lookup"><span data-stu-id="7b003-182">This function requires a handle created by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span></span>                                      |



 

### <a name="starting-an-ftp-session"></a><span data-ttu-id="7b003-183">Démarrage d’une session FTP</span><span class="sxs-lookup"><span data-stu-id="7b003-183">Starting an FTP Session</span></span>

<span data-ttu-id="7b003-184">L’application établit une session FTP en appelant [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) sur un handle créé par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="7b003-184">The application establishes an FTP session by calling [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) on a handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="7b003-185">[**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) a besoin du nom du serveur, du numéro de port, du nom d’utilisateur, du mot de passe et du type de service (qui doit être défini sur Internet \_ service \_ FTP).</span><span class="sxs-lookup"><span data-stu-id="7b003-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) needs the server name, port number, user name, password, and service type (which must be set to INTERNET\_SERVICE\_FTP).</span></span> <span data-ttu-id="7b003-186">Pour la sémantique FTP passive, l’application doit également définir l’indicateur [ \_ \_ passive de l’indicateur Internet](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="7b003-186">For passive FTP semantics, the application must also set the [INTERNET\_FLAG\_PASSIVE](api-flags.md) flag.</span></span>

<span data-ttu-id="7b003-187">Les \_ valeurs de port FTP par défaut Internet \_ \_ et \_ \_ de numéro de port Internet non valides \_ peuvent être utilisées pour le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="7b003-187">The INTERNET\_DEFAULT\_FTP\_PORT and INTERNET\_INVALID\_PORT\_NUMBER values can be used for the port number.</span></span> <span data-ttu-id="7b003-188">Le \_ port FTP par défaut Internet \_ \_ utilise le port FTP par défaut, mais le type de service doit toujours être défini.</span><span class="sxs-lookup"><span data-stu-id="7b003-188">INTERNET\_DEFAULT\_FTP\_PORT uses the default FTP port, but the service type still must be set.</span></span> <span data-ttu-id="7b003-189">\_ \_ Le numéro de port Internet non valide \_ utilise la valeur par défaut pour le type de service indiqué.</span><span class="sxs-lookup"><span data-stu-id="7b003-189">INTERNET\_INVALID\_PORT\_NUMBER uses the default value for the indicated service type.</span></span>

<span data-ttu-id="7b003-190">Les valeurs du nom d’utilisateur et du mot de passe peuvent être définies sur **null**.</span><span class="sxs-lookup"><span data-stu-id="7b003-190">The values for the user name and password can be set to **NULL**.</span></span> <span data-ttu-id="7b003-191">Si les deux valeurs sont définies sur **null**, [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilise « Anonymous » pour le nom d’utilisateur et l’adresse de messagerie de l’utilisateur pour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7b003-191">If both values are set to **NULL**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses "anonymous" for the user name, and the user's email address for the password.</span></span> <span data-ttu-id="7b003-192">Si seul le mot de passe est défini sur **null**, le nom d’utilisateur passé à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) est utilisé pour le nom d’utilisateur et une chaîne vide est utilisée pour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7b003-192">If only the password is set to **NULL**, the user name passed to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) is used for the user name, and an empty string is used for the password.</span></span> <span data-ttu-id="7b003-193">Si aucune valeur n’est **null**, le nom d’utilisateur et le mot de passe fournis à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="7b003-193">If neither value is **NULL**, the user name and password given to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) are used.</span></span>

### <a name="enumerating-directories"></a><span data-ttu-id="7b003-194">Énumération des répertoires</span><span class="sxs-lookup"><span data-stu-id="7b003-194">Enumerating Directories</span></span>

<span data-ttu-id="7b003-195">L’énumération d’un répertoire sur un serveur FTP requiert la création d’un descripteur par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="7b003-195">Enumeration of a directory on an FTP server requires the creation of a handle by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="7b003-196">Ce descripteur est une branche du descripteur de session créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-196">This handle is a branch of the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="7b003-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) localise le premier fichier ou répertoire sur le serveur et le retourne dans une structure de [**\_ \_ données de recherche Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) .</span><span class="sxs-lookup"><span data-stu-id="7b003-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) locates the first file or directory on the server and returns it in a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="7b003-198">Utilisez [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) jusqu’à ce qu’il retourne l' [**erreur \_ aucun \_ \_ fichier supplémentaire**](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="7b003-198">Use [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until it returns [**ERROR\_NO\_MORE\_FILES**](wininet-errors.md).</span></span> <span data-ttu-id="7b003-199">Cette méthode recherche tous les fichiers et répertoires suivants sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-199">This method finds all subsequent files and directories on the server.</span></span> <span data-ttu-id="7b003-200">Pour plus d’informations sur [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), consultez [recherche du fichier suivant](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7b003-200">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="7b003-201">Pour déterminer si le fichier récupéré par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) ou [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) est un répertoire, vérifiez le membre **dwFileAttributes** de la structure de [**\_ \_ données de recherche Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) pour déterminer s’il est égal au répertoire des attributs de fichier \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b003-201">To determine if the file retrieved by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) or [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) is a directory, check the **dwFileAttributes** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure to see if it is equal to FILE\_ATTRIBUTE\_DIRECTORY.</span></span>

<span data-ttu-id="7b003-202">Si l’application apporte des modifications sur le serveur FTP ou si le serveur FTP change fréquemment, les indicateurs de rechargement de l' [ \_ indicateur Internet \_ sans \_ cache \_](api-flags.md) et de l' [indicateur de \_ \_ rechargement Internet](api-flags.md) doivent être définis dans [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="7b003-202">If the application makes changes on the FTP server or if the FTP server changes frequently, the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) and [INTERNET\_FLAG\_RELOAD](api-flags.md) flags should be set in [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="7b003-203">Ces indicateurs garantissent que les informations de répertoire récupérées à partir du serveur FTP sont à jour.</span><span class="sxs-lookup"><span data-stu-id="7b003-203">These flags ensure that the directory information being retrieved from the FTP server is current.</span></span>

<span data-ttu-id="7b003-204">Une fois que l’application a terminé l’énumération de répertoires, l’application doit effectuer un appel à [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) sur le handle créé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="7b003-204">After the application completes the directory enumeration, the application must make a call to [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle created by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="7b003-205">Tant que ce handle n’est pas fermé, l’application ne peut pas appeler à nouveau [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) sur le handle de session créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-205">Until that handle is closed, the application cannot call [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) again on the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="7b003-206">Si un appel à [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) est effectué sur le même handle de session avant la fermeture de l’appel précédent à la même fonction, la fonction échoue et retourne l' [erreur \_ \_ transfert FTP \_ en \_ cours](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="7b003-206">If a call to [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) is made on the same session handle before the previous call to the same function is closed, the function fails, returning [ERROR\_FTP\_TRANSFER\_IN\_PROGRESS](wininet-errors.md).</span></span>

<span data-ttu-id="7b003-207">L’exemple suivant énumère le contenu d’un répertoire FTP dans un contrôle de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="7b003-207">The following example enumerates the contents of an FTP directory into a list box control.</span></span> <span data-ttu-id="7b003-208">Le paramètre *hConnection* est un handle retourné par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après avoir établi une session FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-208">The *hConnection* parameter is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span> <span data-ttu-id="7b003-209">Vous trouverez un exemple de code source pour la fonction InternetErrorOut référencée dans cet exemple dans la rubrique [gestion des erreurs](appendix-c-handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="7b003-209">Sample source code for the InternetErrorOut function referenced in this example can be found in the [Handling Errors](appendix-c-handling-errors.md)topic.</span></span>


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a><span data-ttu-id="7b003-210">Navigation dans les répertoires</span><span class="sxs-lookup"><span data-stu-id="7b003-210">Navigating Directories</span></span>

<span data-ttu-id="7b003-211">Les fonctions [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) et [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) gèrent la navigation dans les répertoires.</span><span class="sxs-lookup"><span data-stu-id="7b003-211">The [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions handle directory navigation.</span></span>

<span data-ttu-id="7b003-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) retourne le répertoire actif de l’application sur le serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) returns the application's current directory on the FTP server.</span></span> <span data-ttu-id="7b003-213">Le chemin d’accès au répertoire à partir du répertoire racine sur le serveur FTP est inclus.</span><span class="sxs-lookup"><span data-stu-id="7b003-213">The directory path from the root directory on the FTP server is included.</span></span>

<span data-ttu-id="7b003-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) modifie le répertoire de travail sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the working directory on the server.</span></span> <span data-ttu-id="7b003-215">Les informations de répertoire transmises à [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) peuvent être un nom de chemin d’accès partiel ou complet relatif au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="7b003-215">The directory information passed to [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) can be either a partially or fully qualified path name relative to the current directory.</span></span> <span data-ttu-id="7b003-216">Par exemple, si l’application se trouve actuellement dans le répertoire « public/info » et que le chemin d’accès est « FTP/example », [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) remplace le répertoire actif par « public/info/FTP/example ».</span><span class="sxs-lookup"><span data-stu-id="7b003-216">For example, if the application is currently in the directory "public/info" and the path is "ftp/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the current directory to "public/info/ftp/example".</span></span>

<span data-ttu-id="7b003-217">L’exemple suivant utilise le handle de session FTP hConnection, qui est retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="7b003-217">The following example uses the FTP session handle hConnection, which is returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="7b003-218">Le nouveau nom de répertoire est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est transmis dans le paramètre *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="7b003-218">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="7b003-219">Avant que le répertoire ne soit modifié, la fonction récupère le répertoire actif et le stocke dans la même zone d’édition.</span><span class="sxs-lookup"><span data-stu-id="7b003-219">Before the directory change is made, the function retrieves the current directory and stores it in the same edit box.</span></span> <span data-ttu-id="7b003-220">Le code de la fonction DisplayFtpDir appelée à la fin est indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7b003-220">The souce code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a><span data-ttu-id="7b003-221">Manipulation de répertoires sur un serveur FTP</span><span class="sxs-lookup"><span data-stu-id="7b003-221">Manipulating Directories on an FTP Server</span></span>

<span data-ttu-id="7b003-222">WinINet offre la possibilité de créer et de supprimer des répertoires sur un serveur FTP auquel l’application dispose des privilèges nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7b003-222">WinINet provides the capability to create and remove directories on an FTP server to which the application has the necessary privileges.</span></span> <span data-ttu-id="7b003-223">Si l’application doit ouvrir une session sur un serveur avec un nom d’utilisateur et un mot de passe spécifiques, les valeurs peuvent être utilisées dans [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) lors de la création du descripteur de session FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-223">If the application must log on to a server with a specific user name and password, the values can be used in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) when creating the FTP session handle.</span></span>

<span data-ttu-id="7b003-224">La fonction [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) prend un handle de session FTP valide et une chaîne se terminant par un caractère **null** qui contient un chemin d’accès qualifié complet ou un nom relatif au répertoire actif et crée un répertoire sur le serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-224">The [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function takes a valid FTP session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and creates a directory on the FTP server.</span></span>

<span data-ttu-id="7b003-225">L’exemple suivant montre deux appels distincts à [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span><span class="sxs-lookup"><span data-stu-id="7b003-225">The following example shows two separate calls to [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span></span> <span data-ttu-id="7b003-226">Dans les deux exemples, hFtpSession est le descripteur de session créé par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) et le répertoire racine est le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="7b003-226">In both examples, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span>

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

<span data-ttu-id="7b003-227">La fonction [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) prend un handle de session et une chaîne se terminant par un caractère **null** qui contient un chemin d’accès qualifié complet ou un nom relatif au répertoire actif et supprime ce répertoire du serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-227">The [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) function takes a session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and removes that directory from the FTP server.</span></span>

<span data-ttu-id="7b003-228">L’exemple suivant montre deux exemples d’appels à [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span><span class="sxs-lookup"><span data-stu-id="7b003-228">The following example shows two sample calls to [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span></span> <span data-ttu-id="7b003-229">Dans les deux appels, hFtpSession est le descripteur de session créé par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) et le répertoire racine est le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="7b003-229">In both calls, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span> <span data-ttu-id="7b003-230">Il existe un répertoire nommé « test » dans le répertoire racine et un répertoire appelé « example » dans le répertoire « test ».</span><span class="sxs-lookup"><span data-stu-id="7b003-230">There is a directory called "test" in the root directory and a directory called "example" in the "test" directory.</span></span>

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



<span data-ttu-id="7b003-231">L’exemple suivant crée un répertoire sur le serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-231">The following example creates a new directory on the FTP server.</span></span> <span data-ttu-id="7b003-232">Le nouveau nom de répertoire est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est transmis dans le paramètre *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="7b003-232">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="7b003-233">Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-233">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="7b003-234">Le code source de la fonction DisplayFtpDir appelée à la fin est indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7b003-234">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



<span data-ttu-id="7b003-235">L’exemple suivant supprime un répertoire du serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-235">The following example deletes a directory from the FTP server.</span></span> <span data-ttu-id="7b003-236">Le nom du répertoire à supprimer est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est passé dans le paramètre *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="7b003-236">The name of the directory to be deleted is taken from the edit box in the parent dialog whose IDC is passed into the *nDirNameId* parameter.</span></span> <span data-ttu-id="7b003-237">Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-237">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="7b003-238">Le code source de la fonction DisplayFtpDir appelée à la fin est indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7b003-238">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a><span data-ttu-id="7b003-239">Obtention de fichiers sur un serveur FTP</span><span class="sxs-lookup"><span data-stu-id="7b003-239">Getting Files on an FTP Server</span></span>

<span data-ttu-id="7b003-240">Il existe trois méthodes pour récupérer des fichiers à partir d’un serveur FTP :</span><span class="sxs-lookup"><span data-stu-id="7b003-240">There are three methods for retrieving files from an FTP server:</span></span>

-   <span data-ttu-id="7b003-241">Utilisez [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) et [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="7b003-241">Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="7b003-242">Utilisez [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) et [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="7b003-242">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="7b003-243">Utilisez [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span><span class="sxs-lookup"><span data-stu-id="7b003-243">Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span></span>

<span data-ttu-id="7b003-244">Pour plus d’informations sur l’utilisation de la fonction [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) , consultez [lecture de fichiers](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7b003-244">For more information about using the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function, see [Reading Files](common-functions.md).</span></span>

<span data-ttu-id="7b003-245">Si l’URL du fichier est disponible, l’application peut appeler [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pour se connecter à cette URL, puis utiliser [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) pour contrôler le téléchargement du fichier.</span><span class="sxs-lookup"><span data-stu-id="7b003-245">If the URL of the file is available, the application can call [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to connect to that URL, then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to control the download of the file.</span></span> <span data-ttu-id="7b003-246">Cela permet à l’application d’exercer un contrôle plus strict sur le téléchargement et est idéal pour les situations où aucune autre opération ne doit être effectuée sur le serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-246">This allows the application tighter control over the download and is ideal for situations where no other operations need to be made on the FTP server.</span></span> <span data-ttu-id="7b003-247">Pour plus d’informations sur l’accès direct aux ressources, consultez [accès direct aux URL](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="7b003-247">For more information about how to directly access resources, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="7b003-248">Si l’application a établi un descripteur de session FTP sur le serveur avec [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), l’application peut appeler [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) avec le nom de fichier existant et avec un nouveau nom pour le fichier stocké localement.</span><span class="sxs-lookup"><span data-stu-id="7b003-248">If the application has established an FTP session handle to the server with [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), the application can call [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with the existing file name and with a new name for the locally stored file.</span></span> <span data-ttu-id="7b003-249">L’application peut ensuite utiliser [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) pour télécharger le fichier.</span><span class="sxs-lookup"><span data-stu-id="7b003-249">The application can then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to download the file.</span></span> <span data-ttu-id="7b003-250">Cela permet à l’application d’exercer un contrôle plus strict sur le téléchargement et de conserver la connexion au serveur FTP, si bien que davantage de commandes peuvent être exécutées.</span><span class="sxs-lookup"><span data-stu-id="7b003-250">This allows the application tighter control over the download and keeps the connection to the FTP server, so more commands can be executed.</span></span>

<span data-ttu-id="7b003-251">Si l’application n’a pas besoin d’un contrôle strict sur le téléchargement, l’application peut utiliser [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) avec le descripteur de session FTP, le nom de fichier distant et le nom de fichier local pour récupérer le fichier.</span><span class="sxs-lookup"><span data-stu-id="7b003-251">If the application does not need tight control over the download, the application can use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) with the FTP session handle, remote file name, and local file name to retrieve the file.</span></span> <span data-ttu-id="7b003-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) effectue toutes les tâches de comptabilité et de surcharge associées à la lecture d’un fichier à partir d’un serveur FTP et à son stockage local.</span><span class="sxs-lookup"><span data-stu-id="7b003-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) performs all the bookkeeping and overhead associated with reading a file from an FTP server and storing it locally.</span></span>

<span data-ttu-id="7b003-253">L’exemple suivant récupère un fichier à partir d’un serveur FTP et l’enregistre localement.</span><span class="sxs-lookup"><span data-stu-id="7b003-253">The following example retrieves a file from an FTP server and saves it locally.</span></span> <span data-ttu-id="7b003-254">Le nom du fichier sur le serveur FTP est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est transmis dans le paramètre *nFtpFileNameId* , et le nom local sous lequel le fichier est enregistré est extrait de la zone d’édition dont l’IDC est transmis dans le paramètre *nLocalFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="7b003-254">The name of the file on the FTP server is taken from the edit box in the parent dialog whose IDC is passed in the *nFtpFileNameId* parameter, and the local name under which the file is saved is taken from the edit box whose IDC is passed in the *nLocalFileNameId* parameter.</span></span> <span data-ttu-id="7b003-255">Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-255">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a><span data-ttu-id="7b003-256">Placement de fichiers sur un serveur FTP</span><span class="sxs-lookup"><span data-stu-id="7b003-256">Placing Files on an FTP Server</span></span>

<span data-ttu-id="7b003-257">Il existe deux méthodes pour placer un fichier sur un serveur FTP :</span><span class="sxs-lookup"><span data-stu-id="7b003-257">There are two methods for placing a file on an FTP server:</span></span>

-   <span data-ttu-id="7b003-258">Utilisez [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) avec [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span><span class="sxs-lookup"><span data-stu-id="7b003-258">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span></span>
-   <span data-ttu-id="7b003-259">Utilisez [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="7b003-259">Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>

<span data-ttu-id="7b003-260">Une application qui doit envoyer des données à un serveur FTP, mais qui n’a pas de fichier local contenant toutes les données, doit utiliser [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) pour créer et ouvrir un fichier sur le serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-260">An application that must send data to an FTP server, but does not have a local file that contains all the data, should use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) to create and open a file on the ftp server.</span></span> <span data-ttu-id="7b003-261">L’application peut ensuite utiliser [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) pour télécharger les informations dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="7b003-261">The application then can use [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) to upload the information to the file.</span></span>

<span data-ttu-id="7b003-262">Si le fichier existe déjà localement, l’application peut utiliser [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) pour charger le fichier sur le serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-262">If the file already exists locally, the application can use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) to upload the file to the FTP server.</span></span> <span data-ttu-id="7b003-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) effectue toute la surcharge liée au téléchargement d’un fichier local sur un serveur FTP distant.</span><span class="sxs-lookup"><span data-stu-id="7b003-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) performs all the overhead that goes with uploading a local file to a remote FTP server.</span></span>

<span data-ttu-id="7b003-264">L’exemple suivant copie un fichier local sur le serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-264">The following example copies a local file onto the FTP server.</span></span> <span data-ttu-id="7b003-265">Le nom local du fichier est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est transmis dans le paramètre *nLocalFileNameId* , et le nom sous lequel le fichier est enregistré sur le serveur FTP est extrait de la zone d’édition dont l’IDC est transmis dans le paramètre *nFtpFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="7b003-265">The local name of the file is taken from the edit box in the parent dialog whose IDC is passed in the *nLocalFileNameId* parameter, and the name under which the file is saved on the FTP server is taken from the edit box whose IDC is passed in the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="7b003-266">Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-266">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a><span data-ttu-id="7b003-267">Suppression de fichiers d’un serveur FTP</span><span class="sxs-lookup"><span data-stu-id="7b003-267">Deleting Files from an FTP Server</span></span>

<span data-ttu-id="7b003-268">Pour supprimer un fichier d’un serveur FTP, utilisez la fonction [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) .</span><span class="sxs-lookup"><span data-stu-id="7b003-268">To delete a file from an FTP server, use the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="7b003-269">L’application appelante doit disposer des privilèges nécessaires pour supprimer un fichier du serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-269">The calling application must have the necessary privileges to delete a file from the FTP server.</span></span>

<span data-ttu-id="7b003-270">L’exemple suivant supprime un fichier du serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-270">The following example deletes a file from the FTP server.</span></span> <span data-ttu-id="7b003-271">Le nom du fichier à supprimer est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC reçoit le paramètre *nFtpFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="7b003-271">The name of the file to be deleted is taken from the edit box in the parent dialog whose IDC is passed int the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="7b003-272">Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-272">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="7b003-273">Étant donné que cette fonction n’actualise pas les listes de fichiers ou l’affichage des répertoires, le processus appelant doit le faire en cas de suppression réussie.</span><span class="sxs-lookup"><span data-stu-id="7b003-273">Since this function does not refresh file listings or directory display, the calling process should do so upon successful deletion.</span></span>


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a><span data-ttu-id="7b003-274">Attribution d’un nouveau nom aux fichiers et répertoires sur un serveur FTP</span><span class="sxs-lookup"><span data-stu-id="7b003-274">Renaming Files and Directories on an FTP Server</span></span>

<span data-ttu-id="7b003-275">Vous pouvez renommer les fichiers et répertoires d’un serveur FTP à l’aide de la fonction [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) .</span><span class="sxs-lookup"><span data-stu-id="7b003-275">Files and directories on an FTP server can be renamed using the [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) function.</span></span> <span data-ttu-id="7b003-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accepte deux chaînes se terminant par un caractère **null** qui contiennent des noms complets ou partiels par rapport au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="7b003-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accepts two **null**-terminated strings that contain either partially or fully qualified names relative to the current directory.</span></span> <span data-ttu-id="7b003-277">La fonction modifie le nom du fichier désigné par la première chaîne en lui assignant le nom désigné par la deuxième chaîne.</span><span class="sxs-lookup"><span data-stu-id="7b003-277">The function changes the name of the file designated by the first string to the name designated by the second string.</span></span>

<span data-ttu-id="7b003-278">L’exemple suivant renomme un fichier ou un répertoire sur le serveur FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-278">The following example renames a file or directory on the FTP server.</span></span> <span data-ttu-id="7b003-279">Le nom actuel du fichier ou du répertoire est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est transmis dans le paramètre *nOldFileNameId* , et le nouveau nom est extrait de la zone d’édition dont l’IDC est passé dans le paramètre *nNewFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="7b003-279">The current name of the file or directory is taken from the edit box in the parent dialog whose IDC is passed in the *nOldFileNameId* parameter, and the new name is taken from the edit box whose IDC is passed in the *nNewFileNameId* parameter.</span></span> <span data-ttu-id="7b003-280">Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP.</span><span class="sxs-lookup"><span data-stu-id="7b003-280">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="7b003-281">Étant donné que cette fonction n’actualise pas les listes de fichiers ou l’affichage des répertoires, le processus appelant doit le faire en cas de changement de nom.</span><span class="sxs-lookup"><span data-stu-id="7b003-281">Since this function does not refresh file listings or directory display, the calling process should do so upon successful renaming.</span></span>


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> <span data-ttu-id="7b003-282">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="7b003-282">WinINet does not support server implementations.</span></span> <span data-ttu-id="7b003-283">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="7b003-283">In addition, it should not be used from a service.</span></span> <span data-ttu-id="7b003-284">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="7b003-284">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 