---
description: Cette section décrit les interfaces IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Interfaces du gestionnaire de méthode d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517109"
---
# <a name="input-method-manager-interfaces"></a><span data-ttu-id="911bf-103">Interfaces du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="911bf-103">Input Method Manager Interfaces</span></span>

<span data-ttu-id="911bf-104">Cette section décrit les interfaces IMM.</span><span class="sxs-lookup"><span data-stu-id="911bf-104">This section describes the IMM interfaces.</span></span>



| <span data-ttu-id="911bf-105">Interface</span><span class="sxs-lookup"><span data-stu-id="911bf-105">Interface</span></span>                                                            | <span data-ttu-id="911bf-106">Description</span><span class="sxs-lookup"><span data-stu-id="911bf-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="911bf-107">**IFECommon**</span><span class="sxs-lookup"><span data-stu-id="911bf-107">**IFECommon**</span></span>](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | <span data-ttu-id="911bf-108">Fournit des services liés à l’IME qui sont communs aux différents langages.</span><span class="sxs-lookup"><span data-stu-id="911bf-108">Provides IME-related services that are common for different languages.</span></span>                                                                         |
| [<span data-ttu-id="911bf-109">**IFEDictionary**</span><span class="sxs-lookup"><span data-stu-id="911bf-109">**IFEDictionary**</span></span>](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | <span data-ttu-id="911bf-110">Permet aux clients d’accéder à un dictionnaire utilisateur Microsoft IME.</span><span class="sxs-lookup"><span data-stu-id="911bf-110">Allows clients to access a Microsoft IME user dictionary.</span></span>                                                                                      |
| [<span data-ttu-id="911bf-111">**IFELanguage**</span><span class="sxs-lookup"><span data-stu-id="911bf-111">**IFELanguage**</span></span>](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | <span data-ttu-id="911bf-112">Fournit des services de traitement de langage à l’aide de l’éditeur IME Microsoft.</span><span class="sxs-lookup"><span data-stu-id="911bf-112">Provides language processing services using the Microsoft IME.</span></span>                                                                                 |
| [<span data-ttu-id="911bf-113">**IImePad**</span><span class="sxs-lookup"><span data-stu-id="911bf-113">**IImePad**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | <span data-ttu-id="911bf-114">Insère du texte dans des applications à partir de IMEPadApplets qui implémentent l’interface [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .</span><span class="sxs-lookup"><span data-stu-id="911bf-114">Inserts text into apps from IMEPadApplets that implement the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span>                                 |
| [<span data-ttu-id="911bf-115">**IImePadApplet**</span><span class="sxs-lookup"><span data-stu-id="911bf-115">**IImePadApplet**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | <span data-ttu-id="911bf-116">Saisit des chaînes dans les applications via l’interface [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) .</span><span class="sxs-lookup"><span data-stu-id="911bf-116">Inputs strings into apps through the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface.</span></span>                                                                     |
| [<span data-ttu-id="911bf-117">**IImePlugInDictDictionaryList**</span><span class="sxs-lookup"><span data-stu-id="911bf-117">**IImePlugInDictDictionaryList**</span></span>](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | <span data-ttu-id="911bf-118">Permet d’accéder à la liste des dictionnaires de plug-in IME.</span><span class="sxs-lookup"><span data-stu-id="911bf-118">Provides access to the list of IME plug-in dictionaries.</span></span>                                                                                       |
| [<span data-ttu-id="911bf-119">**IImeSpecifyApplets**</span><span class="sxs-lookup"><span data-stu-id="911bf-119">**IImeSpecifyApplets**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | <span data-ttu-id="911bf-120">Spécifie les méthodes appelées à partir de l’objet d’interface [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) pour émuler l’interface [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .</span><span class="sxs-lookup"><span data-stu-id="911bf-120">Specifies methods called from the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface object to emulate the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span> |



 

 

 



