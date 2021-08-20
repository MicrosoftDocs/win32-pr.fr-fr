---
title: Constantes ADSI
description: Le tableau suivant répertorie les constantes définies et utilisées dans les interfaces de service Active Directory (ADSI).
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca2a6b7eae4550f4bbd4c8c8373d63c9bdd121e6561f08e591cb6a943d309f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023917"
---
# <a name="adsi-constants"></a>Constantes ADSI

Le tableau suivant répertorie les constantes définies et utilisées dans les interfaces de service Active Directory (ADSI).



| Constante ADSI                      | Valeur                                   | Description                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_INITCREDENTIALS ext \_ ads**      | 1                                       | Code de contrôle qui indique que les données personnalisées fournies à la méthode [**IADsExtension :: action**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contiennent les informations d’identification de l’utilisateur.                                                     |
| **\_ \_ initialisation d’AD ext \_ terminée** | 2                                       | Code de contrôle utilisé avec [**IADsExtension :: action**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) pour indiquer que les extensions peuvent effectuer toute initialisation nécessaire, en fonction des fonctionnalités prises en charge par l’objet parent. |
| **\_MAXEXTDISPID ext \_ ads**         | 16777215                                | DISPID le plus élevé qu’un objet d’extension peut utiliser pour ses méthodes et propriétés.                                                                                                                                   |
| **\_MINEXTDISPID ext \_ ads**         | 1                                       | DISPID le plus bas qu’un objet d’extension peut utiliser pour ses méthodes et propriétés.                                                                                                                                    |
| **\_réponse VLV \_ ads**             | L « fc8cb04d-311D-406c-8CB9-1ae8b843b419 » | Utilisé avec la méthode [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) pour récupérer les métadonnées de recherche VLV. Pour plus d’informations, consultez [Comment effectuer une recherche à l’aide de VLV](how-to-search-using-vlv.md).        |
| **DBPROPFLAGS \_ ADSISEARCH**        | 0x0000C000                              | Utilisé pour travailler avec le fournisseur de OLE DB.                                                                                                                                                                           |



 

 

 




