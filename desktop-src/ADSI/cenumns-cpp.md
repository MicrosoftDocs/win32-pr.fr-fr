---
title: CENUMNS. COTISATIONS
description: Dans l’exemple de composant fournisseur, l’énumération d’un objet Namespace utilise les méthodes de cenumns. cpp, listées dans le tableau suivant.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106518035"
---
# <a name="cenumnscpp"></a>CENUMNS. COTISATIONS

Dans l’exemple de composant fournisseur, l’énumération d’un objet Namespace utilise les méthodes de cenumns. cpp, listées dans le tableau suivant.



| Méthode                                              | Description                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSNamespaceEnum :: Create**                  | Créez un objet pour permettre l’énumération d’un objet d’espace de noms ADS.                                                                                         |
| **CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**  | Constructeur standard.                                                                                                                                     |
| **CSampleDSNamespaceEnum :: ~ CSampleDSNamespaceEnum** | Destructeur standard.                                                                                                                                      |
| **CSampleDSNamespaceEnum :: suivant**                    | Récupère le nombre spécifié d’éléments de l’objet d’espace de noms indiqué.                                                                            |
| **CSampleDSNamespaceEnum :: EnumObjects**             | Gérer la récupération des pointeurs d’interface aux objets.                                                                                                  |
| **CSampleDSNamespaceEnum::FetchObjects**            | Récupérez l’ensemble de pointeurs [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .                                                                          |
| **CSampleDSNamespaceEnum::FetchNextObject**         | Extrait l’objet suivant. S’il est trouvé, créez un objet Active Directory générique et récupérez son pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . |



 

 

 