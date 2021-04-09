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
# <a name="implementing-scesvcattachmentconfig"></a>Implémentation de SceSvcAttachmentConfig

La fonction [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) doit extraire des informations de la base de données de sécurité, puis utiliser ces informations pour configurer le service.

Lors de l’implémentation de [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), vous pouvez récupérer toutes les informations, puis configurer le service, ou récupérer et configurer le service en étapes. L’algorithme suivant récupère toutes les informations, puis configure le service.

**Pour implémenter SceSvcAttachmentConfig**

1.  Définissez les variables nécessaires pour récupérer les informations et les codes de retour.
2.  Appelez la fonction de rappel pfQueryInfo dans la structure de rappel pour récupérer les informations de configuration de la base de données de sécurité.
3.  Configurez le système avec les informations renvoyées.
4.  Appelez la fonction de rappel pfFreeInfo dans la structure de rappel pour libérer de la mémoire utilisée pour les informations renvoyées.
5.  S’il existe un message que l’extension souhaite ajouter au fichier journal d’analyse, appelez la fonction de rappel pfLogInfo dans la structure de rappel.
6.  Retournez les codes **SCESTATUS** appropriés.

L’exemple suivant illustre une implémentation possible de [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md). Notez que dans cet exemple, la fonction ProcessConfigurationLine définit la configuration du service. L’implémentation de cette fonction n’est pas affichée.


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



 

 



