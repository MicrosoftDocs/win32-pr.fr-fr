---
title: Interfaces doubles (COM)
description: Interfaces doubles
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031968"
---
# <a name="dual-interfaces"></a><span data-ttu-id="d2b62-103">Interfaces doubles</span><span class="sxs-lookup"><span data-stu-id="d2b62-103">Dual Interfaces</span></span>

<span data-ttu-id="d2b62-104">OLE Automation permet à un objet d’exposer un ensemble de méthodes de deux façons : via l’interface **IDispatch** et via une liaison directe OLE vtable.</span><span class="sxs-lookup"><span data-stu-id="d2b62-104">OLE Automation enables an object to expose a set of methods in two ways: via the **IDispatch** interface, and through direct OLE VTable binding.</span></span> <span data-ttu-id="d2b62-105">**IDispatch** est utilisé par la plupart des outils disponibles aujourd’hui et prend en charge la liaison tardive à des propriétés et des méthodes.</span><span class="sxs-lookup"><span data-stu-id="d2b62-105">**IDispatch** is used by most tools available today, and offers support for late binding to properties and methods.</span></span>

<span data-ttu-id="d2b62-106">La liaison VTable offre des performances nettement supérieures, car cette méthode est appelée directement plutôt que par le biais de **IDispatch :: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="d2b62-106">VTable binding offers much higher performance because this method is called directly instead of through **IDispatch::Invoke**.</span></span> <span data-ttu-id="d2b62-107">**IDispatch** offre une prise en charge à liaison tardive, où la liaison vtable directe offre un gain de performances significatif ; les deux techniques sont utiles et importantes dans différents scénarios.</span><span class="sxs-lookup"><span data-stu-id="d2b62-107">**IDispatch** offers late bound support, where direct VTable binding offers a significant performance gain; both techniques are valuable and important in different scenarios.</span></span> <span data-ttu-id="d2b62-108">En attribuant une étiquette à une interface \[ [**double**](/windows/desktop/Midl/dual) \] dans la bibliothèque de types, une interface OLE Automation peut être utilisée via **IDispatch**, ou elle peut être liée directement à.</span><span class="sxs-lookup"><span data-stu-id="d2b62-108">By labeling an interface as \[[**dual**](/windows/desktop/Midl/dual)\] in the type library, an OLE Automation interface can be used either via **IDispatch**, or it can be bound to directly.</span></span> <span data-ttu-id="d2b62-109">Les conteneurs peuvent donc choisir la technique la plus appropriée.</span><span class="sxs-lookup"><span data-stu-id="d2b62-109">Containers can thus choose the most appropriate technique.</span></span> <span data-ttu-id="d2b62-110">La prise en charge des interfaces doubles est fortement recommandée pour les contrôles et les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="d2b62-110">Support for dual interfaces is strongly recommended for both controls and containers.</span></span>

 

 