---
description: Moniteur réseau comprend les fonctions d’objet BLOB suivantes.
ms.assetid: 90514067-59e9-4bd9-8612-2263bd414574
title: Fonctions d’objet BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654fb7e7c6879a6df0f3b4aad4d29007a9405186631bd4d9c4dc1a24e606eb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144362"
---
# <a name="blob-functions"></a>Fonctions d’objet BLOB

Moniteur réseau comprend les fonctions d’objet BLOB suivantes.



| Fonction                                                       | Description                                                                                                                      |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [CreateBlob](createblob.md)                                   | Crée un objet BLOB vide.                                                                                                           |
| [CreateNPPInterface](createnppinterface.md)                   | Crée une interface NPP avec un objet BLOB donné.                                                                                      |
| [DestroyBlob](destroyblob.md)                                 | Libère toute la mémoire associée à un objet BLOB donné.                                                                                   |
| [DuplicateBlob](duplicateblob.md)                             | Copie un objet BLOB donné.                                                                                                             |
| [GetBoolFromBlob](getboolfromblob.md)                         | Récupère la valeur booléenne nommée à partir d’un objet BLOB donné.                                                                             |
| [GetClassIDFromBlob](getclassidfromblob.md)                   | Récupère la valeur de l’identificateur de classe nommée à partir d’un objet BLOB donné.                                                                    |
| [GetDwordFromBlob](getdwordfromblob.md)                       | Récupère la valeur **DWORD** nommée à partir d’un objet BLOB donné.                                                                           |
| [GetMacAddressFromBlob](getmacaddressfromblob.md)             | Récupère l’adresse MAC nommée à partir d’un objet BLOB donné.                                                                               |
| [GetNetworkInfoFromBlob](getnetworkinfofromblob.md)           | Récupère des informations réseau à partir d’un objet BLOB donné.                                                                                 |
| [GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md) | Récupère les informations de filtre d’adresse d’un objet BLOB donné.                                                                          |
| [GetNPPBlobFromUI](getnppblobfromui.md)                       | Affiche la boîte de dialogue **Sélectionner un réseau** et retourne l’objet BLOB NPP de la carte réseau sélectionnée.                                       |
| [GetNPPBlobTable](getnppblobtable.md)                         | Récupère une table d’objets BLOB.                                                                                                      |
| [GetNPPEtypeSapFilter](getnppetypesapfilter.md)               | Récupère le filtre ETYPE/SAP d’un objet BLOB donné.                                                                                |
| [GetNPPMacTypeAsNumber](getnppmactypeasnumber.md)             | Récupère le type MAC de la catégorie **NetworkInfo** de la section NPP et convertit les informations en un numéro de type Mac. |
| [GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md) | Récupère le filtre de correspondance de modèle à partir d’un objet BLOB donné.                                                                            |
| [GetNPPTriggerFromBlob](getnpptriggerfromblob.md)             | Récupère le déclencheur d’un objet BLOB donné.                                                                                           |
| [GetStringFromBlob](getstringfromblob.md)                     | Récupère une chaîne unique à partir d’un emplacement spécifique dans un objet BLOB donné.                                                          |
| [GetStringsFromBlob](getstringsfromblob.md)                   | Récupère toutes les chaînes dans les limites spécifiées à partir d’un objet BLOB donné.                                                          |
| [IsRemoteNPP](isremotenpp.md)                                 | Indique si l’objet BLOB donné spécifie un NPP distant.                                                                         |
| [MergeBlob](mergeblob.md)                                     | Fusionne les informations dans les objets BLOB source et cible et remplace les entrées communes par les données de l’objet BLOB source.                  |
| [RegCreateBlobKey](regcreateblobkey.md)                       | Stocke un objet BLOB à la clé de Registre donnée.                                                                                         |
| [RegOpenBlobKey](regopenblobkey.md)                           | Récupère un objet BLOB stocké à la clé de Registre donnée.                                                                               |
| [RemoveFromBlob](removefromblob.md)                           | Supprime des informations de n’importe quel niveau d’un objet BLOB donné.                                                                              |
| [SelectNPPBlobFromTable](selectnppblobfromtable.md)           | Sélectionne un objet BLOB NPP dans une table.                                                                                                |
| [SetBoolInBlob](setboolinblob.md)                             | Définit une valeur booléenne à l’emplacement donné dans un objet BLOB.                                                                        |
| [SetClassIDInBlob](setclassidinblob.md)                       | Définit la valeur de l’identificateur de classe nommée pour un objet BLOB.                                                                                |
| [SetDwordInBlob](setdwordinblob.md)                           | Définit la valeur **DWORD** nommée pour un objet BLOB.                                                                                       |
| [SetMacAddressInBlob](setmacaddressinblob.md)                 | Définit l’adresse MAC nommée pour un objet BLOB.                                                                                           |
| [SetNetworkInfoInBlob](setnetworkinfoinblob.md)               | Définit les informations réseau d’un objet BLOB.                                                                                         |
| [SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)     | Définit le filtre d’adresse donné dans l’objet BLOB.                                                                                       |
| [SetNPPEtypeSapFilter](setnppetypesapfilter.md)               | Définit le filtre ETYPE/SAP dans un objet BLOB.                                                                                             |
| [SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)     | Définit le filtre de correspondance de modèle pour un objet BLOB.                                                                                        |
| [SetNPPTriggerInBlob](setnpptriggerinblob.md)                 | Définit le déclencheur dans un objet BLOB.                                                                                                      |
| [SetStringInBlob](setstringinblob.md)                         | Définit la chaîne à un emplacement donné au sein d’un objet BLOB.                                                                               |
| [WriteBlobToFile](writeblobtofile.md)                         | Écrit un objet BLOB dans un fichier donné.                                                                                                   |



 

 

 



