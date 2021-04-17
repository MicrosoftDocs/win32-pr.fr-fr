---
description: Moniteur réseau ou votre DLL d’analyseur peut mettre en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Mise en forme des données affichées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525144"
---
# <a name="formatting-displayed-data"></a><span data-ttu-id="5c2ac-103">Mise en forme des données affichées</span><span class="sxs-lookup"><span data-stu-id="5c2ac-103">Formatting Displayed Data</span></span>

<span data-ttu-id="5c2ac-104">Moniteur réseau ou votre DLL d’analyseur peut mettre en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-104">Network Monitor or your parser DLL can format the data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="5c2ac-105">Moniteur réseau fournit un formateur générique qui fournit les services de base nécessaires pour afficher la plupart des types de données qui existent dans un protocole.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-105">Network Monitor provides a generic formatter that provides the basic services needed to display most data types that exist within a protocol.</span></span> <span data-ttu-id="5c2ac-106">Toutefois, le formateur générique ne prend pas en charge tous les types de données.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-106">However, the generic formatter does not support all data types.</span></span> <span data-ttu-id="5c2ac-107">Par exemple, le formateur générique ne prend pas en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5c2ac-107">For example, the generic formatter does not support the following:</span></span>

-   <span data-ttu-id="5c2ac-108">Plusieurs types d’adresses.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-108">Several address types.</span></span>
-   <span data-ttu-id="5c2ac-109">Noms conviviaux pour la source et la destination.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-109">Source and destination-friendly names.</span></span>
-   <span data-ttu-id="5c2ac-110">Identificateurs d’objets.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-110">Object identifiers.</span></span>
-   <span data-ttu-id="5c2ac-111">Types de données entiers volumineux.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-111">Large integer data types.</span></span>
-   <span data-ttu-id="5c2ac-112">Types de données entiers de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-112">Variable length small integer data types.</span></span>

<span data-ttu-id="5c2ac-113">L’exemple suivant identifie deux chaînes mises en forme pour la propriété ID de privilège.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-113">The following example identifies two formatted strings for the Privilege ID property.</span></span>

-   <span data-ttu-id="5c2ac-114">La première ligne de code illustre la sortie du formateur générique.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-114">The first line of code shows the output of the generic formatter.</span></span> <span data-ttu-id="5c2ac-115">La sortie est basée sur le type de données.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-115">The output is based on the data type.</span></span>
-   <span data-ttu-id="5c2ac-116">La deuxième ligne de code illustre la sortie d’un formateur personnalisé avec une chaîne de données de propriété.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-116">The second line of code shows the output of a custom formatter with a string to the property data.</span></span>

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> <span data-ttu-id="5c2ac-117">Dans la mesure du possible, utilisez le formateur générique pour afficher vos données, car il vous permet de contrôler la taille de votre DLL d’analyseur et fournit de meilleures fonctionnalités multiplateforme pour votre DLL d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="5c2ac-117">When possible, use the generic formatter to display your data because it allows you to control the size of your parser DLL, and provides better cross-platform capabilities for your parser DLL.</span></span>

 

 

 



