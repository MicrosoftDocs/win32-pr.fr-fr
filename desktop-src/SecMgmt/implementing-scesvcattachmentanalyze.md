---
description: Doit récupérer les informations de configuration de la base de données de sécurité et du service, comparer les deux ensembles d’informations, puis mettre à jour la section d’analyse de la base de données de sécurité avec les différences éventuelles.
ms.assetid: f8420dde-55a2-40a0-b10d-140c28c0e9e4
title: Implémentation de SceSvcAttachmentAnalyze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f8501be2caac84c3dc96363eb85a8bc787d2be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324747"
---
# <a name="implementing-scesvcattachmentanalyze"></a>Implémentation de SceSvcAttachmentAnalyze

La fonction [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) doit extraire les informations de configuration de la base de données de sécurité et du service, comparer les deux ensembles d’informations, puis mettre à jour la section d’analyse de la base de données de sécurité avec les différences éventuelles. Vous pouvez vous en assurer en utilisant l’algorithme suivant.

**Pour implémenter SceSvcAttachmentAnalyze**

1.  Définissez les variables nécessaires à la récupération et à la définition des informations de sécurité et des codes de retour.
2.  Appelez la fonction de rappel pfQueryInfo dans la structure de rappel pour récupérer les informations de configuration de la base de données de sécurité.
3.  Récupérez les informations correspondantes à partir du service.
4.  Comparez les données de configuration récupérées du service à celles récupérées à partir de la base de données de sécurité.
5.  Si les informations ne sont pas les mêmes, appelez la fonction de rappel pfSetInfo dans la structure de rappel pour mettre à jour la base de données.
6.  Libère toutes les mémoires tampons utilisées pour récupérer des informations. Appelez la fonction de rappel pfFreeInfo dans la structure de rappel pour libérer de la mémoire utilisée pour les informations de base de données retournées.
7.  S’il existe un message que l’extension souhaite ajouter au fichier journal d’analyse, appelez la fonction de rappel pfLogInfo dans la structure de rappel.
8.  Retournez les codes **SCESTATUS** appropriés.

L’exemple suivant illustre une implémentation possible de [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md). Notez que dans cet exemple, les fonctions QueryConfigurationLine et CompareValue interrogent respectivement les informations du service et les comparent à celles récupérées de la base de données de sécurité. L’implémentation de ces fonctions n’est pas affichée.


```C++
#include <windows.h>

SCESTATUS WINAPI SceSvcAttachmentAnalyze (
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
  // Retrieve information from security database.
  ///////////////////////////////////////////////////
    do
    {
        retCode =  (*(pSceCbInfo->pfQueryInfo))(
                              pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              NULL,
                              FALSE,
                              &pConfigInfo,
                              &EnumContext
                              );
        if(retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
        {
          ULONG i;
          for(i = 0;i < pConfigInfo->Count; i++)
          {
            if(pConfigInfo->Line[I].Key == NULL) 
                continue;
        
        //////////////////////////////////////////////
        // Query service for corresponding key.
        //////////////////////////////////////////////
            QueryConfigurationLine(
                               pConfigInfo->Line[i].Key,
                               &SystemValue);
        
        //////////////////////////////////////////////
        // Compare values.
        //////////////////////////////////////////////
            CompareValue(
                     pConfigInfo->Line[i].Key,
                     SystemValue,
                     pConfigInfo->Line[i].Value,
                     &Result);
        
        //////////////////////////////////////////////
        // Write to security database if values are 
        // not equal.
        //////////////////////////////////////////////
            if(Result != NULL)
            {
              retCode =  (*(pSceCbInfo->pfSetInfo))(pSceCbInfo->sceHandle,
                                      SceSvcAnalysisInfo,
                                      pConfigInfo->Line[i].Key,
                                      TRUE,
                                      Result);
              if(retCode != SCESTATUS_SUCCESS)
              {
                //////////////////////////////////////////
                // Add code to handle other return codes.
                //////////////////////////////////////////
              }
            }
        }
      
          //////////////////////////////////////////////
          // Free all buffers used to retrieve 
          // SceSvcFree frees memory allocated by call 
          // to SceSvcQueryQueryInfo. 
          /////////////////////////////////////////
        (*(pSceCbInfo->pfFreeInfo)) (PVOID)pConfigInfo);
          pConfigInfo = NULL;
    }
  } while (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL);
  
  
  //////////////////////////////////////////////////
  // If the return code is not SCESTATUS_SUCCESS, add code to 
  // set error message appropriately.
  //////////////////////////////////////////////////
  return retCode;
}
```



 

 



