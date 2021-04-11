---
description: Pour installer un fichier, une police ou une clé de Registre afin qu’il ne soit pas supprimé lors de la désinstallation du produit, la totalité du composant contenant le fichier, la police ou la clé de registre doit être rendue permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Installation des composants permanents, des fichiers, des polices, des clés de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042822"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a><span data-ttu-id="e4ba9-103">Installation des composants permanents, des fichiers, des polices, des clés de Registre</span><span class="sxs-lookup"><span data-stu-id="e4ba9-103">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>

<span data-ttu-id="e4ba9-104">Pour installer un fichier, une police ou une clé de Registre afin qu’il ne soit pas supprimé lors de la désinstallation du produit, la totalité du composant contenant le fichier, la police ou la clé de registre doit être rendue permanente.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-104">To install a file, font, or registry key so that it is not removed when the product is uninstalled, the entire component containing the file, font, or registry key must be made permanent.</span></span> <span data-ttu-id="e4ba9-105">Pour rendre un composant permanent, définissez **msidbComponentAttributesPermanent** dans la colonne attributs de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e4ba9-105">To make a component permanent, set **msidbComponentAttributesPermanent** in the Attributes column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="e4ba9-106">Notez que le programme d’installation supprime une clé de registre après avoir supprimé la dernière valeur ou sous-clé sous la clé.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-106">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="e4ba9-107">Pour éviter qu’une clé de Registre vide ne soit supprimée lors de la désinstallation, écrivez une valeur factice sous la clé que vous avez besoin de conserver, puis entrez + dans la colonne nom de la [table du Registre](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="e4ba9-107">To prevent an empty registry key from being removed on uninstall, write a dummy value under the key you need keep, and enter + in the Name column of the [Registry table](registry-table.md).</span></span>

 

 



