---
title: Contrôler un téléchargement BITS sur une connexion coûteuse
description: Bloquez le téléchargement sur une connexion coûteuse telle qu’un lien mobile itinérant.
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- Téléchargement de BITS, procédure
- Téléchargements de BITS, évitant les coûts
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7cb09dbd277d9ec74ce4988db210bf80c22d97ccaa3054a170fc1c9913282cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959488"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a>Contrôler un téléchargement BITS sur une connexion coûteuse

Cette rubrique montre comment bloquer le téléchargement d’une tâche BITS sur une connexion coûteuse, telle qu’un lien mobile itinérant. Le service BITS est une API asynchrone dans laquelle l’application crée un travail, ajoute des URL à ce travail et appelle la fonction de [**reprise**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) de l’objet de tâche. À partir de ce point, le service BITS choisit le moment où le travail est téléchargé en fonction de facteurs tels que la priorité du travail et la stratégie de transfert. Une fois le travail terminé, le service BITS avertit l’application que l’URL a été téléchargée (si l’application s’est inscrite pour la notification d’achèvement). Pendant la durée de vie de la tâche, si le réseau de l’utilisateur final change (par exemple, si l’utilisateur est en déplacement et qu’il s’agit actuellement de frais d’itinérance), le service BITS interrompt le travail jusqu’à ce que les conditions du réseau soient optimales. Les instructions pas à pas suivantes montrent comment créer le travail et spécifier les paramètres de stratégie de transfert appropriés.

### <a name="prerequisites"></a>Prérequis

-   Microsoft Visual Studio

## <a name="instructions"></a>Instructions

### <a name="step-1-include-the-required-bits-header-files"></a>Étape 1 : inclure les fichiers d’en-tête BITS requis

Insérez les directives d’en-tête suivantes en haut du fichier source.


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a>Étape 2 : initialiser COM

Avant d’instancier l’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) (utilisée pour créer un travail bits), vous devez initialiser com, définir le modèle de thread com et spécifier un niveau d’emprunt d’identité au moins au \_ niveau RPC C \_ IMP \_ \_ Impersonate.


```C++
// Initialize COM and specify the COM threading model.
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
 // Specify an impersonation level of at least RPC_C_IMP_LEVEL_IMPERSONATE.
 hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                           RPC_C_AUTHN_LEVEL_CONNECT,
                           RPC_C_IMP_LEVEL_IMPERSONATE,
                           NULL, EOAC_NONE, 0);
 if (SUCCEEDED(hr))
 {
  ...
```



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a>Étape 3 : instanciation de l’interface IBackgroundCopyManager

Utilisez l’interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) pour créer des tâches de transfert, récupérer un objet énumérateur qui contient les travaux dans la file d’attente et récupérer des tâches individuelles de la file d’attente.


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a>Étape 4 : créer le travail BITS

Seul l’utilisateur qui crée le travail ou un utilisateur disposant de privilèges d’administrateur peut ajouter des fichiers au travail et modifier les propriétés du travail.


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a>Étape 5 : spécifier le paramètre de stratégie de transfert pour le travail

C’est ici que vous spécifiez la stratégie de transfert d’État du coût. Vous pouvez définir plusieurs \_ \_ indicateurs d’État du coût de bits à  l’aide d’une combinaison d’opérations de bits or pour obtenir les résultats souhaités.


```C++
BITS_JOB_PROPERTY_VALUE propval;
IBackgroundCopyJob5* pBackgroundCopyJob5;

propval.Dword = BITS_COST_STATE_USAGE_BASED
              | BITS_COST_STATE_OVERCAP_THROTTLED
              | BITS_COST_STATE_BELOW_CAP
              | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
              | BITS_COST_STATE_UNRESTRICTED;

hr = pBackgroundCopyJob->QueryInterface(__uuidof(IBackgroundCopyJob5),
                                        reinterpret_cast<void**>(&pBackgroundCopyJob5));
if(SUCCEEDED(hr))
{
 pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);
}
```



## <a name="example"></a> Exemple

L’exemple de code suivant montre comment définir la stratégie de transfert d’un travail BITS afin que le traitement du travail ne se produise pas lorsque certaines conditions sont remplies, par exemple lorsque l’utilisateur est en itinérance ou a dépassé sa limite de transfert de données mensuelle.


```C++
//*********************************************************
//
//    Copyright (c) Microsoft. All rights reserved.
//    This code is licensed under the Microsoft Public License.
//    THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF
//    ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY
//    IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR
//    PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.
//
//*********************************************************

#define WIN32_LEAN_AND_MEAN             // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <stdio.h> // define wprintf


int main()
{
 HRESULT hr = S_OK;
 GUID guidJob;
 IBackgroundCopyJob5* pBackgroundCopyJob5;  
 IBackgroundCopyJob* pBackgroundCopyJob;
 IBackgroundCopyManager* pQueueMgr;
 BITS_JOB_PROPERTY_VALUE propval;

 // Specify the COM threading model.
 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 if (SUCCEEDED(hr))
 {
  // The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
  hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                            RPC_C_AUTHN_LEVEL_CONNECT,
                            RPC_C_IMP_LEVEL_IMPERSONATE,
                            NULL, EOAC_NONE, 0);

  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(__uuidof(BackgroundCopyManager), 
                         NULL,
                         CLSCTX_LOCAL_SERVER,
                         __uuidof(IBackgroundCopyManager),
                         (void **)&pQueueMgr);

   if (FAILED(hr))
   {
    // Failed to connect to BITS.
    wprintf(L"Failed to connect to BITS with error %x\n",hr);
    goto done;
   }

   // Create a BITS job.
   wprintf(L"Creating Job...\n");

   hr = pQueueMgr->CreateJob(L"TransferPolicy",
                             BG_JOB_TYPE_DOWNLOAD,
                             &guidJob,
                             (IBackgroundCopyJob **)&pBackgroundCopyJob);

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }

   wprintf(L" Job is succesfully created ...\n");

   // Set the Transfer Policy for the job.
   propval.Dword = BITS_COST_STATE_USAGE_BASED 
                 | BITS_COST_STATE_OVERCAP_THROTTLED
                 | BITS_COST_STATE_BELOW_CAP
                 | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
                 | BITS_COST_STATE_UNRESTRICTED;

   hr = pBackgroundCopyJob->QueryInterface(
         __uuidof(IBackgroundCopyJob5),
         reinterpret_cast<void**>(&pBackgroundCopyJob5)
        );

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }
   pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);

   // Get the Transfer Policy for the new job.
   BITS_JOB_PROPERTY_VALUE actual_propval;

   wprintf(L"Getting TransferPolicy Property ...\n");

   hr = pBackgroundCopyJob5->GetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, 
                                         &actual_propval);
   if (FAILED(hr))
   {
    // SetSSLSecurityFlags failed.
    wprintf(L"GetProperty failed with error %x\n",hr);
    goto cancel;
   }

   DWORD job_transferpolicy = actual_propval.Dword;
   wprintf(L"get TransferPolicy Property returned %#x\n", job_transferpolicy);
  }
done:
  CoUninitialize();
 }
 return 1;

cancel:
 pBackgroundCopyJob->Cancel(); 
 pBackgroundCopyJob->Release();
 goto done;
}
```



 

 




