---
description: Les fonctions suivantes sont utilisées pour gérer les tickets d’impression.
ms.assetid: 9e942a1d-660b-4691-9282-ffb49e0b9848
title: Fonctions de l’API ticket d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5dfda941d0b0f7d99b0ffbef703a98e357ccc6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866177"
---
# <a name="print-ticket-api-functions"></a>Fonctions de l’API ticket d’impression

Les fonctions suivantes sont utilisées pour gérer les tickets d’impression.

## <a name="in-this-section"></a>Dans cette section



| Fonction                                                                                  | Description                                                                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertDevModeToPrintTicketThunk2**](convertdevmodetoprintticketthunk2.md)<br/> | Convertit une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en un ticket d’impression.<br/>                                                                          |
| [**ConvertPrintTicketToDevModeThunk2**](convertprinttickettodevmodethunk2.md)<br/> | Convertit un ticket d’impression en une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .<br/>                                                                          |
| [**MergeAndValidatePrintTicketThunk2**](mergeandvalidateprintticketthunk2.md)<br/> | Fusionne deux tickets d’impression et retourne un ticket d’impression valide et viable.<br/>                                                                          |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)<br/>                                     | Ferme un handle de fournisseur de tickets d’impression.<br/>                                                                                                      |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)<br/>         | Convertit une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en un ticket d’impression à l’intérieur d’un [**IStream**](/windows/desktop/Stg/istream-compound-file-implementation).<br/>        |
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)<br/>         | Convertit un ticket d’impression en une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .<br/>                                                                        |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)<br/>                       | Récupère les fonctionnalités de l’imprimante mises en forme en conformité avec le [schéma d’impression](./printschema.md)XML.<br/>                   |
| [**PTGetPrintDeviceCapabilities**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities)<br/>    | Récupère les fonctionnalités de l’imprimante de périphérique mises en forme en conformité avec le [schéma d’impression](./printschema.md)XML.<br/>            |
| [**PTGetPrintDeviceResources**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdeviceresources)<br/>          | Il récupère les ressources des périphériques d’impression pour une imprimante mise en forme conformément au [schéma d’impression](./printschema.md)XML.<br/> |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)<br/>         | Fusionne deux tickets d’impression et retourne un ticket d’impression valide et viable.<br/>                                                                          |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)<br/>                                       | Ouvre une instance d’un fournisseur de tickets d’impression.<br/>                                                                                               |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)<br/>                                   | Ouvre une instance d’un fournisseur de tickets d’impression.<br/>                                                                                               |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)<br/>             | Récupère la version la plus élevée (la plus récente) du [schéma d’impression](./printschema.md) que l’imprimante spécifiée prend en charge.<br/>           |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)<br/>                                     | Libère les mémoires tampons associées aux tickets d’impression et aux fonctionnalités d’impression.<br/>                                                                      |
| [**UnbindPTProviderThunk**](unbindptproviderthunk.md)<br/>                         | Ferme un handle vers un fournisseur de tickets d’impression.<br/>                                                                                                 |



 

 

