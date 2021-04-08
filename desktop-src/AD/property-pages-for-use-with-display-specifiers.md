---
title: Pages de propriétés à utiliser avec les spécificateurs d’affichage
description: Active Directory Domain Services fournir un mécanisme pour ajouter des pages à la feuille de propriétés affichée pour un objet d’annuaire à partir des composants logiciels enfichables d’administration de Active Directory ou de l’interpréteur de commandes Windows.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- spécificateurs d’affichage AD, pages de propriétés à utiliser avec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842046"
---
# <a name="property-pages-for-use-with-display-specifiers"></a><span data-ttu-id="63a1e-104">Pages de propriétés à utiliser avec les spécificateurs d’affichage</span><span class="sxs-lookup"><span data-stu-id="63a1e-104">Property Pages for Use with Display Specifiers</span></span>

<span data-ttu-id="63a1e-105">Active Directory Domain Services fournir un mécanisme pour ajouter des pages à la feuille de propriétés affichée pour un objet d’annuaire à partir des composants logiciels enfichables d’administration de Active Directory ou de l’interpréteur de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="63a1e-105">Active Directory Domain Services provide a mechanism for adding pages to the property sheet displayed for a directory object from the Active Directory administrative snap-ins or the Windows shell.</span></span> <span data-ttu-id="63a1e-106">Pour ajouter une page à la feuille de propriétés, implémentez une extension de feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="63a1e-106">To add a page to the property sheet, implement a property sheet extension.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="63a1e-107">Public de développeurs</span><span class="sxs-lookup"><span data-stu-id="63a1e-107">Developer Audience</span></span>

<span data-ttu-id="63a1e-108">Cette documentation suppose que le lecteur est familiarisé avec l’opération COM et le développement de composants à l’aide de C++.</span><span class="sxs-lookup"><span data-stu-id="63a1e-108">This documentation assumes that the reader is familiar with COM operation and component development using C++.</span></span> <span data-ttu-id="63a1e-109">Il n’est actuellement pas possible de créer une extension de feuille de propriétés Active Directory à l’aide de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="63a1e-109">It is not currently possible to create an Active Directory property sheet extension using Visual Basic.</span></span>

## <a name="creating-an-active-directory-property-sheet-extension"></a><span data-ttu-id="63a1e-110">Création d’une extension de feuille de propriétés Active Directory</span><span class="sxs-lookup"><span data-stu-id="63a1e-110">Creating an Active Directory Property Sheet Extension</span></span>

<span data-ttu-id="63a1e-111">Une *extension de feuille de propriétés* est un serveur com in-proc qui implémente certaines interfaces et est inscrit avec Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="63a1e-111">A *property sheet extension* is a COM in-proc server that implements certain interfaces and is registered with Active Directory Domain Services.</span></span> <span data-ttu-id="63a1e-112">Pour créer une extension de feuille de propriétés, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="63a1e-112">To create a property sheet extension, perform the following steps.</span></span>

<span data-ttu-id="63a1e-113">**Pour créer une extension de feuille de propriétés Active Directory**</span><span class="sxs-lookup"><span data-stu-id="63a1e-113">**To create an Active Directory property sheet extension**</span></span>

1.  <span data-ttu-id="63a1e-114">Créez la DLL d’extension de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="63a1e-114">Create the property sheet extension DLL.</span></span> <span data-ttu-id="63a1e-115">Une extension de feuille de propriétés est un serveur COM in-proc qui, au minimum, implémente les interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) et [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) .</span><span class="sxs-lookup"><span data-stu-id="63a1e-115">A property sheet extension is a COM in-proc server that, at a minimum, implements the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) and [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interfaces.</span></span> <span data-ttu-id="63a1e-116">Pour plus d’informations, consultez [implémentation de l’objet com de la page de propriétés](implementing-the-property-page-com-object.md).</span><span class="sxs-lookup"><span data-stu-id="63a1e-116">For more information, see [Implementing the Property Page COM Object](implementing-the-property-page-com-object.md).</span></span>
2.  <span data-ttu-id="63a1e-117">Installez l’extension de la feuille de propriétés sur les ordinateurs où l’extension de la feuille de propriétés doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="63a1e-117">Install the property sheet extension on the computers where the property sheet extension is to be used.</span></span> <span data-ttu-id="63a1e-118">Pour ce faire, créez un package Microsoft Windows Installer pour la DLL d’extension de feuille de propriétés et déployez le package de manière appropriée à l’aide de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="63a1e-118">To do this, create a Microsoft Windows Installer package for the property sheet extension DLL and deploy the package appropriately using the group policy.</span></span> <span data-ttu-id="63a1e-119">Pour plus d’informations, consultez distribution des composants de l' [interface utilisateur](distributing-user-interface-components.md).</span><span class="sxs-lookup"><span data-stu-id="63a1e-119">For more information, see [Distributing User Interface Components](distributing-user-interface-components.md).</span></span>
3.  <span data-ttu-id="63a1e-120">Enregistrez l’extension de la feuille de propriétés dans le Registre Windows et avec Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="63a1e-120">Register the property sheet extension in the Windows registry and with Active Directory Domain Services.</span></span> <span data-ttu-id="63a1e-121">Pour plus d’informations, consultez [inscription de l’objet com de la page de propriétés dans un spécificateur d’affichage](registering-the-property-page-com-object-in-a-display-specifier.md).</span><span class="sxs-lookup"><span data-stu-id="63a1e-121">For more information, see [Registering the Property Page COM Object in a Display Specifier](registering-the-property-page-com-object-in-a-display-specifier.md).</span></span>

 

 