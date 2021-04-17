---
description: L’une des nouvelles fonctionnalités intéressantes de Tablet PC est le système d’entrée de stylet.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Entrée, encre et reconnaissance du stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558270"
---
# <a name="pen-input-ink-and-recognition"></a><span data-ttu-id="5b48e-103">Entrée, encre et reconnaissance du stylet</span><span class="sxs-lookup"><span data-stu-id="5b48e-103">Pen Input, Ink, and Recognition</span></span>

<span data-ttu-id="5b48e-104">L’une des nouvelles fonctionnalités intéressantes de Tablet PC est le système d’entrée de stylet.</span><span class="sxs-lookup"><span data-stu-id="5b48e-104">One interesting new feature of Tablet PC is the pen input system.</span></span> <span data-ttu-id="5b48e-105">Tous les ordinateurs Tablet PC ont un digitaliseur sous l’écran qui accepte les entrées de stylet.</span><span class="sxs-lookup"><span data-stu-id="5b48e-105">All Tablet PC computers have a digitizer beneath the screen that accepts pen input.</span></span> <span data-ttu-id="5b48e-106">Ce nouveau mécanisme d’entrée vous oblige à réfléchir à la création d’applications spécifiquement pour Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="5b48e-106">This new input mechanism requires you to think about how to build applications specifically for Tablet PC.</span></span> <span data-ttu-id="5b48e-107">L’interface de programmation d’applications (API) Tablet PC Platform vous aide à effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="5b48e-107">The Tablet PC platform application programming interface (API) helps you do this.</span></span>

## <a name="collection-data-management-and-recognition"></a><span data-ttu-id="5b48e-108">Collection, Gestion des données et reconnaissance</span><span class="sxs-lookup"><span data-stu-id="5b48e-108">Collection, Data Management, and Recognition</span></span>

<span data-ttu-id="5b48e-109">La plateforme Tablet PC peut être divisée en trois zones distinctes :</span><span class="sxs-lookup"><span data-stu-id="5b48e-109">The Tablet PC platform can be divided into three distinct areas:</span></span>

-   <span data-ttu-id="5b48e-110">Collection d’encres (objets utilisés pour collecter l’encre du digitaliseur).</span><span class="sxs-lookup"><span data-stu-id="5b48e-110">Ink collection (objects that are used to collect ink from the digitizer).</span></span>
-   <span data-ttu-id="5b48e-111">Gestion des données d’encre (objets utilisés pour gérer l’encre collectée).</span><span class="sxs-lookup"><span data-stu-id="5b48e-111">Ink data management (objects that are used to manage the collected ink).</span></span>
-   <span data-ttu-id="5b48e-112">Reconnaissance de l’encre (objets utilisés pour convertir l’encre collectée en d’autres types de données, tels que du texte).</span><span class="sxs-lookup"><span data-stu-id="5b48e-112">Ink recognition (objects that are used to convert the collected ink into other types of data, such as text).</span></span>

<span data-ttu-id="5b48e-113">L’illustration suivante montre, à un niveau élevé, comment l’API de collection d’encres (API Pen), l’API Ink Gestion des données (API Ink) et l’API de reconnaissance d’encre (API de reconnaissance) fonctionnent ensemble dans la plateforme Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="5b48e-113">The following image shows, at a high level, how the Ink Collection API (Pen API), Ink Data Management API (Ink API), and Ink Recognition API (Recognition API) work together in the Tablet PC platform.</span></span>

![illustraton illustrant le fonctionnement conjoint des API de stylet, de l’API Ink et de la reconnaissance](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

<span data-ttu-id="5b48e-115">L’API de plateforme Tablet PC est disponible dans les API gérées, ainsi que dans une bibliothèque COM.</span><span class="sxs-lookup"><span data-stu-id="5b48e-115">The Tablet PC platform API is available in Managed APIs as well as a COM library.</span></span> <span data-ttu-id="5b48e-116">Les rubriques suivantes décrivent les objets de l’API et illustrent comment les applications utilisent ces objets :</span><span class="sxs-lookup"><span data-stu-id="5b48e-116">The following topics describe the objects in the API and illustrate how applications use these objects:</span></span>

-   [<span data-ttu-id="5b48e-117">Collection d’encres</span><span class="sxs-lookup"><span data-stu-id="5b48e-117">Ink Collection</span></span>](ink-collection.md)
-   [<span data-ttu-id="5b48e-118">Données manuscrites</span><span class="sxs-lookup"><span data-stu-id="5b48e-118">Ink Data</span></span>](ink-data.md)
-   [<span data-ttu-id="5b48e-119">Reconnaissance de l’encre</span><span class="sxs-lookup"><span data-stu-id="5b48e-119">Ink Recognition</span></span>](ink-recognition.md)
-   [<span data-ttu-id="5b48e-120">Analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="5b48e-120">Ink Analysis</span></span>](ink-analysis.md)
-   [<span data-ttu-id="5b48e-121">Reconnaissance de l’écriture manuscrite dans Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5b48e-121">Handwriting Recognition in Windows Server 2008 R2</span></span>](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



