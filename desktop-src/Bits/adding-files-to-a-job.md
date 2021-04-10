---
title: Ajout de fichiers à un travail
description: Un travail contient un ou plusieurs fichiers que vous souhaitez transférer.
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- transférer les BITS du travail, ajouter des fichiers
- BITS de transfert de fichiers, ajout
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: ecb46a535fee117750b8b46066d798a4525aa44c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941134"
---
# <a name="adding-files-to-a-job"></a><span data-ttu-id="49e7d-105">Ajout de fichiers à un travail</span><span class="sxs-lookup"><span data-stu-id="49e7d-105">Adding Files to a Job</span></span>

<span data-ttu-id="49e7d-106">Un travail contient un ou plusieurs fichiers que vous souhaitez transférer.</span><span class="sxs-lookup"><span data-stu-id="49e7d-106">A job contains one or more files that you want to transfer.</span></span> <span data-ttu-id="49e7d-107">Utilisez l’une des méthodes suivantes pour ajouter des fichiers à un travail :</span><span class="sxs-lookup"><span data-stu-id="49e7d-107">Use one of the following methods to add files to a job:</span></span>

<dl> <dt>

<span data-ttu-id="49e7d-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**Méthode ibackgroundcopyjob :: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span><span class="sxs-lookup"><span data-stu-id="49e7d-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span></span>
</dt> <dd>

<span data-ttu-id="49e7d-109">Ajoute un seul fichier à un travail.</span><span class="sxs-lookup"><span data-stu-id="49e7d-109">Adds a single file to a job.</span></span>

</dd> <dt>

<span data-ttu-id="49e7d-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**Méthode ibackgroundcopyjob :: AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span><span class="sxs-lookup"><span data-stu-id="49e7d-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span></span>
</dt> <dd>

<span data-ttu-id="49e7d-111">Ajoute un ou plusieurs fichiers à un travail.</span><span class="sxs-lookup"><span data-stu-id="49e7d-111">Adds one or more files to a job.</span></span> <span data-ttu-id="49e7d-112">Si vous ajoutez plusieurs fichiers, il est plus efficace d’appeler cette méthode que d’appeler la méthode **AddFile** dans une boucle.</span><span class="sxs-lookup"><span data-stu-id="49e7d-112">If you are adding multiple files, it is more efficient to call this method than to call the **AddFile** method in a loop.</span></span>

</dd> <dt>

<span data-ttu-id="49e7d-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span><span class="sxs-lookup"><span data-stu-id="49e7d-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span></span>
</dt> <dd>

<span data-ttu-id="49e7d-114">Ajoute un seul fichier à un travail.</span><span class="sxs-lookup"><span data-stu-id="49e7d-114">Adds a single file to a job.</span></span> <span data-ttu-id="49e7d-115">Utilisez cette méthode si vous souhaitez télécharger des plages de données à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="49e7d-115">Use this method if you want to download ranges of data from a file.</span></span> <span data-ttu-id="49e7d-116">Vous pouvez utiliser cette méthode uniquement pour les travaux de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="49e7d-116">You can use this method only for download jobs.</span></span>

</dd> </dl>

<span data-ttu-id="49e7d-117">Lorsque vous ajoutez un fichier à un travail, vous spécifiez le nom distant et le nom local du fichier.</span><span class="sxs-lookup"><span data-stu-id="49e7d-117">When you add a file to a job, you specify the remote name and the local name of the file.</span></span> <span data-ttu-id="49e7d-118">Pour plus d’informations sur le format des noms de fichiers locaux et distants, consultez la structure d' [**\_ \_ informations de fichier BG**](/windows/desktop/api/Bits/ns-bits-bg_file_info) .</span><span class="sxs-lookup"><span data-stu-id="49e7d-118">For details on the format of the local and remote file names, see the [**BG\_FILE\_INFO**](/windows/desktop/api/Bits/ns-bits-bg_file_info) structure.</span></span>

