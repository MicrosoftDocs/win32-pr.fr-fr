---
title: CENUMOBJ. COTISATIONS
description: Dans l’exemple de composant fournisseur, l’énumération d’un objet conteneur utilise les routines de cenumobj. cpp, énumérées dans le tableau suivant.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730196"
---
# <a name="cenumobjcpp"></a>CENUMOBJ. COTISATIONS

Dans l’exemple de composant fournisseur, l’énumération d’un objet conteneur utilise les routines de cenumobj. cpp, énumérées dans le tableau suivant.



| Méthode                                                 | Description                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObjectEnum :: Create**                     | Créez un objet pour permettre l’énumération des objets Active Directory génériques.                                                                                           |
| **CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**     | Initialisation.                                                                                                                                                       |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Gérer la récupération d’objets.                                                                                                                                          |
| **CSampleDSGenObjectEnum::FetchObjects**               | Récupérez l’ensemble de pointeurs [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui correspondent au filtre.                                                             |
| **CSampleDSGenObjectEnum::FetchNextObject**            | Récupérez un objet et comparez-le au filtre. Si elle correspond, encapsulez-la dans l’objet générique et retournez un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Gérer la récupération des objets.                                                                                                                                        |
| **CSampleDSGenObjectEnum :: suivant**                       | Récupère le nombre spécifié d’éléments de l’objet d’énumération indiqué.                                                                                      |
| **CSampleDSGenObjectEnum::IsValidDSFilter**            | Vérifiez que la classe d’objet en trouve une dans la liste de filtres.                                                                                                              |
| **CSampleDSGenObjectEnum::BuildDSFilterArray**         | Gérez le tableau de filtres.                                                                                                                                              |
| **CSampleDSGenObjectEnum::CreateAndAppendFilterEntry** | Ajoutez une nouvelle classe d’objet au filtre et définissez le filtre comme étant contigu.                                                                                                |
| **FreeFilterList**                                     | Libérez le filtre.                                                                                                                                                      |



 

 

 