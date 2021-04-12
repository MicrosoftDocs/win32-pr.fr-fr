---
description: Cette rubrique décrit ce que vous devez faire pour commencer à créer des programmes qui utilisent l’API de capteur.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Configuration générale requise pour le développement d’applications (API de capteur)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320034"
---
# <a name="general-requirements-for-application-development-sensor-api"></a><span data-ttu-id="d185f-103">Configuration générale requise pour le développement d’applications (API de capteur)</span><span class="sxs-lookup"><span data-stu-id="d185f-103">General Requirements for Application Development (Sensor API)</span></span>

<span data-ttu-id="d185f-104">Cette rubrique décrit ce que vous devez faire pour commencer à créer des programmes qui utilisent l’API de capteur.</span><span class="sxs-lookup"><span data-stu-id="d185f-104">This topic describes what you must do to start to create programs that use the Sensor API.</span></span>

<span data-ttu-id="d185f-105">Pour créer une application API de capteur, vous devez installer Windows 7 et le kit de développement logiciel (SDK) Windows 7 sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d185f-105">To create a Sensor API application, you must install Windows 7 and the Windows 7 Software Development Kit (SDK) on your computer.</span></span> <span data-ttu-id="d185f-106">Le tableau suivant décrit les fichiers spécifiques dont vous aurez besoin.</span><span class="sxs-lookup"><span data-stu-id="d185f-106">The following table describes the specific files that you will need.</span></span>



| <span data-ttu-id="d185f-107">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="d185f-107">File name</span></span>               | <span data-ttu-id="d185f-108">Description</span><span class="sxs-lookup"><span data-stu-id="d185f-108">Description</span></span>                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d185f-109">Sensorsapi. h</span><span class="sxs-lookup"><span data-stu-id="d185f-109">Sensorsapi.h</span></span>            | <span data-ttu-id="d185f-110">Fichier d’en-tête principal pour l’API de capteur.</span><span class="sxs-lookup"><span data-stu-id="d185f-110">The main header file for the Sensor API.</span></span> <span data-ttu-id="d185f-111">Ce fichier d’en-tête contient les définitions d’interface.</span><span class="sxs-lookup"><span data-stu-id="d185f-111">This header file contains the interface definitions.</span></span>               |
| <span data-ttu-id="d185f-112">Capteurs. h</span><span class="sxs-lookup"><span data-stu-id="d185f-112">Sensors.h</span></span>               | <span data-ttu-id="d185f-113">Fichier d’en-tête qui contient les définitions des constantes définies par la plateforme.</span><span class="sxs-lookup"><span data-stu-id="d185f-113">The header file that contains definitions of platform-defined constants.</span></span>                                    |
| <span data-ttu-id="d185f-114">Initguid. h</span><span class="sxs-lookup"><span data-stu-id="d185f-114">Initguid.h</span></span>              | <span data-ttu-id="d185f-115">Fichier d’en-tête qui contient les définitions pour le contrôle de l’initialisation du **GUID** .</span><span class="sxs-lookup"><span data-stu-id="d185f-115">The header file that contains definitions for controlling **GUID** initialization.</span></span>                          |
| <span data-ttu-id="d185f-116">FunctionDiscoveryKeys. h</span><span class="sxs-lookup"><span data-stu-id="d185f-116">FunctionDiscoveryKeys.h</span></span> | <span data-ttu-id="d185f-117">Fichier d’en-tête qui définit les clés de propriété d’ID d’appareil qui sont requises lorsque vous vous connectez aux capteurs logiques.</span><span class="sxs-lookup"><span data-stu-id="d185f-117">The header file that defines device ID property keys that are required when you connect to logical sensors.</span></span> |
| <span data-ttu-id="d185f-118">Sensorsapi. lib</span><span class="sxs-lookup"><span data-stu-id="d185f-118">Sensorsapi.lib</span></span>          | <span data-ttu-id="d185f-119">Bibliothèque statique qui contient des définitions de **GUID** pour l’API de capteur.</span><span class="sxs-lookup"><span data-stu-id="d185f-119">A static library that contains **GUID** definitions for the Sensor API.</span></span>                                     |
| <span data-ttu-id="d185f-120">PortableDeviceGuids. lib</span><span class="sxs-lookup"><span data-stu-id="d185f-120">PortableDeviceGuids.lib</span></span> | <span data-ttu-id="d185f-121">Bibliothèque statique qui contient des définitions **GUID** pour les objets périphériques mobiles Windows.</span><span class="sxs-lookup"><span data-stu-id="d185f-121">A static library that contains **GUID** definitions for Windows Portable Devices objects.</span></span>                   |



 

