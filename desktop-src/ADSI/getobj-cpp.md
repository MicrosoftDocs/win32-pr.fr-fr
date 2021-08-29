---
title: GETOBJ. COTISATIONS
description: Dans l’exemple de composant fournisseur, apparaît un exemple de code utilisé pour rechercher et lier des objets dans Getobj. cpp. Les routines prises en charge sont répertoriées dans le tableau suivant.
ms.assetid: d202e5ec-27b5-4809-a7fa-4a2e39c65295
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1bada2480c8d361ba6dc1b71928aa6d1a1f945c75e0202312cc7f3e34c97b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082573"
---
# <a name="getobjcpp"></a>GETOBJ. COTISATIONS

Dans l’exemple de composant fournisseur, apparaît un exemple de code utilisé pour rechercher et lier des objets dans Getobj. cpp. Les routines prises en charge sont répertoriées dans le tableau suivant.



| Élément                                | Description                                                                                                                                                                                                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RelativeGetObject**               | Obtient un objet par rapport à un ADsPath donné.                                                                                                                                                                                                                                                       |
| **GetObject**                       | Appelle **ADsObject** (Parse. cpp) pour vérifier la syntaxe du chemin d’accès, vérifie que le chemin d’accès a le jeton de fournisseur approprié et valide le type d’objet. Si aucune erreur n’existe, créez une instance du type d’objet approprié et récupérez un pointeur vers l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’objet. |
| **BuildADsPathFromDSPath**          | Génération d’une chaîne ADsPath à partir du chemin d’accès du répertoire natif.                                                                                                                                                                                                                                           |
| **BuildDSTreeNameFromADsPath**      | Utilisez l’ADsPath pour créer un chemin d’accès au répertoire d’arborescence possible pour le chemin d’accès du répertoire natif.                                                                                                                                                                                                           |
| **BuildDSPathFromADsPath**          | Utilise ADsPath et DSPathName.                                                                                                                                                                                                                                                                      |
| **BuildADsParentPath**              | Générez l’ADsPath vers le parent de cet objet.                                                                                                                                                                                                                                                  |
| **GetNamespaceObject**              | Validez et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) un exemple d’objet d’espace de noms.                                                                                                                                                                                                           |
| **ValidateNamespaceObject**         | Vérifiez que l’objet Namespace correspond au nom du fournisseur actuel.                                                                                                                                                                                                                               |
| **ValidateProvider**                | Validez le nom du fournisseur (respecte la casse).                                                                                                                                                                                                                                                          |
| **GetSchemaObject**                 | Validez et ouvrez le type d’objet de schéma approprié. Créez ensuite la bonne et récupérez le pointeur d’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) sur celle-ci.                                                                                                                                        |
| **ValidateSchemaObject**            | Vérifiez qu’il s’agit d’un type d’objet de schéma valide.                                                                                                                                                                                                                                                     |
| **ValidateObjectType**              | Vérifiez que le type d’objet existe dans le schéma.                                                                                                                                                                                                                                                 |
| **BuildSampleDSRootRDNFromADsPath** | Générez l’ADsPath vers le nœud racine pour le composant de l’exemple de fournisseur.                                                                                                                                                                                                                            |
| **BuildDSPathFromADsPath**          | Utilise ADsPath, DSRootRDN et DSPathName.                                                                                                                                                                                                                                                          |



 

 

 