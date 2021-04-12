---
title: REGDSAPI. COTISATIONS
description: Dans l’exemple de composant fournisseur, les fonctions qui représentent une API qui accède directement au système d’exploitation natif se trouvent dans Regdsapi. cpp.
ms.assetid: dc5ab286-5c70-43a3-90a1-f3f8a1c61c43
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e160ab212960753c6f793f734ebd96dffdd0f9e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309229"
---
# <a name="regdsapicpp"></a>REGDSAPI. COTISATIONS

Dans l’exemple de composant fournisseur, les fonctions qui représentent une API qui accède directement au système d’exploitation natif se trouvent dans Regdsapi. cpp. L’exemple de composant de fournisseur implémente son service d’annuaire dans le registre. Pour écrire un fournisseur qui accède à votre propre service d’annuaire, créez vos propres implémentations de cette API. Les fonctions prises en charge sont répertoriées dans le tableau suivant.



| Méthode                             | Description                                                                                                                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SampleDSOpenObject**             | Ouvrez cet objet par nom. Si le paramètre de type de classe de schéma est **null**, renseignez le type trouvé. Récupérez un handle sur l’objet.                                                             |
| **SampleDSCloseObject**            | Utilisez le handle récupéré par **SampleDSOpenObject**.                                                                                                                                            |
| **SampleDSRDNEnum**                | Récupérez le descripteur sur un objet énumérateur pour gérer l’énumération de noms uniques relatifs (RDN) à partir d’un objet conteneur.                                                          |
| **SampleDSNextRDN**                | À l’aide du handle récupéré par **SampleDSRDNEnum**, récupérez le nom unique relatif suivant de cet objet conteneur.                                                                        |
| **SampleDSFreeEnum**               | Libérer l’objet énumérateur alloué dans **SampleDSRDNEnum**.                                                                                                                                   |
| **SampleDSModifyObject**           | Modifiez les propriétés d’un objet dans le service d’annuaire en fonction du handle de l’objet et d’une liste d’attributs et de leurs valeurs.                                                              |
| **SampleDSReadObject**             | Lisez les propriétés de l’objet à partir du service d’annuaire. Mappez la syntaxe du stockage natif aux valeurs de syntaxe ADS appropriées. Gérer les propriétés avec plusieurs valeurs en conséquence. |
| **SampleDSGetPropertyDefinition**  | Dans le schéma, recherchez toutes les définitions de propriétés et leurs attributs pour ce type d’objet de classe de schéma.                                                                                     |
| **SampleDSGetPropertyDefinition**  | Dans le schéma, recherchez cette propriété et ses attributs par nom.                                                                                                                               |
| **SampleDSFreePropertyDefinition** | Mémoire disponible allouée par **GetPropertyDefinition**.                                                                                                                                            |
| **SampleDSGetTypeText**            | Obtient le type de classe de schéma d’un objet au format texte.                                                                                                                                         |
| **SampleDSGetType**                | Obtient le type de classe de schéma d’un objet.                                                                                                                                                        |
| **SampleDSGetPropertyInfo**        | À partir d’un handle sur l’objet de classe de schéma et d’un nom de propriété, récupérez les informations de propriété, telles que la syntaxe, et ainsi de suite.                                                                      |
| **FreeList**                       | Libère la mémoire utilisée par une \_ liste LPWStr.                                                                                                                                                        |
| **SampleDSGetClassDefinition**     | Récupérez l’ensemble de toutes les définitions de classe de schéma et leurs données associées à partir du schéma.                                                                                                    |
| **SampleDSGetClassDefinition**     | Récupérez les données relatives à une classe de schéma particulière dans le schéma.                                                                                                                                   |
| **SampleDSGetClassInfo**           | À partir du nom d’une classe de schéma, recherchez ses données associées, comme les propriétés obligatoires.                                                                                                      |
| **SampleDSAddObject**              | Ajoutez un objet dans le service d’annuaire.                                                                                                                                                        |
| **SampleDSRemoveObject**           | Supprimer un objet du service d’annuaire.                                                                                                                                                   |
| **SampleDSCreateBuffer**           | Créez une mémoire tampon pour les données d’attribut et les données d’opération.                                                                                                                                  |
| **SampleDSFreeBuffer**             | Libérez la mémoire tampon créée dans **SampleDSCreateBuffer**.                                                                                                                                           |



 

 

 




