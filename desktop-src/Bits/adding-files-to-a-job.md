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
# <a name="adding-files-to-a-job"></a>Ajout de fichiers à un travail

Un travail contient un ou plusieurs fichiers que vous souhaitez transférer. Utilisez l’une des méthodes suivantes pour ajouter des fichiers à un travail :

<dl> <dt>

<span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**Méthode ibackgroundcopyjob :: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
</dt> <dd>

Ajoute un seul fichier à un travail.

</dd> <dt>

<span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**Méthode ibackgroundcopyjob :: AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
</dt> <dd>

Ajoute un ou plusieurs fichiers à un travail. Si vous ajoutez plusieurs fichiers, il est plus efficace d’appeler cette méthode que d’appeler la méthode **AddFile** dans une boucle.

</dd> <dt>

<span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)
</dt> <dd>

Ajoute un seul fichier à un travail. Utilisez cette méthode si vous souhaitez télécharger des plages de données à partir d’un fichier. Vous pouvez utiliser cette méthode uniquement pour les travaux de téléchargement.

</dd> </dl>

Lorsque vous ajoutez un fichier à un travail, vous spécifiez le nom distant et le nom local du fichier. Pour plus d’informations sur le format des noms de fichiers locaux et distants, consultez la structure d' [**\_ \_ informations de fichier BG**](/windows/desktop/api/Bits/ns-bits-bg_file_info) .

Un travail de chargement ne peut contenir qu’un seul fichier. Les méthodes [**méthode ibackgroundcopyjob :: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) et [**méthode ibackgroundcopyjob :: AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) retournent le \_ \_ nombre de fichiers BG E trop de \_ \_ fichiers si vous essayez d’ajouter plusieurs fichiers à un travail de chargement. Si vous devez télécharger plusieurs fichiers, envisagez d’utiliser un fichier CAB ou ZIP.

Pour les travaux de téléchargement, BITS limite le nombre de fichiers qu’un utilisateur peut ajouter à un travail sur 200 fichiers et le nombre de plages d’un fichier à 500 plages. Ces limites ne s’appliquent pas aux administrateurs ou aux services. Pour modifier ces limites par défaut, consultez [stratégies de groupe](group-policies.md).

Le propriétaire du travail ou un utilisateur disposant de privilèges d’administrateur peut ajouter des fichiers au travail à tout moment avant d’appeler la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou la méthode [**méthode ibackgroundcopyjob :: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .

Si vous avez besoin de modifier le nom distant du fichier une fois que vous avez ajouté le fichier au travail, vous pouvez appeler la méthode [**IBackgroundCopyJob3 :: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) ou la méthode [**IBackgroundCopyFile2 :: SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) . Utilisez la méthode **ReplaceRemotePrefix** pour modifier la partie serveur du nom distant lorsque le serveur n’est pas disponible ou pour permettre aux utilisateurs itinérants de se connecter au serveur le plus proche. Utilisez la méthode **SetRemoteName** pour modifier le protocole utilisé pour transférer le fichier ou pour modifier le nom ou le chemin d’accès du fichier.

Le service BITS crée un fichier temporaire dans le répertoire de destination et utilise le fichier temporaire pour le transfert de fichiers. Pour récupérer le nom de fichier temporaire, appelez la méthode [**IBackgroundCopyFile3 :: GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) . Le service BITS remplace le nom de fichier temporaire par le nom de fichier de destination lorsque vous appelez la méthode [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Le service BITS ne spécifie pas de descripteur de sécurité lors de la [**création**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) du fichier temporaire (le fichier hérite des informations de la liste de contrôle d’accès du répertoire de destination). Si les données transférées sont sensibles, l’application doit spécifier une liste de contrôle d’accès (ACL) appropriée dans le répertoire de destination pour empêcher tout accès non autorisé.

Pour conserver les informations relatives au propriétaire et à la liste de contrôle d’accès avec le fichier transféré, appelez la méthode [**IBackgroundCopyJob3 :: SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) .

Le propriétaire du travail (l’utilisateur qui a créé le travail ou l’administrateur qui [a pris possession](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) du travail) doit disposer d’autorisations sur le fichier sur le serveur, ainsi que sur le client. Par exemple, pour télécharger un fichier, l’utilisateur doit disposer d’autorisations de lecture sur le serveur et d’autorisations d’écriture sur le répertoire local sur le client.

L’exemple suivant montre comment ajouter un seul fichier au travail. L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, est valide.


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



L’exemple suivant montre comment ajouter plusieurs fichiers au travail. L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, est valide et que les noms locaux et distants proviennent d’une liste dans l’interface utilisateur.


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



 

 