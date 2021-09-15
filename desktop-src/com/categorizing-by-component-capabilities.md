---
title: Catégorisation par fonctionnalités de composant
description: Les catégories de composants peuvent être utilisées pour afficher un sous-ensemble de tous les composants installés.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411274"
---
# <a name="categorizing-by-component-capabilities"></a>Catégorisation par fonctionnalités de composant

Les catégories de composants peuvent être utilisées pour afficher un sous-ensemble de tous les composants installés. Chaque catégorie de composant est identifiée par un GUID, connu sous le nom d’ID de catégorie (CATID). Chaque CATID contient une liste de noms explicites et explicites qui lui sont associés. Une liste des CATID et des noms explicites est stockée dans un emplacement bien connu du Registre.

Par exemple, tous les composants qui implémentent la fonctionnalité d’incorporation de documents OLE peuvent être classés dans une catégorie de composant. Dans le passé, ces objets auraient été identifiés par la clé « Insertable » dans le registre. Pour utiliser des catégories de composant à la place, les informations suivantes sont ajoutées au registre :

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

Chaque classe qui implémente les fonctionnalités correspondant à une catégorie de composant répertorie l’ID de catégorie de cette catégorie dans la clé CLSID du Registre. Étant donné qu’un seul composant peut prendre en charge un large éventail de fonctionnalités, les composants peuvent appartenir à plusieurs catégories de composants. par exemple, un contrôle ole particulier peut prendre en charge toutes les fonctionnalités requises pour participer en tant qu’incorporation de documents ole, Microsoft Visual Basic la liaison de données et les fonctionnalités Internet. Ce type de contrôle aurait les informations suivantes stockées dans sa clé CLSID dans le registre :

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

Grâce à ces informations, un conteneur peut énumérer les contrôles installés sur un système et afficher uniquement les contrôles qui prennent en charge les fonctionnalités requises par le conteneur. L’utilisation de catégories de composants permet de classer les composants par la fonctionnalité implémentée du composant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Association d’icônes à une catégorie](associating-icons-with-a-category.md)
</dt> <dt>

[Catégorisation par fonctionnalités de conteneur](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classes et associations par défaut](default-classes-and-associations.md)
</dt> <dt>

[Définition des catégories de composants](defining-component-categories.md)
</dt> <dt>

[Gestionnaire de catégories de composants](the-component-categories-manager.md)
</dt> </dl>

 

 




