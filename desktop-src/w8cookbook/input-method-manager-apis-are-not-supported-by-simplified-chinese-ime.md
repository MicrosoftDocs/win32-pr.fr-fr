---
title: Les API du gestionnaire de méthode d’entrée ne sont pas prises en charge par l’éditeur IME chinois simplifié
description: Les API du gestionnaire de méthode d’entrée ne sont pas prises en charge par l’éditeur IME chinois simplifié
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101901"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a><span data-ttu-id="2d48f-103">Les API du gestionnaire de méthode d’entrée ne sont pas prises en charge par l’éditeur IME chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="2d48f-103">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>

## <a name="platforms"></a><span data-ttu-id="2d48f-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="2d48f-104">Platforms</span></span>

<dl> <span data-ttu-id="2d48f-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2d48f-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="2d48f-106">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2d48f-106">Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="2d48f-107">Description</span><span class="sxs-lookup"><span data-stu-id="2d48f-107">Description</span></span>

<span data-ttu-id="2d48f-108">Les API du gestionnaire de méthode d’entrée suivantes ne sont pas prises en charge par les éditeurs IME chinois simplifié dans Windows 8.1 :</span><span class="sxs-lookup"><span data-stu-id="2d48f-108">The following input method manager APIs are not supported by Simplified Chinese IMEs in Windows 8.1:</span></span>

-   <span data-ttu-id="2d48f-109">Interface IFECommon</span><span class="sxs-lookup"><span data-stu-id="2d48f-109">IFECommon interface</span></span>
-   <span data-ttu-id="2d48f-110">Interface IFEDictionary</span><span class="sxs-lookup"><span data-stu-id="2d48f-110">IFEDictionary interface</span></span>
-   <span data-ttu-id="2d48f-111">Interface IFELanguage</span><span class="sxs-lookup"><span data-stu-id="2d48f-111">IFELanguage interface</span></span>
-   <span data-ttu-id="2d48f-112">Interface IImePad</span><span class="sxs-lookup"><span data-stu-id="2d48f-112">IImePad interface</span></span>
-   <span data-ttu-id="2d48f-113">Interface IImePadApplet</span><span class="sxs-lookup"><span data-stu-id="2d48f-113">IImePadApplet interface</span></span>
-   <span data-ttu-id="2d48f-114">Interface IImeSpecifyApplets</span><span class="sxs-lookup"><span data-stu-id="2d48f-114">IImeSpecifyApplets interface</span></span>

## <a name="manifestations"></a><span data-ttu-id="2d48f-115">Manifestations</span><span class="sxs-lookup"><span data-stu-id="2d48f-115">Manifestations</span></span>

<span data-ttu-id="2d48f-116">Les fonctions qui utilisent ces API ne fonctionnent pas avec l’éditeur IME chinois simplifié.</span><span class="sxs-lookup"><span data-stu-id="2d48f-116">The functions that use those APIs don’t work with Simplified Chinese IME.</span></span>

## <a name="solution"></a><span data-ttu-id="2d48f-117">Solution</span><span class="sxs-lookup"><span data-stu-id="2d48f-117">Solution</span></span>

<span data-ttu-id="2d48f-118">Les applications doivent être conçues pour que les utilisateurs puissent terminer la tâche souhaitée sans utiliser l’API spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2d48f-118">Applications must be designed so that users can complete the desired task without using the specified API.</span></span>

## <a name="resources"></a><span data-ttu-id="2d48f-119">Ressources</span><span class="sxs-lookup"><span data-stu-id="2d48f-119">Resources</span></span>

-   [<span data-ttu-id="2d48f-120">Interfaces du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="2d48f-120">Input Method Manager Interfaces</span></span>](../intl/input-method-manager-interfaces.md)
-   [<span data-ttu-id="2d48f-121">IFECommon</span><span class="sxs-lookup"><span data-stu-id="2d48f-121">IFECommon</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="2d48f-122">Interface IFECommon</span><span class="sxs-lookup"><span data-stu-id="2d48f-122">IFECommon interface</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="2d48f-123">Interface IFEDictionary</span><span class="sxs-lookup"><span data-stu-id="2d48f-123">IFEDictionary interface</span></span>](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [<span data-ttu-id="2d48f-124">IFELanguage</span><span class="sxs-lookup"><span data-stu-id="2d48f-124">IFELanguage</span></span>](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [<span data-ttu-id="2d48f-125">IImePad</span><span class="sxs-lookup"><span data-stu-id="2d48f-125">IImePad</span></span>](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [<span data-ttu-id="2d48f-126">IImePadApplet</span><span class="sxs-lookup"><span data-stu-id="2d48f-126">IImePadApplet</span></span>](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [<span data-ttu-id="2d48f-127">IimePlugInDictDictionaryList</span><span class="sxs-lookup"><span data-stu-id="2d48f-127">IimePlugInDictDictionaryList</span></span>](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [<span data-ttu-id="2d48f-128">IImeSpecifyApplets</span><span class="sxs-lookup"><span data-stu-id="2d48f-128">IImeSpecifyApplets</span></span>](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 