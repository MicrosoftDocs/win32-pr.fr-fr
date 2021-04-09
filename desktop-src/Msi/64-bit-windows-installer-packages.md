---
description: Un package 64 bits se compose partiellement ou entièrement de composants Windows Installer de 64 bits.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: Packages de Windows Installer 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864541"
---
# <a name="64-bit-windows-installer-packages"></a><span data-ttu-id="14df1-103">Packages de Windows Installer 64 bits</span><span class="sxs-lookup"><span data-stu-id="14df1-103">64-bit Windows Installer Packages</span></span>

<span data-ttu-id="14df1-104">Un package 64 bits se compose partiellement ou entièrement de composants [Windows Installer](windows-installer-components.md) de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="14df1-104">A 64-bit package consists partially or entirely of 64-bit [Windows Installer](windows-installer-components.md) components.</span></span> <span data-ttu-id="14df1-105">La liste suivante répertorie les conditions requises pour chaque package Windows Installer 64 bits :</span><span class="sxs-lookup"><span data-stu-id="14df1-105">The following list identifies the requirements for every 64-bit Windows Installer package:</span></span>

-   <span data-ttu-id="14df1-106">La valeur « Intel64 » doit être entrée dans le champ plateforme de la propriété [**Résumé du modèle**](template-summary.md) si et seulement si le package s’exécute sur un processeur Intel64 (Itanium).</span><span class="sxs-lookup"><span data-stu-id="14df1-106">The value "Intel64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Intel64 (Itanium) processor.</span></span>
-   <span data-ttu-id="14df1-107">La valeur « x64 » doit être entrée dans le champ plateforme de la propriété [**Résumé du modèle**](template-summary.md) si et uniquement si le package s’exécute sur un processeur x64.</span><span class="sxs-lookup"><span data-stu-id="14df1-107">The value "x64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an x64 processor.</span></span>
-   <span data-ttu-id="14df1-108">La valeur « Arm64 » doit être entrée dans le champ Platform de la propriété [**Résumé du modèle**](template-summary.md) si et seulement si le package s’exécute sur un processeur Arm64.</span><span class="sxs-lookup"><span data-stu-id="14df1-108">The value "Arm64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Arm64 processor.</span></span>
-   <span data-ttu-id="14df1-109">La propriété de [**Résumé du nombre de pages**](page-count-summary.md) doit être définie sur l’entier 200 ou supérieur, car Windows Installer 2,0 est la version minimale qui est capable d’installer les composants 64 bits.</span><span class="sxs-lookup"><span data-stu-id="14df1-109">The [**Page Count Summary**](page-count-summary.md) property must be set to the integer 200 or greater, because Windows Installer 2.0 is the minimum version that is capable of installing 64-bit components.</span></span> <span data-ttu-id="14df1-110">Les packages pour la plateforme Arm64 nécessitent une valeur supérieure ou égale à 500.</span><span class="sxs-lookup"><span data-stu-id="14df1-110">Packages for the Arm64 platform require a value of 500 or greater.</span></span>
-   <span data-ttu-id="14df1-111">Chaque composant de Windows Installer 64 bits dans le package doit inclure le bit **msidbComponentAttributes64bit** dans la colonne attributs de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="14df1-111">Each 64-bit Windows Installer component in the package must include the **msidbComponentAttributes64bit** bit in the Attributes column of the [Component Table](component-table.md).</span></span>

<span data-ttu-id="14df1-112">Pour plus d’informations, consultez [Windows Installer sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md) et les [packages Windows Installer 32 bits](32-bit-windows-installer-packages.md).</span><span class="sxs-lookup"><span data-stu-id="14df1-112">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md) and [32-bit Windows Installer Packages](32-bit-windows-installer-packages.md).</span></span>

 

 



