---
title: Fonctions courantes (Windows Internet)
description: Les différents protocoles Internet (tels que FTP et http) utilisent plusieurs des mêmes fonctions WinINet pour gérer les informations sur Internet.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1893b085da1b3e77228e4a9abf75acc166d84726
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106510107"
---
# <a name="common-functions-windows-internet"></a><span data-ttu-id="c22c2-103">Fonctions courantes (Windows Internet)</span><span class="sxs-lookup"><span data-stu-id="c22c2-103">Common Functions (Windows Internet)</span></span>

<span data-ttu-id="c22c2-104">Les différents protocoles Internet (tels que FTP et http) utilisent plusieurs des mêmes fonctions WinINet pour gérer les informations sur Internet.</span><span class="sxs-lookup"><span data-stu-id="c22c2-104">The different Internet protocols (such as ftp and http) use several of the same WinINet functions to handle information on the Internet.</span></span> <span data-ttu-id="c22c2-105">Ces fonctions courantes gèrent leurs tâches de manière cohérente, quel que soit le protocole auquel elles s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="c22c2-105">These common functions handle their tasks in a consistent manner, regardless of the particular protocol to which they are being applied.</span></span> <span data-ttu-id="c22c2-106">Les applications peuvent utiliser ces fonctions pour créer des fonctions à usage général qui gèrent les tâches entre les différents protocoles (telles que la lecture de fichiers pour FTP et http).</span><span class="sxs-lookup"><span data-stu-id="c22c2-106">Applications can use these functions to create general-purpose functions that handle tasks across the different protocols (such as reading files for ftp and http).</span></span>

<span data-ttu-id="c22c2-107">Les fonctions courantes gèrent les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c22c2-107">The common functions handle the following tasks:</span></span>

-   <span data-ttu-id="c22c2-108">Téléchargement des ressources à partir d’Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)et [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span><span class="sxs-lookup"><span data-stu-id="c22c2-108">Downloading resources from the Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), and [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span></span>
-   <span data-ttu-id="c22c2-109">Configuration des opérations asynchrones ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span><span class="sxs-lookup"><span data-stu-id="c22c2-109">Setting up asynchronous operations ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span></span>
-   <span data-ttu-id="c22c2-110">Affichage et modification des options ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) et [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span><span class="sxs-lookup"><span data-stu-id="c22c2-110">Viewing and changing options ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span></span>
-   <span data-ttu-id="c22c2-111">Fermeture de tous les types de handles [**HINTERNET**](appendix-a-hinternet-handles.md) ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span><span class="sxs-lookup"><span data-stu-id="c22c2-111">Closing all types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span></span>
-   <span data-ttu-id="c22c2-112">Placement et suppression de verrous sur les ressources ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) et [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span><span class="sxs-lookup"><span data-stu-id="c22c2-112">Placing and removing locks on resources ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) and [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span></span>

## <a name="using-common-functions"></a><span data-ttu-id="c22c2-113">Utilisation des fonctions courantes</span><span class="sxs-lookup"><span data-stu-id="c22c2-113">Using Common Functions</span></span>

<span data-ttu-id="c22c2-114">Le tableau suivant répertorie les fonctions courantes incluses dans les fonctions WinINet.</span><span class="sxs-lookup"><span data-stu-id="c22c2-114">The following table lists the common functions included in the WinINet functions.</span></span> <span data-ttu-id="c22c2-115">Les fonctions courantes peuvent être utilisées sur différents types de descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) ou peuvent être utilisées dans différents types de sessions.</span><span class="sxs-lookup"><span data-stu-id="c22c2-115">The common functions can be used on different types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles or can be used during different types of sessions.</span></span>



