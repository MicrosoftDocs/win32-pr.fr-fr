---
description: Pour utiliser des propriétés dans votre installation, vous pouvez récupérer et définir des valeurs de propriété à partir de programmes à l’aide de MsiGetProperty et MsiSetProperty et les inclure dans le cadre des instructions conditionnelles de la base de données d’installation.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: obtention et définition des propriétés (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1009fc9370a870c53b3fe5ad471f52dea195648b36bab28dff76fe1271283be1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635949"
---
# <a name="getting-and-setting-properties-windows-installer"></a>obtention et définition des propriétés (Windows Installer)

Pour utiliser des [Propriétés](properties.md) dans votre installation, vous pouvez récupérer et définir des valeurs de propriété à partir de programmes à l’aide de [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) et [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) et les inclure dans le cadre des instructions conditionnelles de la base de données d’installation.

-   Pour obtenir une propriété actuelle, appelez la fonction [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) .
-   Pour obtenir l’état d’installation actuel, appelez la fonction [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .
-   Pour obtenir la langue de l’installation actuelle, appelez la fonction [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) .
-   Pour définir une propriété, appelez la fonction [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) .
-   Pour définir l’état de l’installation, appelez la fonction [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) .
-   Pour effacer une propriété (en lui affectant la valeur null), définissez la valeur de la propriété sur une chaîne vide : "".

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de propriétés](using-properties.md)
</dt> <dt>

[Définition des valeurs de propriété publiques sur la ligne de commande](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[Suppression d’une propriété du programme d’installation](clearing-an-installer-property.md)
</dt> </dl>

 

 



