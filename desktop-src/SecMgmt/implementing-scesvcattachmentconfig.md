---
description: Doit extraire les informations de la base de données de sécurité, puis utiliser ces informations pour configurer le service.
ms.assetid: c0c1c1e4-de5b-405d-abe8-33a985ce98e5
title: Implémentation de SceSvcAttachmentConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98eb519e6422e3036ddfb203811322befd2713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952503"
---
# <a name="implementing-scesvcattachmentconfig"></a><span data-ttu-id="9666c-103">Implémentation de SceSvcAttachmentConfig</span><span class="sxs-lookup"><span data-stu-id="9666c-103">Implementing SceSvcAttachmentConfig</span></span>

<span data-ttu-id="9666c-104">La fonction [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) doit extraire des informations de la base de données de sécurité, puis utiliser ces informations pour configurer le service.</span><span class="sxs-lookup"><span data-stu-id="9666c-104">The [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) function must retrieve information from the security database and then use that information to configure the service.</span></span>

<span data-ttu-id="9666c-105">Lors de l’implémentation de [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), vous pouvez récupérer toutes les informations, puis configurer le service, ou récupérer et configurer le service en étapes.</span><span class="sxs-lookup"><span data-stu-id="9666c-105">When implementing [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), you can either retrieve all of the information and then configure the service, or retrieve and configure the service in steps.</span></span> <span data-ttu-id="9666c-106">L’algorithme suivant récupère toutes les informations, puis configure le service.</span><span class="sxs-lookup"><span data-stu-id="9666c-106">The following algorithm retrieves all of the information and then configures the service.</span></span>

<span data-ttu-id="9666c-107">**Pour implémenter SceSvcAttachmentConfig**</span><span class="sxs-lookup"><span data-stu-id="9666c-107">**To implement SceSvcAttachmentConfig**</span></span>

1.  <span data-ttu-id="9666c-108">Définissez les variables nécessaires pour récupérer les informations et les codes de retour.</span><span class="sxs-lookup"><span data-stu-id="9666c-108">Define the variables needed to retrieve information and return codes.</span></span>
2.  <span data-ttu-id="9666c-109">Appelez la fonction de rappel pfQueryInfo dans la structure de rappel pour récupérer les informations de configuration de la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9666c-109">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="9666c-110">Configurez le système avec les informations renvoyées.</span><span class="sxs-lookup"><span data-stu-id="9666c-110">Configure the system with the returned information.</span></span>
4.  <span data-ttu-id="9666c-111">Appelez la fonction de rappel pfFreeInfo dans la structure de rappel pour libérer de la mémoire utilisée pour les informations renvoyées.</span><span class="sxs-lookup"><span data-stu-id="9666c-111">Call the pfFreeInfo callback function in the callback structure to free memory used for returned information.</span></span>
5.  <span data-ttu-id="9666c-112">S’il existe un message que l’extension souhaite ajouter au fichier journal d’analyse, appelez la fonction de rappel pfLogInfo dans la structure de rappel.</span><span class="sxs-lookup"><span data-stu-id="9666c-112">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
6.  <span data-ttu-id="9666c-113">Retournez les codes **SCESTATUS** appropriés.</span><span class="sxs-lookup"><span data-stu-id="9666c-113">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="9666c-114">L’exemple suivant illustre une implémentation possible de [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="9666c-114">The following example shows one possible implementation of [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span></span> <span data-ttu-id="9666c-115">Notez que dans cet exemple, la fonction ProcessConfigurationLine définit la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="9666c-115">Note that in this example, the function ProcessConfigurationLine sets the service configuration.</span></span> <span data-ttu-id="9666c-116">L’implémentation de cette fonction n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="9666c-116">The implementation of this function is not shown.</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo
)
{
  
  ////////////////////////////////////////////////////
  // Define variables.
  ////////////////////////////////////////////////////
     PSCESVC_CONFIGURATION_INFO     pConfigInfo = NULL;
     SCESTATUS                      retCode;
     SCE_ENUMERATION_CONTEXT        EnumContext = 0;
  
     if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ) 
     {
        return(SCESTATUS_INVALID_PARAMETER);
     }
  
  
      ////////////////////////////////////////////////////
      // Retrieve configuration information and configure
      // system. 
      ////////////////////////////////////////////////////
      do
      {
            retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                  SceSvcConfigurationInfo,
                                  NULL,
                                  FALSE,
                                  (PVOID *)&pConfigInfo,
                                  &EnumContext
                                 );
            if (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
            {
              ULONG i:
              //////////////////////////////////////////////////
              // Configure system.
              /////////////////////////////////////////////////
              for(i = 0; < pConfigInfo->Count; i++)
              {
                if(pConfigInfo->Line[i].Key == NULL) 
                    continue;
                ProcessConfigurationLine(pConfigInfo->Line[i]);
              }
      
      
              //////////////////////////////////////////////////
              // Free data returned.
              /////////////////////////////////////////////////
              (*(pSceCbInfo->pfFreeInfo)) ((PVOPID)pConfigInfo);
              pConfigInfo = NULL;
            }
        } while (retCode == SCESTATUS_SUCCESS && CountReturned > 0);
  
  
  ////////////////////////////////////////////////////
  // Add code for other return codes if retCode is 
  // not SCESTATUS_SUCCESS.
  ///////////////////////////////////////////////////
  return retCode;
}
```



 

 



