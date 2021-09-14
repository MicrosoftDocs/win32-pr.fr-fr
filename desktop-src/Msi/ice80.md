---
description: ICE80 valide que la valeur de la propriété de résumé de modèle ( \_ modèle PID) spécifie correctement &\# 0034 ; Intel64&\# 0034 ;, &\# 0034 ; x64&\# 0034 ; ou &\# 0034 ; Intel&\# 0034 ; selon la présence de composants 64 bits ou de scripts d’action personnalisée.
ms.assetid: fd2a15cf-d117-4a87-a26e-caff4b12a2e9
title: ICE80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5233f260e9cc248bdb2d0c19b47956a2b7dbe1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021483"
---
# <a name="ice80"></a>ICE80

ICE80 valide que la valeur de la propriété de [**Résumé de modèle**](template-summary.md) ( \_ modèle PID) spécifie correctement « Intel64 », « x64 », « Arm64 » ou « Intel », en fonction de la présence de composants 64 bits ou de scripts d’action personnalisés. ICE80 vérifie la [table](component-table.md) des composants pour tous les composants avec l’attribut **msidbComponentAttributes64bit** et vérifie la [table CustomAction](customaction-table.md) pour tous les scripts avec l’attribut **msidbCustomActionType64BitScript** . ICE80 vérifie qu’un package avec « Intel64 », « x64 » ou « Arm64 » dans sa propriété **Summary de modèle** a également une propriété de résumé du [**nombre de pages**](page-count-summary.md) (PID \_ PAGECOUNT) d’au moins 150.

ICE80 vérifie également que l’ID de langue spécifié par la propriété [**ProductLanguage**](productlanguage.md) doit être contenu dans la propriété [**Résumé du modèle**](template-summary.md) .

pour plus d’informations, consultez [Windows Installer sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md).

## <a name="result"></a>Résultats

ICE80 publie les erreurs suivantes.



| Erreur                                                                                                                                                                   | Description                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ce package contient le composant 64 bit « \[ 1 \] », mais la propriété [**Résumé du modèle**](template-summary.md) ne contient pas Intel64, x64 ou Arm64.                    | La [table Component](component-table.md)contient un composant avec l’attribut **msidbComponentAttributes64bit** et la propriété [**Résumé du modèle**](template-summary.md) ne contient pas Intel64, x64 ou Arm64.        |
| Ce package contient le script d’action personnalisée 64 bits « \[ 1 \] », mais la propriété [**Résumé du modèle**](template-summary.md) ne contient pas Intel64, x64 ou Arm64.         | La [table CustomAction](customaction-table.md) contient une action personnalisée de script avec **msidbCustomActionType64BitScript** mais la propriété [**Résumé du modèle**](template-summary.md) ne contient pas Intel64, x64 ou Arm64. |
| Valeur incorrecte dans le flux d’informations de résumé pour% s.                                                                                                                         | Valeur renvoyée pour \_ la propriété de modèle PID si cette propriété est une chaîne vide ou n’est pas de \_ type VT LPSTR. Renvoyé pour PID \_ PageCount si cette propriété n’est pas de \_ type VT I4.<br/>                                         |
| Ce package est marqué avec Intel64 mais son schéma est inférieur à 150.                                                                                                  | La \_ propriété de modèle PID du package est Intel64, mais sa \_ propriété PID PageCount est inférieure à 150.                                                                                                            |
| Ce package est marqué avec x64, mais son schéma est inférieur à 200.                                                                                                      | La \_ propriété de modèle PID du package est x64, mais sa \_ propriété PID PageCount est inférieure à 200.                                                                                                            |
| Ce package est marqué avec Arm64, mais son schéma est inférieur à 500.                                                                                                    | La \_ propriété de modèle PID du package est Arm64, mais sa \_ propriété PID PageCount est inférieure à 500.                                                                                                            |
| Ce package 32 bits utilise la propriété 1 de 64 bits \[\]                                                                                                                       | Un package 32 bits utilise une propriété 64 bits.                                                                                                                                                                              |
| Ce package 32 bits utilise le type de localisateur 64 bit dans l’entrée de table RegLocator \[ 1\]                                                                                         | Un package 32 bits contient **msidbLocatorType64bit** dans le champ type de la [table RegLocator](reglocator-table.md).                                                                                                    |
| Ce 64BitComponent \[ 1 \] utilise 32BitDirectory \[ 3\]                                                                                                                     | Un composant 64 bits utilise un répertoire 32 bits.                                                                                                                                                                           |
| Ce 32BitComponent \[ 1 \] utilise 64BitDirectory \[ 3\]                                                                                                                     | Un composant 32 bits utilise un répertoire 64 bits.                                                                                                                                                                           |
| La propriété «[**ProductLanguage**](productlanguage.md)» dans la table de propriétés a la valeur « \[ 2 \] », qui n’est pas contenue dans le flux de propriétés de résumé du modèle. | La valeur de la propriété [**ProductLanguage**](productlanguage.md) n’est pas indiquée dans la propriété [**Résumé du modèle**](template-summary.md) .                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> <dt>

[Windows Programme d’installation sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md)
</dt> </dl>

 

 




