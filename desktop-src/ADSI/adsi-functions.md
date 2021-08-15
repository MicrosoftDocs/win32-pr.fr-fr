---
title: Fonctions ADSI
description: Active Directory interfaces de service exposent les fonctions d’assistance suivantes aux clients qui n’utilisent pas Automation.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, référence, fonctions
- function ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7245069ca427cbf6b1e4548749636a2c8448c2d4b9853bb27f7fa273f4a19a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180613"
---
# <a name="adsi-functions"></a>Fonctions ADSI

Active Directory interfaces de service exposent les fonctions d’assistance suivantes aux clients qui n’utilisent pas Automation.



| Fonction                                           | Description                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | Crée un objet énumérateur pour l’objet conteneur ADSI spécifié.                              |
| [**ADsBuildVarArrayInt**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | Génère un tableau de variant à partir d’un tableau de **DWORD** s.                                                |
| [**ADsBuildVarArrayStr**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | Génère un tableau de variant à partir d’un tableau de chaînes Unicode.                                           |
| [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | Convertit un objet blob de données binaires au format approprié pour un filtre de recherche.                         |
| [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | Remplit un tableau de variants avec les éléments récupérés à partir de l’objet énumérateur spécifié.            |
| [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | Libère un objet énumérateur créé précédemment par [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator). |
| [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | Récupère la dernière valeur de code d’erreur du thread appelant.                                         |
| [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | Crée une liaison avec un objet ADSI à l’aide des informations d’identification actuelles.                                             |
| [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | Crée une liaison avec un objet ADSI à l’aide des informations d’identification spécifiées                                                |
| [**ADsSetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | Définit la valeur du code d’erreur du thread appelant.                                                   |
| [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | Alloue un bloc de mémoire.                                                                       |
| [**AllocADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | Alloue de la mémoire pour une chaîne donnée.                                                               |
| [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | Libère la mémoire allouée par [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).                                  |
| [**FreeADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | Libère la mémoire allouée pour la chaîne donnée.                                                   |
| [**ReallocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | Affecte le contenu de mémoire existant à un emplacement de mémoire nouvellement créé.                            |
| [**ReallocADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | Remplace une chaîne existante par une nouvelle.                                                        |



 

Les fonctions ADSI suivantes sont obsolètes.



| Fonction                                                  | Description |
|-----------------------------------------------------------|-------------|
| [**AdsFreeAllErrorRecords**](obsolete-adsi-functions.md) | Obsolète.   |
| [**AdsDecodeBinaryData**](obsolete-adsi-functions.md)    | Obsolète.   |
| [**PropVariantToAdsType**](obsolete-adsi-functions.md)   | Obsolète.   |
| [**AdsTypeToPropVariant**](obsolete-adsi-functions.md)   | Obsolète.   |
| [**AdsFreeAdsValues**](obsolete-adsi-functions.md)       | Obsolète.   |
| [**InitAdsMem**](obsolete-adsi-functions.md)             | Obsolète.   |
| [**AssertAdsmemLeaks**](obsolete-adsi-functions.md)      | Obsolète.   |
| [**DumpMemorytracker**](obsolete-adsi-functions.md)      | Obsolète.   |



 

 

 




