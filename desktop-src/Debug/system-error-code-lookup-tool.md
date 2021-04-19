---
description: Décrit comment utiliser l’outil de recherche d’erreurs Microsoft pour rechercher des explications de texte sur les codes d’erreur hexadécimaux dans Windows.
title: Outil de recherche d’erreurs Microsoft
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514331"
---
# <a name="the-microsoft-error-lookup-tool"></a><span data-ttu-id="31f11-103">Outil de recherche d’erreurs Microsoft</span><span class="sxs-lookup"><span data-stu-id="31f11-103">The Microsoft Error Lookup Tool</span></span>

<span data-ttu-id="31f11-104">L’outil de recherche d’erreurs Microsoft affiche le texte du message associé à un code d’État hexadécimal (ou autre code).</span><span class="sxs-lookup"><span data-stu-id="31f11-104">The Microsoft Error Lookup Tool displays the message text that is associated with a hexadecimal status code (or other code).</span></span> <span data-ttu-id="31f11-105">Ce texte est défini dans différents fichiers d’en-tête de code source Microsoft, tels que winerror. h, Setupapi. h, etc.</span><span class="sxs-lookup"><span data-stu-id="31f11-105">This text is defined in various Microsoft source-code header files, such as Winerror.h, Setupapi.h, and so on.</span></span>

<span data-ttu-id="31f11-106">L’outil est signé numériquement par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="31f11-106">The tool is digitally signed by Microsoft.</span></span> <span data-ttu-id="31f11-107">Voici les informations SHA256 pour le téléchargement de fichiers :</span><span class="sxs-lookup"><span data-stu-id="31f11-107">The following is the SHA256 information for the file download:</span></span>  

|<span data-ttu-id="31f11-108">Algorithm</span><span class="sxs-lookup"><span data-stu-id="31f11-108">Algorithm</span></span> |<span data-ttu-id="31f11-109">Hachage</span><span class="sxs-lookup"><span data-stu-id="31f11-109">Hash</span></span> |
| --- | --- |
|<span data-ttu-id="31f11-110">SHA256</span><span class="sxs-lookup"><span data-stu-id="31f11-110">SHA256</span></span> |<span data-ttu-id="31f11-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span><span class="sxs-lookup"><span data-stu-id="31f11-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span></span> |

> [!NOTE]
> <span data-ttu-id="31f11-112">Les environnements d’entreprise peuvent limiter les fichiers qui peuvent être exécutés et à partir de où.</span><span class="sxs-lookup"><span data-stu-id="31f11-112">Business environments may restrict which files can run and from where.</span></span> <span data-ttu-id="31f11-113">Avant de télécharger et d’exécuter cet outil, vérifiez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="31f11-113">Before you download and run this tool, check the following details:</span></span>
> - <span data-ttu-id="31f11-114">Avez-vous besoin d’une autorisation ou d’une exception de sécurité pour pouvoir télécharger ou exécuter l’outil ?</span><span class="sxs-lookup"><span data-stu-id="31f11-114">Do you have to have permission or a security exception in order to download or run the tool?</span></span>
> - <span data-ttu-id="31f11-115">Pouvez-vous stocker et exécuter cet outil sur votre ordinateur (par exemple, dans votre dossier de documents) ?</span><span class="sxs-lookup"><span data-stu-id="31f11-115">Can you store and run this tool on your computer (for example, in your Documents folder)?</span></span> <span data-ttu-id="31f11-116">Ou avez-vous besoin de stocker et d’exécuter l’outil sur un ordinateur spécialisé, tel qu’un serveur de fichiers central ?</span><span class="sxs-lookup"><span data-stu-id="31f11-116">Or do you have to store and run the tool on a specialized computer, such as a central file server?</span></span>

## <a name="usage"></a><span data-ttu-id="31f11-117">Utilisation</span><span class="sxs-lookup"><span data-stu-id="31f11-117">Usage</span></span>

1. <span data-ttu-id="31f11-118">Téléchargez l’outil en sélectionnant [ce lien](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span><span class="sxs-lookup"><span data-stu-id="31f11-118">Download the tool by selecting [this link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span></span>
1. <span data-ttu-id="31f11-119">Si vous n’avez pas spécifié d’emplacement à l’étape 1, accédez à votre dossier de téléchargement, puis copiez ou déplacez le fichier téléchargé (Err_6.4.5.exe) dans le dossier dans lequel vous allez stocker l’outil.</span><span class="sxs-lookup"><span data-stu-id="31f11-119">If you didn't specify a location in step 1, go to your download folder, and copy or move the downloaded file (Err_6.4.5.exe) to folder in which you will store the tool.</span></span> <span data-ttu-id="31f11-120">Vous n’avez pas besoin de développer ou d’installer le fichier.</span><span class="sxs-lookup"><span data-stu-id="31f11-120">You do not have to expand or install the file.</span></span>
   > [!NOTE]
   > <span data-ttu-id="31f11-121">Si vous copiez ou déplacez le fichier vers un dossier qui est listé dans la variable **d’environnement PATH** de votre système d’exploitation, il fonctionnera à n’importe quelle invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="31f11-121">If you copy or move the file to a folder that is listed in your operating system's **Path** environment variable, it will work at any command prompt.</span></span>

1. <span data-ttu-id="31f11-122">Ouvrez une fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="31f11-122">Open a Command Prompt window.</span></span> <span data-ttu-id="31f11-123">Si nécessaire, remplacez le répertoire par l’emplacement de l’outil de recherche d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="31f11-123">If necessary, change the directory to the location of the Error Lookup Tool.</span></span>
1. <span data-ttu-id="31f11-124">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="31f11-124">Run the following command:</span></span>
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > <span data-ttu-id="31f11-125">Dans cette commande, \<*error code*> représente le code hexadécimal que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="31f11-125">In this command, \<*error code*> represents the hexadecimal code that you want to look up.</span></span>

## <a name="examples"></a><span data-ttu-id="31f11-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="31f11-126">Examples</span></span>

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a><span data-ttu-id="31f11-127">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="31f11-127">More information</span></span>

<span data-ttu-id="31f11-128">Gardez à l’esprit qu’il s’agit d’un outil « à un point dans le temps ».</span><span class="sxs-lookup"><span data-stu-id="31f11-128">Keep in mind that this is a "point-in-time" tool.</span></span> <span data-ttu-id="31f11-129">L’outil de recherche d’erreurs Microsoft décode la plupart des codes d’erreur Microsoft à la date de compilation de l’outil.</span><span class="sxs-lookup"><span data-stu-id="31f11-129">The Microsoft Error Lookup Tool decodes most Microsoft error codes as of the date on which the tool was compiled.</span></span> <span data-ttu-id="31f11-130">À mesure que de nouvelles versions de Windows ajoutent de nouveaux codes d’événement et d’erreur, vous devrez peut-être télécharger une nouvelle version de l’outil de recherche d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="31f11-130">As new releases of Windows add new event and error codes, you may have to download a new version of the Error Lookup Tool.</span></span> <span data-ttu-id="31f11-131">Consultez le centre de téléchargement Microsoft pour obtenir une nouvelle version ou consultez [codes d’erreur](system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="31f11-131">Check the Microsoft Download Center for a new version, or see [Error Codes](system-error-codes.md).</span></span>
