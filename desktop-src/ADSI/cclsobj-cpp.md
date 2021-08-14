---
title: CCLSOBJ. COTISATIONS
description: Dans l’exemple de composant fournisseur, les fonctions de l’objet de classe de schéma sont contenues dans cclsobj. cpp.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- CSampleDSClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a24efbabe20a227ef91cb8f70e201a0562257e42cc926ba96b46b32e7a7d9568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180384"
---
# <a name="cclsobjcpp"></a>CCLSOBJ. COTISATIONS

Dans l’exemple de composant fournisseur, les fonctions de l’objet de classe de schéma sont contenues dans cclsobj. cpp.

La classe **CSampleDSClass** est définie dans ce fichier. **CSampleDSClass** est défini avec les méthodes et les propriétés énumérées dans le tableau suivant.



| Méthode                      | Description                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSClass**          | Constructeur standard.                                                                                                                                                                                      |
| **~ CSampleDSClass**         | Destructeur standard.                                                                                                                                                                                       |
| **CreateClass**             | Créez un objet de classe de schéma ADs. Recherchez les définitions d’attribut en appelant **SampleDSGetClassDefinition**.                                                                                                 |
| **CreateClass**             | Créez un objet de classe de schéma, en fonction des définitions d’attributs, en définissant des attributs connus, tels que ceux répertoriés dans [**IADsClass :: MandatoryAttributes**](iadsclass-property-methods.md).                     |
| **AllocateClassObject**     | Créez un objet de classe de schéma et chargez ses données de type.                                                                                                                                                       |
| **QueryInterface**          | Retourne le pointeur d’interface demandé, s’il est disponible.                                                                                                                                                      |
| Méthodes IADs standard.      | Méthodes d’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard incluses dans ce fichier.                                                                                                                                     |
| Méthodes IADsClass standard. | Méthodes d’interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) standard incluses dans ce fichier.                                                                                                                           |
| **CreatePropertyList**      | Créez une liste de propriétés associées à cette classe de schéma en appelant **CreatePropertyEntry**.                                                                                                          |
| **CreatePropertyEntry**     | Créez un objet de propriété dans cette classe de schéma.                                                                                                                                                           |
| **FreePropertyEntry**       | Libérez l’entrée dans **CreatePropertyEntry**.                                                                                                                                                            |
| **MakeVariantFromPropList** | Créez un tableau de VARIANTs à partir de la liste de propriétés créée par **CreatePropertyList**. Peut être utilisé dans l’implémentation de [**IADsClass :: MandatoryAttributes**](iadsclass-property-methods.md) , et ainsi de suite. |



 

 

 




