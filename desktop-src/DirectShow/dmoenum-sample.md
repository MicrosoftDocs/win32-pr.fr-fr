---
description: Exemple DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Exemple DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200819"
---
# <a name="dmoenum-sample"></a><span data-ttu-id="e659b-103">Exemple DMOEnum</span><span class="sxs-lookup"><span data-stu-id="e659b-103">DMOEnum Sample</span></span>

## <a name="description"></a><span data-ttu-id="e659b-104">Description</span><span class="sxs-lookup"><span data-stu-id="e659b-104">Description</span></span>

<span data-ttu-id="e659b-105">Cet exemple d’application énumère tous les objets DMOs ( [DirectX Media Objects](directx-media-objects.md) ) inscrits dans le système de l’utilisateur et affiche des informations à leur sujet.</span><span class="sxs-lookup"><span data-stu-id="e659b-105">This sample application enumerates all of the [DirectX Media Objects](directx-media-objects.md) (DMOs) registered in the user's system, and displays information about them.</span></span>

<span data-ttu-id="e659b-106">L’exemple utilise la fonction [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) et l’interface [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) pour énumérer le DMOs.</span><span class="sxs-lookup"><span data-stu-id="e659b-106">The sample uses the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function and the [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) interface to enumerate the DMOs.</span></span> <span data-ttu-id="e659b-107">Elle utilise l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) et d’autres interfaces DMO pour récupérer des informations sur chaque DMO.</span><span class="sxs-lookup"><span data-stu-id="e659b-107">It uses the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface and other DMO interfaces to retrieve information about each DMO.</span></span>

## <a name="usage"></a><span data-ttu-id="e659b-108">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e659b-108">Usage</span></span>

<span data-ttu-id="e659b-109">Lorsque l’application démarre, elle énumère tous les DMOs installés.</span><span class="sxs-lookup"><span data-stu-id="e659b-109">When the application launches, it enumerates all of the installed DMOs.</span></span> <span data-ttu-id="e659b-110">Si vous sélectionnez une catégorie DMO spécifique, l’application affiche uniquement les DMOs dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="e659b-110">If you select a specific DMO category, the application displays only the DMOs in that category.</span></span> <span data-ttu-id="e659b-111">Pour afficher des informations sur un DMO, sélectionnez DMO dans la liste.</span><span class="sxs-lookup"><span data-stu-id="e659b-111">To view information about a DMO, select the DMO from the list.</span></span> <span data-ttu-id="e659b-112">L’application affiche le nombre de flux, les types de médias préférés, le serveur DLL pour cette solution DMO et d’autres informations sur la solution DMO.</span><span class="sxs-lookup"><span data-stu-id="e659b-112">The application displays the number of streams, the preferred media types, the DLL server for that DMO, and other information about the DMO.</span></span> <span data-ttu-id="e659b-113">Pour inclure ou exclure des DMOs à clé, activez la case à cocher **inclure les DMOs de clé** .</span><span class="sxs-lookup"><span data-stu-id="e659b-113">To include or exclude keyed DMOs, toggle the **Include Keyed DMOs?** checkbox.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="e659b-114">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e659b-114">Downloading the Sample</span></span>

<span data-ttu-id="e659b-115">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e659b-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="e659b-116">Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ \\ \\ DirectShow \\ divers \\ DMOEnum.</span><span class="sxs-lookup"><span data-stu-id="e659b-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Misc\\DMOEnum.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e659b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e659b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e659b-118">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="e659b-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



