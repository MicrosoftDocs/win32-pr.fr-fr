---
description: Une application de gestion utilisant le fournisseur de Registre système peut définir des classes avec des propriétés qui représentent des données de Registre pour des clés particulières, puis stocke les classes dans le référentiel WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Définition des classes pour le fournisseur de Registre système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952550"
---
# <a name="defining-classes-for-the-system-registry-provider"></a><span data-ttu-id="842a2-103">Définition des classes pour le fournisseur de Registre système</span><span class="sxs-lookup"><span data-stu-id="842a2-103">Defining Classes for the System Registry Provider</span></span>

<span data-ttu-id="842a2-104">Une application de gestion utilisant le fournisseur de Registre système peut définir des classes avec des propriétés qui représentent des données de Registre pour des clés particulières, puis stocke les classes dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="842a2-104">A management application using the System Registry provider can define classes with properties that represent registry data for particular keys and then stores the classes in the WMI repository.</span></span> <span data-ttu-id="842a2-105">La plupart des processus de définition d’une classe pour le registre système sont identiques à la définition d’une autre classe.</span><span class="sxs-lookup"><span data-stu-id="842a2-105">Most of the processes for defining a class for the system registry is identical to defining any other class.</span></span> <span data-ttu-id="842a2-106">Toutefois, le fournisseur de Registre système nécessite que vous utilisiez des qualificateurs et des types de données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="842a2-106">However, the System Registry provider requires that you use specific data types and qualifiers.</span></span>

<span data-ttu-id="842a2-107">La procédure suivante décrit comment définir une classe pour le fournisseur de Registre système.</span><span class="sxs-lookup"><span data-stu-id="842a2-107">The following procedure describes how to define a class for the System Registry provider.</span></span>

<span data-ttu-id="842a2-108">**Pour définir une classe pour le fournisseur de Registre système**</span><span class="sxs-lookup"><span data-stu-id="842a2-108">**To define a class for the System Registry provider**</span></span>

1.  <span data-ttu-id="842a2-109">Créez la classe comme vous le feriez pour toute autre classe.</span><span class="sxs-lookup"><span data-stu-id="842a2-109">Create the class as you would any other class.</span></span>

    <span data-ttu-id="842a2-110">Pour plus d’informations, consultez [création d’une classe](creating-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="842a2-110">For more information, see [Creating a Class](creating-a-class.md).</span></span>

2.  <span data-ttu-id="842a2-111">Mappez les types de données de registre appropriés aux types WMI appropriés.</span><span class="sxs-lookup"><span data-stu-id="842a2-111">Map the appropriate registry data types to the appropriate WMI types.</span></span>

    <span data-ttu-id="842a2-112">Le fournisseur de Registre système mappe les types de données de Registre à des types de données WMI spécifiques.</span><span class="sxs-lookup"><span data-stu-id="842a2-112">The System Registry provider maps the registry data types to specific WMI data types.</span></span> <span data-ttu-id="842a2-113">Pour plus d’informations, consultez [mappage d’un type de données de Registre à un type de données WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="842a2-113">For more information, see [Mapping a Registry Data Type to a WMI Data Type](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span></span>

3.  <span data-ttu-id="842a2-114">Utilisez les qualificateurs requis pour définir l’emplacement du fournisseur du Registre et l’emplacement de la clé de registre appropriée.</span><span class="sxs-lookup"><span data-stu-id="842a2-114">Use the required qualifiers to define the location of the Registry provider and the location of the appropriate registry key.</span></span>

    <span data-ttu-id="842a2-115">Le fournisseur de Registre système utilise trois qualificateurs pour définir l’emplacement de diverses classes, fournisseurs et entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="842a2-115">The System Registry provider uses three qualifiers to define the location of various classes, providers, and registry entries.</span></span> <span data-ttu-id="842a2-116">Pour plus d’informations, consultez [définition d’une classe de Registre avec des qualificateurs](defining-a-registry-class-with-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="842a2-116">For more information, see [Defining a Registry Class With Qualifiers](defining-a-registry-class-with-qualifiers.md).</span></span>

 

 



