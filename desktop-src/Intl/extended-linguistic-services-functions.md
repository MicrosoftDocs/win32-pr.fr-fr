---
description: ELS prend en charge les fonctions définies dans le tableau suivant.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Fonctions de services linguistiques étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541833"
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



 

 

 