<span data-ttu-id="49e7d-119">Un travail de chargement ne peut contenir qu’un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="49e7d-119">An upload job can contain only one file.</span></span> <span data-ttu-id="49e7d-120">Les méthodes [**méthode ibackgroundcopyjob :: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) et [**méthode ibackgroundcopyjob :: AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) retournent le \_ \_ nombre de fichiers BG E trop de \_ \_ fichiers si vous essayez d’ajouter plusieurs fichiers à un travail de chargement.</span><span class="sxs-lookup"><span data-stu-id="49e7d-120">The [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) and [**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) methods return BG\_E\_TOO\_MANY\_FILES if you try to add more than one file to an upload job.</span></span> <span data-ttu-id="49e7d-121">Si vous devez télécharger plusieurs fichiers, envisagez d’utiliser un fichier CAB ou ZIP.</span><span class="sxs-lookup"><span data-stu-id="49e7d-121">If you need to upload more than one file, consider using a CAB or ZIP file.</span></span>

<span data-ttu-id="49e7d-122">Pour les travaux de téléchargement, BITS limite le nombre de fichiers qu’un utilisateur peut ajouter à un travail sur 200 fichiers et le nombre de plages d’un fichier à 500 plages.</span><span class="sxs-lookup"><span data-stu-id="49e7d-122">For download jobs, BITS limits the number of files that a user can add to a job to 200 files and the number of ranges for a file to 500 ranges.</span></span> <span data-ttu-id="49e7d-123">Ces limites ne s’appliquent pas aux administrateurs ou aux services.</span><span class="sxs-lookup"><span data-stu-id="49e7d-123">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="49e7d-124">Pour modifier ces limites par défaut, consultez [stratégies de groupe](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="49e7d-124">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="49e7d-125">Le propriétaire du travail ou un utilisateur disposant de privilèges d’administrateur peut ajouter des fichiers au travail à tout moment avant d’appeler la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou la méthode [**méthode ibackgroundcopyjob :: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="49e7d-125">The owner of the job or a user with administrator privileges can add files to the job anytime prior to calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>

<span data-ttu-id="49e7d-126">Si vous avez besoin de modifier le nom distant du fichier une fois que vous avez ajouté le fichier au travail, vous pouvez appeler la méthode [**IBackgroundCopyJob3 :: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) ou la méthode [**IBackgroundCopyFile2 :: SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) .</span><span class="sxs-lookup"><span data-stu-id="49e7d-126">If you need to change the remote name of the file after you add the file to the job, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) method or the [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method.</span></span> <span data-ttu-id="49e7d-127">Utilisez la méthode **ReplaceRemotePrefix** pour modifier la partie serveur du nom distant lorsque le serveur n’est pas disponible ou pour permettre aux utilisateurs itinérants de se connecter au serveur le plus proche.</span><span class="sxs-lookup"><span data-stu-id="49e7d-127">Use the **ReplaceRemotePrefix** method to change the server portion of the remote name when the server is unavailable or to let roaming users connect to the closest server.</span></span> <span data-ttu-id="49e7d-128">Utilisez la méthode **SetRemoteName** pour modifier le protocole utilisé pour transférer le fichier ou pour modifier le nom ou le chemin d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="49e7d-128">Use the **SetRemoteName** method to change the protocol used to transfer the file or to change the file name or path.</span></span>

<span data-ttu-id="49e7d-129">Le service BITS crée un fichier temporaire dans le répertoire de destination et utilise le fichier temporaire pour le transfert de fichiers.</span><span class="sxs-lookup"><span data-stu-id="49e7d-129">BITS creates a temporary file in the destination directory and uses the temporary file for the file transfer.</span></span> <span data-ttu-id="49e7d-130">Pour récupérer le nom de fichier temporaire, appelez la méthode [**IBackgroundCopyFile3 :: GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) .</span><span class="sxs-lookup"><span data-stu-id="49e7d-130">To get the temporary file name, call the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method.</span></span> <span data-ttu-id="49e7d-131">Le service BITS remplace le nom de fichier temporaire par le nom de fichier de destination lorsque vous appelez la méthode [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="49e7d-131">BITS changes the temporary file name to the destination file name when you call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="49e7d-132">Le service BITS ne spécifie pas de descripteur de sécurité lors de la [**création**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) du fichier temporaire (le fichier hérite des informations de la liste de contrôle d’accès du répertoire de destination).</span><span class="sxs-lookup"><span data-stu-id="49e7d-132">BITS does not specify a security descriptor when it [**creates**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) the temporary file (the file inherits the ACL information from the destination directory).</span></span> <span data-ttu-id="49e7d-133">Si les données transférées sont sensibles, l’application doit spécifier une liste de contrôle d’accès (ACL) appropriée dans le répertoire de destination pour empêcher tout accès non autorisé.</span><span class="sxs-lookup"><span data-stu-id="49e7d-133">If the transferred data is sensitive, the application should specify an appropriate ACL on the destination directory to prevent unauthorized access.</span></span>

<span data-ttu-id="49e7d-134">Pour conserver les informations relatives au propriétaire et à la liste de contrôle d’accès avec le fichier transféré, appelez la méthode [**IBackgroundCopyJob3 :: SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) .</span><span class="sxs-lookup"><span data-stu-id="49e7d-134">To maintain the owner and ACL information with the transferred file, call the [**IBackgroundCopyJob3::SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) method.</span></span>

<span data-ttu-id="49e7d-135">Le propriétaire du travail (l’utilisateur qui a créé le travail ou l’administrateur qui [a pris possession](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) du travail) doit disposer d’autorisations sur le fichier sur le serveur, ainsi que sur le client.</span><span class="sxs-lookup"><span data-stu-id="49e7d-135">The owner of the job (the user who created the job or the administrator who [took ownership](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) of the job) must have permissions to the file on the server as well as the client.</span></span> <span data-ttu-id="49e7d-136">Par exemple, pour télécharger un fichier, l’utilisateur doit disposer d’autorisations de lecture sur le serveur et d’autorisations d’écriture sur le répertoire local sur le client.</span><span class="sxs-lookup"><span data-stu-id="49e7d-136">For example, to download a file the user must have read permissions on the server and write permissions to the local directory on the client.</span></span>

<span data-ttu-id="49e7d-137">L’exemple suivant montre comment ajouter un seul fichier au travail.</span><span class="sxs-lookup"><span data-stu-id="49e7d-137">The following example shows how to add a single file to the job.</span></span> <span data-ttu-id="49e7d-138">L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, est valide.</span><span class="sxs-lookup"><span data-stu-id="49e7d-138">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;

//Replace parameters with variables that contain valid paths.
hr = pJob->AddFile(L"https://ServerName/Path/File.Ext", L"d:\\Path\\File.Ext");
if (SUCCEEDED(hr))
{
  //Do something.
}
```



<span data-ttu-id="49e7d-139">L’exemple suivant montre comment ajouter plusieurs fichiers au travail.</span><span class="sxs-lookup"><span data-stu-id="49e7d-139">The following example shows how to add multiple files to the job.</span></span> <span data-ttu-id="49e7d-140">L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, est valide et que les noms locaux et distants proviennent d’une liste dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49e7d-140">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid and the local and remote names come from a list in the user interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_FILE_INFO* paFiles = NULL;
ULONG idx = 0;
ULONG nCount = 0;            //Set to the number of files to add to the job.
LPWSTR pszLocalName = NULL;  //Comes from the list in the user interface.
LPWSTR pszRemoteName = NULL; //Comes from the list in the user interface.

//Set nCount to the number of files to transfer.

//Allocate a block of memory to contain the array of BG_FILE_INFO structures.
//The BG_FILE_INFO structure contains the local and remote names of the 
//file being transferred.
paFiles = (BG_FILE_INFO*) malloc(sizeof(BG_FILE_INFO) * nCount);
if (NULL == paFiles)
{
  //Handle error
}
else
{
  //Add local and remote file name pairs to the memory block. 
  for (idx=0; idx<nCount; idx++)
  {
    //Set pszLocalName to point to an LPWSTR that contains the local name or
    //allocate memory for pszLocalName and copy the local name to pszLocalName.
    (paFiles+idx)->LocalName = pszLocalName;

    //Set pszRemoteName to point to an LPWSTR that contains the remote name or
    //allocate memory for pszRemoteName and copy the remote name to pszRemoteName.
    (paFiles+idx)->RemoteName = pszRemoteName;
  }

  //Add the files to the job.
  hr = pJob->AddFileSet(nCount, paFiles);
  if (SUCCEEDED(hr))
  {
     //Do Something.
  }

  //Free the memory block for the array of BG_FILE_INFO structures. If you allocated
  //memory for the local and remote file names, loop through the array and free the
  //memory for the file names before you free paFiles.
  free(paFiles);
}
```



 

 