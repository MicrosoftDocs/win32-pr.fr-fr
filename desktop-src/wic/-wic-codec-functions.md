---
title: Fonctions WIC
description: Cette section contient des informations sur les fonctions WIC (Windows Imaging Component).
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ce53f51f439ab5d0a697c824a1d37db7fd755f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862478"
---
# <a name="wic-functions"></a>Fonctions WIC

Cette section contient des informations sur les fonctions WIC (Windows Imaging Component).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                      | Description                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*ProgressNotificationCallback*](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | Fonction de rappel définie par l’application appelée lorsque la progression du composant de codec est effectuée.<br/>                                                                                                                        |
| [**WICConvertBitmapSource**](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | Obtient un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) dans le format de pixel souhaité à partir d’un **IWICBitmapSource** donné.<br/>                                                                           |
| [**WICCreateBitmapFromSection**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | Retourne un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) qui est sauvegardé par les pixels d’un handle de section Windows Graphics Device Interface (GDI).<br/>                                                |
| [**WICCreateBitmapFromSectionEx**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | Retourne un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) qui est sauvegardé par les pixels d’un handle de section GDI.<br/>                                                                                    |
| [**WICGetMetadataContentSize**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | Retourne la taille du contenu des métadonnées contenues par le [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)spécifié. La taille retournée compte pour l’en-tête et la longueur des métadonnées.<br/> |
| [**WICMapGuidToShortName**](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | Obtient le nom abrégé associé à un GUID donné.<br/>                                                                                                                                                       |
| [**WICMapSchemaToName**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | Obtient le nom associé à un schéma donné.<br/>                                                                                                                                                           |
| [**WICMapShortNameToGuid**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | Obtient le GUID associé au nom abrégé donné.<br/>                                                                                                                                                     |
| [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | Obtient un GUID de format de métadonnées pour un format de conteneur spécifié et un fournisseur qui correspond le mieux au contenu d’un flux donné.<br/>                                                                            |
| [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | Écrit les métadonnées dans un flux donné.<br/>                                                                                                                                                                       |
| [Fonctions proxy WIC](wic-proxy-functions.md)<br/>                                  | Cette section contient les fonctions de proxy WIC.<br/>                                                                                                                                                             |



 

 

 




