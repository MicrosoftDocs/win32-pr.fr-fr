---
description: Pour utiliser des propriétés dans votre installation, vous pouvez récupérer et définir des valeurs de propriété à partir de programmes à l’aide de MsiGetProperty et MsiSetProperty et les inclure dans le cadre des instructions conditionnelles de la base de données d’installation.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Obtention et définition des propriétés (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0154b84af656d295b9fa84ebcca881eab1c288f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866329"
---
# <a name="getting-and-setting-properties-windows-installer"></a><span data-ttu-id="94469-103">Obtention et définition des propriétés (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="94469-103">Getting and Setting Properties (Windows Installer)</span></span>

<span data-ttu-id="94469-104">Pour utiliser des [Propriétés](properties.md) dans votre installation, vous pouvez récupérer et définir des valeurs de propriété à partir de programmes à l’aide de [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) et [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) et les inclure dans le cadre des instructions conditionnelles de la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="94469-104">To use [properties](properties.md) in your installation, you can get and set property values from programs using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) and [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) and include as part of conditional statements in the installation database.</span></span>

-   <span data-ttu-id="94469-105">Pour obtenir une propriété actuelle, appelez la fonction [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) .</span><span class="sxs-lookup"><span data-stu-id="94469-105">To obtain a current property, call the [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) function.</span></span>
-   <span data-ttu-id="94469-106">Pour obtenir l’état d’installation actuel, appelez la fonction [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .</span><span class="sxs-lookup"><span data-stu-id="94469-106">To obtain the current installation state, call the [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function.</span></span>
-   <span data-ttu-id="94469-107">Pour obtenir la langue de l’installation actuelle, appelez la fonction [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) .</span><span class="sxs-lookup"><span data-stu-id="94469-107">To obtain the language for the current installation, call the [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) function.</span></span>
-   <span data-ttu-id="94469-108">Pour définir une propriété, appelez la fonction [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) .</span><span class="sxs-lookup"><span data-stu-id="94469-108">To set a property, call the [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) function.</span></span>
-   <span data-ttu-id="94469-109">Pour définir l’état de l’installation, appelez la fonction [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) .</span><span class="sxs-lookup"><span data-stu-id="94469-109">To set the installation state, call the [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) function.</span></span>
-   <span data-ttu-id="94469-110">Pour effacer une propriété (en lui affectant la valeur null), définissez la valeur de la propriété sur une chaîne vide : "".</span><span class="sxs-lookup"><span data-stu-id="94469-110">To clear a property (setting it to Null), set the property's value to an empty string: "".</span></span>

## <a name="related-topics"></a><span data-ttu-id="94469-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94469-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94469-112">Utilisation de propriétés</span><span class="sxs-lookup"><span data-stu-id="94469-112">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="94469-113">Définition des valeurs de propriété publiques sur la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="94469-113">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="94469-114">Suppression d’une propriété du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="94469-114">Clearing an Installer Property</span></span>](clearing-an-installer-property.md)
</dt> </dl>

 

 



