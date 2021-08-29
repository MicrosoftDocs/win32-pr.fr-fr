---
description: ELS prend en charge les fonctions définies dans le tableau suivant.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Fonctions de services linguistiques étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f7c798a71e9973bce2e7f1bf8720c30877ab87019eeaff103a73b9b0fb7afd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041509"
---
# <a name="extended-linguistic-services-functions"></a>Fonctions de services linguistiques étendues

ELS prend en charge les fonctions définies dans le tableau suivant.



| Fonction                                                 | Description                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | Fonction de rappel définie par l’application qui traite de façon asynchrone les données produites par la fonction **MappingRecognizeText** .                 |
| [**MappingDoAction**](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | Fait en sorte qu’un service ELS effectue une action après la reconnaissance du texte.                                                                |
| [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | Libère de la mémoire et des ressources allouées pendant une opération de reconnaissance de texte ELS.                                                                 |
| [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | Libère de la mémoire et des ressources allouées pour que l’application interagisse avec un ou plusieurs services ELS.                                            |
| [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | Récupère la liste des services pris en charge par la plateforme ELS disponibles, ainsi que les informations associées, en fonction des critères spécifiés par l’application. |
| [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | Appelle sur un service ELS pour reconnaître du texte.                                                                                                   |



 

 

 



