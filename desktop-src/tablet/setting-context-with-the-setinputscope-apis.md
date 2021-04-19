---
description: La technique de programmation recommandée pour définir des contextes dans une application qui n’est pas compatible avec l’encre consiste à utiliser les fonctions SetInputScope pour associer le contexte aux champs de l’application.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Définition du contexte avec les API SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544933"
---
# <a name="setting-context-with-the-setinputscope-apis"></a><span data-ttu-id="e8426-103">Définition du contexte avec les API SetInputScope</span><span class="sxs-lookup"><span data-stu-id="e8426-103">Setting Context with the SetInputScope APIs</span></span>

<span data-ttu-id="e8426-104">La technique de programmation recommandée pour définir des contextes dans une application qui n’est pas compatible avec l’encre consiste à utiliser les fonctions [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) pour associer le contexte aux champs de l’application.</span><span class="sxs-lookup"><span data-stu-id="e8426-104">The recommended programmatic technique for setting contexts in an application that is not ink enabled is to use the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions to associate context with the fields in the application.</span></span>

<span data-ttu-id="e8426-105">Le kit de développement Microsoft Windows XP Tablet PC Edition 1,7 était la première version de Microsoft Windows à offrir [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span><span class="sxs-lookup"><span data-stu-id="e8426-105">The Microsoft Windows XP Tablet PC Edition Development Kit 1.7 was the first version of Microsoft Windows to offer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span> <span data-ttu-id="e8426-106">Windows Vista prend également en charge ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="e8426-106">Windows Vista also provides support for these functions.</span></span> <span data-ttu-id="e8426-107">Les définitions **SetInputScope** sont déclarées dans InputScope. idl et InputScope. h.</span><span class="sxs-lookup"><span data-stu-id="e8426-107">The **SetInputScope** definitions are declared in InputScope.idl and InputScope.h.</span></span> <span data-ttu-id="e8426-108">Pour plus d’informations, consultez [Text Services Framework](../tsf/text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="e8426-108">For more details, see [Text Services Framework](../tsf/text-services-framework.md).</span></span>

<span data-ttu-id="e8426-109">Les fonctions [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) sont la méthode recommandée pour définir le contexte pour les contrôles et les applications qui ne sont pas activés par l’encre.</span><span class="sxs-lookup"><span data-stu-id="e8426-109">The [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions are the recommended way to set context for controls and applications that are not ink enabled.</span></span>

## <a name="common-input-scopes"></a><span data-ttu-id="e8426-110">Étendues d’entrée courantes</span><span class="sxs-lookup"><span data-stu-id="e8426-110">Common Input Scopes</span></span>

<span data-ttu-id="e8426-111">À l’aide des fonctions [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) et du jeu défini d’étendues d’entrée communes décrites dans l’énumération [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , vous pouvez améliorer la précision de la reconnaissance des reconnaissance de l’écriture manuscrite Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e8426-111">Using the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions and the defined set of common input scopes described in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration, you can improve the recognition accuracy of the Microsoft handwriting recognizers.</span></span>

> [!Note]  
> <span data-ttu-id="e8426-112">Les programmes de reconnaissance pour l’anglais (États-Unis), l’anglais (Royaume-Uni), l’allemand, le français, l’italien, l’espagnol, le néerlandais et le portugais prennent actuellement en charge l’utilisation des étendues d’entrée courantes avec [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span><span class="sxs-lookup"><span data-stu-id="e8426-112">The recognizers for English (United States), English (United Kingdom), German, French, Italian, Spanish, Dutch, and Portuguese currently support using the common input scopes with [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span>

 

 

 