<span data-ttu-id="d185f-122">Votre programme peut nécessiter des fichiers supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d185f-122">Your program may require additional files.</span></span>

## <a name="supported-operating-systems"></a><span data-ttu-id="d185f-123">Systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="d185f-123">Supported Operating Systems</span></span>

<span data-ttu-id="d185f-124">Les applications API de capteur s’exécutent sur toutes les éditions de Windows 7, à l’exception de Windows 7 Édition Starter.</span><span class="sxs-lookup"><span data-stu-id="d185f-124">Sensor API applications will run on all editions of Windows 7, except for Windows 7 Starter edition.</span></span>

## <a name="windows-portable-devices-interfaces"></a><span data-ttu-id="d185f-125">Interfaces des appareils mobiles Windows</span><span class="sxs-lookup"><span data-stu-id="d185f-125">Windows Portable Devices Interfaces</span></span>

<span data-ttu-id="d185f-126">L’API de capteur utilise certains objets WPD (Windows Portable Devices) pour encapsuler les clés et les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="d185f-126">The Sensor API uses certain Windows Portable Devices (WPD) objects to encapsulate property keys and values.</span></span> <span data-ttu-id="d185f-127">Le tableau suivant décrit les interfaces de ces objets.</span><span class="sxs-lookup"><span data-stu-id="d185f-127">The following table describes the interfaces for these objects.</span></span>



| <span data-ttu-id="d185f-128">Interface</span><span class="sxs-lookup"><span data-stu-id="d185f-128">Interface</span></span>                                                                       | <span data-ttu-id="d185f-129">Description</span><span class="sxs-lookup"><span data-stu-id="d185f-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d185f-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d185f-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span></span>        | <span data-ttu-id="d185f-131">Cette interface offre un moyen pratique de créer un conteneur de propriétés de paires nom/valeur.</span><span class="sxs-lookup"><span data-stu-id="d185f-131">This interface provides a convenient way to create a property bag of name/value pairs.</span></span> <span data-ttu-id="d185f-132">Les noms sont représentés par **PROPERTYKEY** s et les valeurs sont représentées par **PROPVARIANT** s.</span><span class="sxs-lookup"><span data-stu-id="d185f-132">Names are represented by **PROPERTYKEY** s and values are represented by **PROPVARIANT** s.</span></span> <br/> <span data-ttu-id="d185f-133">L’API utilise cette interface pour définir et récupérer à la fois des valeurs uniques et des ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="d185f-133">The API uses this interface for setting and retrieving both single values and sets of values.</span></span> <span data-ttu-id="d185f-134">Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, en appelant **CoCreateInstance** avec CLSID \_ PortableDeviceValues.</span><span class="sxs-lookup"><span data-stu-id="d185f-134">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceValues.</span></span><br/> |
| <span data-ttu-id="d185f-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d185f-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span></span> | <span data-ttu-id="d185f-136">Cette interface contient une collection de **PROPERTYKEY** s.</span><span class="sxs-lookup"><span data-stu-id="d185f-136">This interface contains a collection of **PROPERTYKEY** s.</span></span> <span data-ttu-id="d185f-137">Ces clés représentent des noms de propriétés qui peuvent être stockés par **IPortableDeviceValues**.</span><span class="sxs-lookup"><span data-stu-id="d185f-137">These keys represent property names that can be stored by **IPortableDeviceValues**.</span></span> <span data-ttu-id="d185f-138">L’API utilise cet objet de collection pour définir et récupérer à la fois des noms de propriété uniques et des ensembles de noms de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d185f-138">The API uses this collection object for setting and retrieving both single property names and sets of property names.</span></span><br/> <span data-ttu-id="d185f-139">Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, en appelant **CoCreateInstance** avec CLSID \_ PortableDeviceKeyCollection.</span><span class="sxs-lookup"><span data-stu-id="d185f-139">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceKeyCollection.</span></span> <br/>    |



 

 

