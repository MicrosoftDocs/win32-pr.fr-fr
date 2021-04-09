---
title: Gestion des erreurs (BITS)
description: Il existe deux types d’erreurs à gérer dans votre application.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- gestion des BITS d’erreur
- BITS de tâche de transfert, Erreurs
- BITS d’erreur
- BITS d’erreur, gestion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1544788192d4bfd778fef83caaca922f1f84c01e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032175"
---
# <a name="handling-errors-bits"></a>Gestion des erreurs (BITS)

Il existe deux types d’erreurs à gérer dans votre application. La première erreur est un appel de méthode qui a échoué. Chaque méthode retourne une valeur **HRESULT** . La page de référence de chaque méthode identifie les valeurs de retour qu’il est le plus susceptible de générer. Pour obtenir des valeurs de retour supplémentaires, consultez [bits Return values](bits-return-values.md). Pour obtenir le texte du message associé à la valeur de retour, appelez la méthode [**IBackgroundCopyManager :: GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) .

Le deuxième type d’erreur à gérer est un travail dont l' [État](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) passe à [ \_ \_ \_ erreur d’état de la tâche BG](/windows/desktop/api/Bits/ne-bits-bg_job_state) ou à une **\_ \_ \_ \_ erreur temporaire d’état de travail BG**. Pour récupérer les informations relatives à ces types d’erreurs, appelez la méthode [**méthode ibackgroundcopyjob :: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) du travail. La méthode retourne un pointeur d’interface [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) qui contient les informations que vous utilisez pour déterminer la cause de l’erreur. Vous pouvez également recevoir une notification d’erreur en vous inscrivant pour recevoir une notification d’événement. Pour plus d’informations, consultez [inscription d’un rappel com](registering-a-com-callback.md).

BITS considère chaque travail comme atomique. Si l’un des fichiers du travail génère une erreur, le travail reste dans un état d’erreur jusqu’à ce que l’erreur soit résolue. Par conséquent, vous ne pouvez pas supprimer le fichier à l’origine de l’erreur du travail. Toutefois, si l’erreur est due au fait que le serveur n’est pas disponible ou qu’il s’agit d’un fichier distant non valide, vous pouvez appeler la méthode [**IBackgroundCopyJob3 :: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) ou [**IBackgroundCopyFile2 :: SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) pour identifier un nouveau serveur ou nom de fichier.

Après avoir déterminé la cause de l’erreur, effectuez l’une des options suivantes :

-   Annulez la tâche en appelant la méthode [**méthode ibackgroundcopyjob :: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .
-   Pour un travail de téléchargement, appelez la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) pour enregistrer les fichiers qui ont été transférés correctement avant l’erreur.
-   Corrigez l’erreur et appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) pour terminer le travail.

Pour une tâche de chargement-réponse, vérifiez la valeur du membre **bytesTotal** de la structure de progression de la réponse de la [**\_ tâche \_ \_ BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) pour déterminer si l’erreur s’est produite lors du chargement ou de la réponse de la tâche. L’erreur s’est produite lors du téléchargement si la valeur de la taille BG est \_ \_ inattendue.

L’exemple suivant montre comment récupérer un pointeur d’interface [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) . L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide.


```C++
HRESULT hr = 0;
HRESULT hrError = 0;
IBackgroundCopyJob* pJob;
IBackgroundCopyError* pError = NULL;
IBackgroundCopyFile* pFile = NULL;
WCHAR* pszDescription = NULL;
WCHAR* pszRemoteName = NULL;
BG_ERROR_CONTEXT Context;

hr = pJob->GetError(&pError);
if (SUCCEEDED(hr))
{
  //Retrieve the HRESULT associated with the error. The context tells you
  //where the error occurred, for example, in the transport, queue manager, the 
  //local file, or the remote file.
  pError->GetError(&Context, &hrError);  

  //Retrieve a description associated with the HRESULT value.
  hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    if (BG_ERROR_CONTEXT_REMOTE_FILE == Context)
    {
      hr = pError->GetFile(&pFile);  
      if (SUCCEEDED(hr))
      {
        hr = pFile->GetRemoteName(&pszRemoteName);
        if (SUCCEEDED(hr))
        {
          //Do something with the information.
          CoTaskMemFree(pszRemoteName);
        }
        pFile->Release();
      }
    }
    CoTaskMemFree(pszDescription);
  }
  pError->Release();
}
else
{
  //Error information is not available.
}
```



 

 




