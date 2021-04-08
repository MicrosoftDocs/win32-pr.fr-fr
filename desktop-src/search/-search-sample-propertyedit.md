---
description: L’exemple de code PropertyEdit montre comment convertir le nom de propriété canonique en PROPERTYKEY, définir la valeur de la Banque de propriétés sur celle de l’élément, puis réécrire les données dans le flux de fichier.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862166"
---
# <a name="propertyedit"></a>PropertyEdit

L’exemple de code PropertyEdit montre comment convertir le nom de propriété canonique en PROPERTYKEY, définir la valeur de la Banque de propriétés sur celle de l’élément, puis réécrire les données dans le flux de fichier.

Cette rubrique contient les sections suivantes.

-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="requirements"></a>Configuration requise



| Produit     | Version minimale du produit |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Kit de développement logiciel (SDK) Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement      | URL du chemin                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Exemple PropertyEdit](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.

 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **PropertyEdit** . 
2.  Entrez `msbuild PropertyEdit.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **PropertyEdit** .
2.  Double-cliquez sur l’icône du fichier PropertyEdit. sln pour ouvrir le projet dans Visual Studio.
    > [!Note]  
    > L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut. Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».

     

3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.
2.  À l’invite de commandes, entrez `PropertyEdit.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de PropertyEdit.exe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Rechercher des exemples de code](-search-samples-ovw.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[À propos des propriétés et gestionnaires de propriétés](../properties/building-property-handlers-properties.md)
</dt> <dt>

[Schéma de la description de propriété](/previous-versions//cc144127(v=vs.85))
</dt> </dl>

 

 