| <span data-ttu-id="c22c2-116">Fonction</span><span class="sxs-lookup"><span data-stu-id="c22c2-116">Function</span></span>                                                         | <span data-ttu-id="c22c2-117">Description</span><span class="sxs-lookup"><span data-stu-id="c22c2-117">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c22c2-118">**InternetFindNextFile**</span><span class="sxs-lookup"><span data-stu-id="c22c2-118">**InternetFindNextFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | <span data-ttu-id="c22c2-119">Poursuit l’énumération des fichiers ou la recherche.</span><span class="sxs-lookup"><span data-stu-id="c22c2-119">Continues file enumeration or search.</span></span> <span data-ttu-id="c22c2-120">Requiert un handle créé par la fonction [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-120">Requires a handle created by the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span>                                                                            |
| [<span data-ttu-id="c22c2-121">**InternetLockRequestFile**</span><span class="sxs-lookup"><span data-stu-id="c22c2-121">**InternetLockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | <span data-ttu-id="c22c2-122">Permet à l’utilisateur de placer un verrou sur le fichier utilisé.</span><span class="sxs-lookup"><span data-stu-id="c22c2-122">Allows the user to place a lock on the file that is being used.</span></span> <span data-ttu-id="c22c2-123">Cette fonction requiert un handle retourné par la fonction [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-123">This function requires a handle returned by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="c22c2-124">**InternetQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="c22c2-124">**InternetQueryDataAvailable**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | <span data-ttu-id="c22c2-125">Récupère la quantité de données disponibles.</span><span class="sxs-lookup"><span data-stu-id="c22c2-125">Retrieves the amount of data available.</span></span> <span data-ttu-id="c22c2-126">Requiert un handle créé par la fonction [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-126">Requires a handle created by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                                    |
| [<span data-ttu-id="c22c2-127">**InternetQueryOption**</span><span class="sxs-lookup"><span data-stu-id="c22c2-127">**InternetQueryOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | <span data-ttu-id="c22c2-128">Récupère le paramètre d’une option Internet.</span><span class="sxs-lookup"><span data-stu-id="c22c2-128">Retrieves the setting of an Internet option.</span></span>                                                                                                                                                                                                            |
| [<span data-ttu-id="c22c2-129">**InternetReadFile**</span><span class="sxs-lookup"><span data-stu-id="c22c2-129">**InternetReadFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | <span data-ttu-id="c22c2-130">Lit les données d’URL.</span><span class="sxs-lookup"><span data-stu-id="c22c2-130">Reads URL data.</span></span> <span data-ttu-id="c22c2-131">Requiert un handle créé par la fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-131">Requires a handle created by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                |
| [<span data-ttu-id="c22c2-132">**InternetSetFilePointer**</span><span class="sxs-lookup"><span data-stu-id="c22c2-132">**InternetSetFilePointer**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | <span data-ttu-id="c22c2-133">Définit la position de la lecture suivante dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="c22c2-133">Sets the position for the next read in a file.</span></span> <span data-ttu-id="c22c2-134">Requiert un handle créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (sur une URL http uniquement) ou un descripteur créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) à l’aide du verbe http obtenir.</span><span class="sxs-lookup"><span data-stu-id="c22c2-134">Requires a handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (on an HTTP URL only) or a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) using the GET HTTP verb.</span></span>                 |
| [<span data-ttu-id="c22c2-135">**InternetSetOption**</span><span class="sxs-lookup"><span data-stu-id="c22c2-135">**InternetSetOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | <span data-ttu-id="c22c2-136">Définit une option Internet.</span><span class="sxs-lookup"><span data-stu-id="c22c2-136">Sets an Internet option.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="c22c2-137">**InternetSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="c22c2-137">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | <span data-ttu-id="c22c2-138">Définit une fonction de rappel qui reçoit des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="c22c2-138">Sets a callback function that receives status information.</span></span> <span data-ttu-id="c22c2-139">Assigne une fonction de rappel au handle [**HINTERNET**](appendix-a-hinternet-handles.md) désigné et à tous les handles dérivés de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c22c2-139">Assigns a callback function to the designated [**HINTERNET**](appendix-a-hinternet-handles.md) handle and all handles derived from it.</span></span>                                                      |
| [<span data-ttu-id="c22c2-140">**InternetUnlockRequestFile**</span><span class="sxs-lookup"><span data-stu-id="c22c2-140">**InternetUnlockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | <span data-ttu-id="c22c2-141">Déverrouille un fichier qui a été verrouillé à l’aide de la fonction [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-141">Unlocks a file that was locked using the [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function.</span></span>                                                                                                                                           |



 

<span data-ttu-id="c22c2-142">La lecture des fichiers, la recherche du fichier suivant, la manipulation des options et la configuration d’opérations asynchrones sont communes aux fonctions qui prennent en charge divers protocoles et types de descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-142">Reading files, finding the next file, manipulating options, and setting up asynchronous operations are common to the functions that support various protocols and [**HINTERNET**](appendix-a-hinternet-handles.md) handle types.</span></span>

### <a name="reading-files"></a><span data-ttu-id="c22c2-143">Lecture des fichiers</span><span class="sxs-lookup"><span data-stu-id="c22c2-143">Reading Files</span></span>

<span data-ttu-id="c22c2-144">La fonction [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) est utilisée pour télécharger des ressources à partir d’un handle [**HINTERNET**](appendix-a-hinternet-handles.md) retourné par la fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-144">The [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function is used to download resources from an [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>

<span data-ttu-id="c22c2-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accepte une variable de pointeur void qui contient l’adresse d’une mémoire tampon et un pointeur vers une variable qui contient la longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c22c2-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accepts a void pointer variable that contains the address of a buffer and a pointer to a variable that contains the length of the buffer.</span></span> <span data-ttu-id="c22c2-146">La fonction retourne les données dans la mémoire tampon et la quantité de données téléchargées dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c22c2-146">The function returns the data in the buffer and the amount of data downloaded into the buffer.</span></span>

<span data-ttu-id="c22c2-147">Les fonctions WinINet fournissent deux techniques pour télécharger une ressource entière :</span><span class="sxs-lookup"><span data-stu-id="c22c2-147">The WinINet functions provide two techniques to download an entire resource:</span></span>

-   <span data-ttu-id="c22c2-148">Fonction [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-148">The [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) function.</span></span>
-   <span data-ttu-id="c22c2-149">Valeurs de retour de [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="c22c2-149">The return values of [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>

<span data-ttu-id="c22c2-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) prend le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (après que [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) a été appelé sur le descripteur) et retourne le nombre d’octets disponibles.</span><span class="sxs-lookup"><span data-stu-id="c22c2-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) has been called on the handle) and returns the number of bytes available.</span></span> <span data-ttu-id="c22c2-151">L’application doit allouer une mémoire tampon égale au nombre d’octets disponibles, plus 1 pour le caractère **null** de fin, et utiliser cette mémoire tampon avec [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="c22c2-151">The application should allocate a buffer equal to the number of bytes available, plus 1 for the terminating **null** character, and use that buffer with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="c22c2-152">Cette méthode ne fonctionne pas toujours, car [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) vérifie la taille de fichier indiquée dans l’en-tête, et non le fichier réel.</span><span class="sxs-lookup"><span data-stu-id="c22c2-152">This method does not always work because [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) is checking the file size listed in the header and not the actual file.</span></span> <span data-ttu-id="c22c2-153">Les informations contenues dans le fichier d’en-tête peuvent être obsolètes ou le fichier d’en-tête peut être manquant, car il n’est actuellement pas requis dans toutes les normes.</span><span class="sxs-lookup"><span data-stu-id="c22c2-153">The information in the header file could be outdated, or the header file could be missing, since it is not currently required under all standards.</span></span>

<span data-ttu-id="c22c2-154">L’exemple suivant lit le contenu de la ressource accessible par le handle hResource et affiché dans la zone d’édition indiquée par intCtrlID.</span><span class="sxs-lookup"><span data-stu-id="c22c2-154">The following example reads the contents of the resource accessed by the hResource handle and displayed in the edit box indicated by intCtrlID.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    // Return.
    return TRUE;
}
```



<span data-ttu-id="c22c2-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) retourne une lecture de zéro octet et se termine avec succès lorsque toutes les données disponibles ont été lues.</span><span class="sxs-lookup"><span data-stu-id="c22c2-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) returns zero bytes read and completes successfully when all available data has been read.</span></span> <span data-ttu-id="c22c2-156">Cela permet à une application d’utiliser [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) dans une boucle pour télécharger les données et de quitter lorsqu’elle retourne zéro octet de lecture et se termine correctement.</span><span class="sxs-lookup"><span data-stu-id="c22c2-156">This allows an application to use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) in a loop to download the data and exit when it returns zero bytes read and completes successfully.</span></span>

<span data-ttu-id="c22c2-157">L’exemple suivant lit la ressource à partir d’Internet et affiche la ressource dans la zone d’édition indiquée par intCtrlID.</span><span class="sxs-lookup"><span data-stu-id="c22c2-157">The following example reads the resource from the Internet and displays the resource in the edit box indicated by intCtrlID.</span></span> <span data-ttu-id="c22c2-158">Le handle [**HINTERNET**](appendix-a-hinternet-handles.md) , HINTERNET, a été retourné [**par InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (après envoi par [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span><span class="sxs-lookup"><span data-stu-id="c22c2-158">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hInternet, was returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after being sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span></span>


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a><span data-ttu-id="c22c2-159">Recherche du fichier suivant</span><span class="sxs-lookup"><span data-stu-id="c22c2-159">Finding the Next File</span></span>

<span data-ttu-id="c22c2-160">La fonction [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) est utilisée pour rechercher le fichier suivant dans une recherche de fichiers, à l’aide des paramètres de recherche et du handle [**HINTERNET**](appendix-a-hinternet-handles.md) de [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="c22c2-160">The [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) function is used to find the next file in a file search, using the search parameters and [**HINTERNET**](appendix-a-hinternet-handles.md) handle from [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="c22c2-161">Pour effectuer une recherche de fichier, continuez à appeler [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) à l’aide du handle [**HINTERNET**](appendix-a-hinternet-handles.md) retourné par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) jusqu’à ce que la fonction échoue avec le message d’erreur étendu erreur, plus [ \_ aucun \_ \_ fichier](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c22c2-161">To complete a file search, continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) using the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) until the function fails with the extended error message [ERROR\_NO\_MORE\_FILES](wininet-errors.md).</span></span> <span data-ttu-id="c22c2-162">Pour récupérer les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-162">To get the extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="c22c2-163">L’exemple suivant affiche le contenu d’un répertoire FTP dans la zone de liste indiquée par lstDirectory.</span><span class="sxs-lookup"><span data-stu-id="c22c2-163">The following example displays the contents of an FTP directory in the list box indicated by lstDirectory.</span></span> <span data-ttu-id="c22c2-164">Le handle [**HINTERNET**](appendix-a-hinternet-handles.md) , hConnect, est un handle retourné par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après avoir établi une session FTP.</span><span class="sxs-lookup"><span data-stu-id="c22c2-164">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hConnect, is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span>


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a><span data-ttu-id="c22c2-165">Manipulation des options</span><span class="sxs-lookup"><span data-stu-id="c22c2-165">Manipulating Options</span></span>

<span data-ttu-id="c22c2-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) et [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) sont utilisées pour manipuler les options wininet.</span><span class="sxs-lookup"><span data-stu-id="c22c2-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) are used to manipulate the WinINet options.</span></span>

<span data-ttu-id="c22c2-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accepte une variable qui indique l’option à définir, une mémoire tampon destinée à contenir la valeur de l’option et un pointeur qui contient l’adresse de la variable qui contient la longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c22c2-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accepts a variable that indicates the option to set, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

<span data-ttu-id="c22c2-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accepte une variable qui indique l’option à récupérer, une mémoire tampon destinée à contenir la valeur de l’option et un pointeur qui contient l’adresse de la variable qui contient la longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c22c2-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accepts a variable that indicates the option to retrieve, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

### <a name="setting-up-asynchronous-operations"></a><span data-ttu-id="c22c2-169">Configuration des opérations asynchrones</span><span class="sxs-lookup"><span data-stu-id="c22c2-169">Setting Up Asynchronous Operations</span></span>

<span data-ttu-id="c22c2-170">Par défaut, les fonctions WinINet fonctionnent de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="c22c2-170">By default, the WinINet functions operate synchronously.</span></span> <span data-ttu-id="c22c2-171">Une application peut demander une opération asynchrone en définissant l’indicateur [ \_ \_ Async Internet](api-flags.md) dans l’appel à la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-171">An application can request asynchronous operation by setting the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in the call to the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function.</span></span> <span data-ttu-id="c22c2-172">Tous les appels futurs effectués sur des handles dérivés du handle retourné par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) sont effectués de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c22c2-172">All future calls made against handles derived from the handle returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) are made asynchronously.</span></span>

<span data-ttu-id="c22c2-173">Le raisonnement pour les opérations asynchrones et synchrones consiste à permettre à une application monothread de maximiser son utilisation du processeur sans devoir attendre la fin de l’exécution des e/s réseau.</span><span class="sxs-lookup"><span data-stu-id="c22c2-173">The rationale for asynchronous versus synchronous operation is to allow a single-threaded application to maximize its utilization of the CPU without having to wait for network I/O to complete.</span></span> <span data-ttu-id="c22c2-174">Par conséquent, en fonction de la demande, l’opération peut s’effectuer de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c22c2-174">Therefore, depending on the request, the operation might complete synchronously or asynchronously.</span></span> <span data-ttu-id="c22c2-175">L’application doit vérifier le code de retour.</span><span class="sxs-lookup"><span data-stu-id="c22c2-175">The application should check the return code.</span></span> <span data-ttu-id="c22c2-176">Si une fonction retourne **false** ou **null**, et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne \_ des erreurs d’e/s \_ en attente, la demande a été effectuée de façon asynchrone et l’application est rappelée avec la \_ demande d’État Internet \_ \_ terminée lorsque la fonction est terminée.</span><span class="sxs-lookup"><span data-stu-id="c22c2-176">If a function returns **FALSE** or **NULL**, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_IO\_PENDING, the request has been made asynchronously, and the application is called back with INTERNET\_STATUS\_REQUEST\_COMPLETE when the function has completed.</span></span>

<span data-ttu-id="c22c2-177">Pour commencer l’opération asynchrone, l’application doit définir l’indicateur [ \_ \_ Async Internet Flag](api-flags.md) dans son appel à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="c22c2-177">To begin asynchronous operation, the application must set the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in its call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="c22c2-178">L’application doit ensuite inscrire une fonction de rappel valide à l’aide de [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="c22c2-178">The application must then register a valid callback function, using [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span></span>

<span data-ttu-id="c22c2-179">Une fois qu’une fonction de rappel est inscrite pour un handle, toutes les opérations sur ce handle peuvent générer des indications d’État, à condition que la valeur de contexte qui a été fournie lors de la création du handle ne soit pas égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="c22c2-179">After a callback function is registered for a handle, all operations on that handle can generate status indications, provided that the context value that was supplied when the handle was created was not zero.</span></span> <span data-ttu-id="c22c2-180">La spécification d’une valeur de contexte zéro force une opération à se terminer de façon synchrone, même si l' [ \_ indicateur Internet \_ Async](api-flags.md) a été spécifié dans [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="c22c2-180">Providing a zero context value forces an operation to complete synchronously, even though [INTERNET\_FLAG\_ASYNC](api-flags.md) was specified in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span>

<span data-ttu-id="c22c2-181">Les indications d’État fournissent à l’application des commentaires sur la progression des opérations réseau, telles que la résolution d’un nom d’hôte, la connexion à un serveur et la réception de données.</span><span class="sxs-lookup"><span data-stu-id="c22c2-181">Status indications give the application feedback about the progress of network operations, such as resolving a host name, connecting to a server, and receiving data.</span></span> <span data-ttu-id="c22c2-182">Trois indications d’État à usage spécial peuvent être effectuées pour un descripteur :</span><span class="sxs-lookup"><span data-stu-id="c22c2-182">Three special-purpose status indications can be made for a handle:</span></span>

-   <span data-ttu-id="c22c2-183">\_ \_ La fermeture du descripteur d’État Internet \_ est la dernière indication d’État effectuée pour un descripteur.</span><span class="sxs-lookup"><span data-stu-id="c22c2-183">INTERNET\_STATUS\_HANDLE\_CLOSING is the last status indication that is made for a handle.</span></span>
-   <span data-ttu-id="c22c2-184">\_ \_ Le descripteur d’État Internet \_ créé indique le moment où le descripteur est initialement créé.</span><span class="sxs-lookup"><span data-stu-id="c22c2-184">INTERNET\_STATUS\_HANDLE\_CREATED indicates when the handle is initially created.</span></span>
-   <span data-ttu-id="c22c2-185">La \_ \_ demande d’État Internet \_ est terminée indique qu’une opération asynchrone est terminée.</span><span class="sxs-lookup"><span data-stu-id="c22c2-185">INTERNET\_STATUS\_REQUEST\_COMPLETE indicates an asynchronous operation has completed.</span></span>

<span data-ttu-id="c22c2-186">L’application doit vérifier la structure des [**\_ \_ résultats Async Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) pour déterminer si l’opération a réussi ou échoué après avoir reçu une indication de la \_ demande d’État Internet \_ \_ terminée.</span><span class="sxs-lookup"><span data-stu-id="c22c2-186">The application must check the [**INTERNET\_ASYNC\_RESULT**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) structure to determine whether the operation succeeded or failed after receiving an INTERNET\_STATUS\_REQUEST\_COMPLETE indication.</span></span>

<span data-ttu-id="c22c2-187">L’exemple suivant montre un exemple de fonction de rappel et un appel à [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) pour inscrire la fonction en tant que fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="c22c2-187">The following sample shows an example of a callback function and a call to [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) to register the function as the callback function.</span></span>


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a><span data-ttu-id="c22c2-188">Fermeture des handles HINTERNET</span><span class="sxs-lookup"><span data-stu-id="c22c2-188">Closing HINTERNET Handles</span></span>

<span data-ttu-id="c22c2-189">Tous les descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) peuvent être fermés à l’aide de la fonction [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) .</span><span class="sxs-lookup"><span data-stu-id="c22c2-189">All [**HINTERNET**](appendix-a-hinternet-handles.md) handles can be closed by using the [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) function.</span></span> <span data-ttu-id="c22c2-190">Les applications clientes doivent fermer tous les descripteurs **HINTERNET** dérivés du descripteur **HINTERNET** qu’ils essaient de fermer avant d’appeler [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) sur le descripteur.</span><span class="sxs-lookup"><span data-stu-id="c22c2-190">Client applications must close all **HINTERNET** handles derived from the **HINTERNET** handle they are trying to close before calling [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle.</span></span>

<span data-ttu-id="c22c2-191">L’exemple suivant illustre la hiérarchie des handles.</span><span class="sxs-lookup"><span data-stu-id="c22c2-191">The following example illustrates the handle hierarchy.</span></span>


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a><span data-ttu-id="c22c2-192">Verrouillage et déverrouillage des ressources</span><span class="sxs-lookup"><span data-stu-id="c22c2-192">Locking and Unlocking Resources</span></span>

<span data-ttu-id="c22c2-193">La fonction [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) permet à une application de s’assurer que la ressource mise en cache associée au descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) qui lui est passée ne disparaît pas du cache.</span><span class="sxs-lookup"><span data-stu-id="c22c2-193">The [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function allows an application to ensure that the cached resource associated with the [**HINTERNET**](appendix-a-hinternet-handles.md) handle passed to it does not disappear from the cache.</span></span> <span data-ttu-id="c22c2-194">Si un autre téléchargement tente de valider une ressource qui a la même URL que le fichier verrouillé, le cache évite de supprimer le fichier en procédant à une suppression sécurisée.</span><span class="sxs-lookup"><span data-stu-id="c22c2-194">If another download tries to commit a resource that has the same URL as the locked file, the cache avoids removing the file by doing a safe delete.</span></span> <span data-ttu-id="c22c2-195">Une fois que l’application a appelé la fonction [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) , le cache reçoit l’autorisation de supprimer le fichier.</span><span class="sxs-lookup"><span data-stu-id="c22c2-195">After the application calls the [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) function, the cache is given permission to delete the file.</span></span>

<span data-ttu-id="c22c2-196">Si l' [indicateur \_ Internet \_ aucun \_ cache \_ Write](api-flags.md) ou indicateur de [ \_ \_ \_ cache](api-flags.md) de l’indicateur Internet n’a pas été défini, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) crée un fichier temporaire avec l’extension tmp, sauf si le descripteur est connecté à une ressource HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c22c2-196">If the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) or [INTERNET\_FLAG\_DONT\_CACHE](api-flags.md) flag has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) creates a temporary file with the extension TMP, unless the handle is connected to an https resource.</span></span> <span data-ttu-id="c22c2-197">Si la fonction accède à une ressource https et qu' \_ \_ aucune écriture dans le cache n’est définie pour l’indicateur Internet \_ (ou le cache de l' \_ \_ indicateur Internet \_ \_ ), [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) échoue.</span><span class="sxs-lookup"><span data-stu-id="c22c2-197">If the function accesses an https resource and INTERNET\_FLAG\_NO\_CACHE\_WRITE (or INTERNET\_FLAG\_DONT\_CACHE) has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) fails.</span></span>

> [!Note]  
> <span data-ttu-id="c22c2-198">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="c22c2-198">WinINet does not support server implementations.</span></span> <span data-ttu-id="c22c2-199">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="c22c2-199">In addition, it should not be used from a service.</span></span> <span data-ttu-id="c22c2-200">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="c22c2-200">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
