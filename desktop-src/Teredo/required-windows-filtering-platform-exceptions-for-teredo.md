---
title: Windows Filtrage des exceptions de plateforme pour Teredo
description: les Exceptions qui permettent aux applications de recevoir le trafic non sollicité via Teredo via un pare-feu doivent être créées à l’aide de Windows api de filtre de la plateforme.
ms.assetid: 8e562757-cd31-4c83-bf4a-92c2e0d3f2ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd4d84b97afeaf1157eaac3cd9cc5fc3e24aff0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193455"
---
# <a name="windows-filtering-platform-exceptions-for-teredo"></a>Windows Filtrage des exceptions de plateforme pour Teredo

les Exceptions qui permettent aux applications de recevoir le trafic non sollicité via [Teredo](about-teredo.md) via un pare-feu doivent être créées à l’aide de Windows api de filtre de la [plateforme](/windows/desktop/FWP/windows-filtering-platform-start-page) . Pour ce faire, vous devez ouvrir les exceptions entrantes et sortantes basées sur l’application (application <app name> ) dans la sous-couche Teredo de ALE pour le trafic IPv6. Cela garantit que seules les applications avec l’exception Teredo peuvent utiliser Teredo. Soyez vigilant lors de la création de ces exceptions. L’utilisation de l’option générale « \* » (tout) peut permettre aux programmes non enregistrés avec la sous-couche Teredo ou le trafic du tunnel de transmettre le pare-feu et de compromettre la sécurité.

Dans tous les cas, au moins une application bloquée est nécessaire, mais il peut y avoir zéro ou plusieurs applications autorisées ajoutées par un pare-feu en fonction du nombre d’applications qui doivent être autorisées.

L’exemple suivant illustre l’utilisation d’un bloc allow et One.


```C++
/*--
Routine Description:

    Adds the necessary filters to permit specific applications and block all other
    via the Windows Filtering Platform (WFP).

Arguments:
   
   [in] HANDLE engineHandle - Handle to the base firewall engine.
   [in] FWP_BYTE_BLOB* applicationId - Identifier for this application.

Return Value:

    NO_ERROR or a specific Result

--*/
   DWORD Result = NO_ERROR;
   FWPM_FILTER0 Filter;
   FWPM_FILTER_CONDITION0 FilterConditions[3]; // We only need three.
   DWORD TempResult;
   FWP_BYTE_BLOB* applicationId;

   printf("Starting Transaction\n");

   Result = FwpmTransactionBegin0(engineHandle, 0);
   if (NO_ERROR != Result)
   {
      goto abort;
   }
   
   printf("Successfully Started Transaction\n");

   RtlZeroMemory(&Filter, sizeof(FWPM_FILTER0));

   Filter.layerKey = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6;
   Filter.displayData.name = L"Teredo Filter for Application Specific Permit";
   Filter.displayData.description = L"Implement Teredo Filter for Application Specific Permit at the Recv Accept layer";
   Filter.action.type = FWP_ACTION_PERMIT;
   Filter.subLayerKey = FWPM_SUBLAYER_TEREDO;
   Filter.weight.type = FWP_EMPTY; // auto-weight
   Filter.filterCondition = FilterConditions;
   Filter.numFilterConditions = 3;

   RtlZeroMemory(FilterConditions, sizeof(FilterConditions));

   //
   // Enable this for IfType == Tunnel, TunnelType == Teredo.
   //
   FilterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   FilterConditions[0].matchType = FWP_MATCH_EQUAL;
   FilterConditions[0].conditionValue.type = FWP_UINT32;
   FilterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   //
   // Enable this for IfType == Tunnel, TunnelType == Teredo.
   //
   FilterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   FilterConditions[1].matchType = FWP_MATCH_EQUAL;
   FilterConditions[1].conditionValue.type = FWP_UINT32;
   FilterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   //
   // Add a permitted application.
   //
   FilterConditions[2].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   FilterConditions[2].matchType = FWP_MATCH_EQUAL;
   FilterConditions[2].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   FilterConditions[2].conditionValue.byteBlob = applicationId;

   printf("Adding Recv Accept Application specific V6 Teredo Filter.\n");

   Result = FwpmFilterAdd0(engineHandle,
                           &Filter,
                           NULL,
                           NULL);

   if (NO_ERROR != Result)
   {
      goto abort;
   }
   
   printf("Successfully added Recv Accept Application specific V6 Teredo Filter.\n");

   Filter.layerKey = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6;
   Filter.displayData.name = L"Teredo Filter for Blocking other applications";
   Filter.displayData.description = L"This blocks any other traffic coming in over the Teredo interface that hasn't explicitly been permitted.";
   Filter.action.type = FWP_ACTION_BLOCK;
   Filter.subLayerKey = FWPM_SUBLAYER_TEREDO;
   Filter.weight.type = FWP_EMPTY; // auto-weight
   Filter.filterCondition = FilterConditions;
   Filter.numFilterConditions = 2;

   RtlZeroMemory(FilterConditions, sizeof(FilterConditions));

   //
   // Enable this for IfType == Tunnel, TunnelType == Teredo.
   //
   FilterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   FilterConditions[0].matchType = FWP_MATCH_EQUAL;
   FilterConditions[0].conditionValue.type = FWP_UINT32;
   FilterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   //
   // Enable this for IfType == Tunnel, TunnelType == Teredo.
   //
   FilterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   FilterConditions[1].matchType = FWP_MATCH_EQUAL;
   FilterConditions[1].conditionValue.type = FWP_UINT32;
   FilterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   printf("Adding Recv Accept block all non-permitted V6 Teredo Filter.\n");

   Result = FwpmFilterAdd0(engineHandle,
                           &Filter,
                           NULL,
                           NULL);

   if (NO_ERROR != Result)
   {
      goto abort;
   }
   
   printf("Successfully added Recv Accept block all non-permitted V6 Teredo Filter.\n");

   printf("Committing Transaction\n");
   Result = FwpmTransactionCommit0(engineHandle);
   if (NO_ERROR == Result)
   {
      printf("Successfully Committed Transaction\n");
   }
   goto cleanup;

abort:
   printf("Aborting Transaction\n");
   TempResult = FwpmTransactionAbort0(engineHandle);
   if (NO_ERROR == TempResult)
   {
      printf("Successfully Aborted Transaction\n");
   }

cleanup:
   
   return Result;

```



 

 