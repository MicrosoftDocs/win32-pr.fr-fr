---
title: Personnalisation du plug-in d’interface utilisateur
description: Personnalisation du plug-in d’interface utilisateur
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Plug-ins du lecteur Windows Media, personnalisation
- plug-ins, personnalisation
- plug-ins d’interface utilisateur, personnalisation
- Plug-ins d’interface utilisateur, personnalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029619"
---
# <a name="customizing-the-ui-plug-in"></a><span data-ttu-id="feafa-107">Personnalisation du plug-in d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="feafa-107">Customizing the UI Plug-in</span></span>

<span data-ttu-id="feafa-108">À ce stade, votre projet est prêt pour la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="feafa-108">At this point, your project is ready for customization.</span></span> <span data-ttu-id="feafa-109">Vous pouvez modifier l’implémentation générée par l’Assistant de l’interface **IWMPPluginUI** , vous pouvez ajouter une interface utilisateur à la classe **CPluginWindow** , et vous pouvez implémenter une page de propriétés dans la classe **CPropertyDialog** .</span><span class="sxs-lookup"><span data-stu-id="feafa-109">You can modify the wizard-generated implementation of the **IWMPPluginUI** interface, you can add a user interface to the **CPluginWindow** class, and you can implement a property page in the **CPropertyDialog** class.</span></span> <span data-ttu-id="feafa-110">Si votre plug-in est configuré pour écouter les événements du lecteur Windows Media, l’Assistant aura généré des implémentations par défaut ou vides de tous les gestionnaires d’événements nécessaires, que vous pouvez également modifier ou créer.</span><span class="sxs-lookup"><span data-stu-id="feafa-110">If your plug-in is configured to listen to Windows Media Player events, the wizard will have generated default or empty implementations of all the necessary event handlers, which you also modify or create.</span></span>

<span data-ttu-id="feafa-111">Le type de plug-in et les fonctionnalités qu’il prend en charge sont indiqués par une valeur stockée dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="feafa-111">The type of plug-in and the features it supports are indicated by a value which is stored in the Windows registry.</span></span> <span data-ttu-id="feafa-112">L’Assistant génère un fichier avec une extension de nom de fichier. RGS qui contient les informations pour inscrire le plug-in.</span><span class="sxs-lookup"><span data-stu-id="feafa-112">The wizard generates a file with a .rgs file name extension that contains the information to register the plug-in with.</span></span> <span data-ttu-id="feafa-113">La valeur « Capabilities » dans ce fichier est l’équivalent décimal d’un booléen ou des constantes de type de plug-in et des indicateurs de plug-in définis dans wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="feafa-113">The "Capabilities" value in this file is the decimal equivalent of a Boolean OR of the plug-in type constants and plug-in flags defined in wmpplug.h.</span></span> <span data-ttu-id="feafa-114">Bien que cette valeur soit déterminée par les options que vous sélectionnez dans l’Assistant, vous devez la modifier si vous souhaitez créer un plug-in avec plusieurs présélections ou l’un des éléments multimédias ou des sélections que vous pouvez envoyer.</span><span class="sxs-lookup"><span data-stu-id="feafa-114">Although this value is determined by the options you select in the wizard, you must modify it if you want to create a plug-in with multiple presets or one that media items or playlists can be sent to.</span></span>

<span data-ttu-id="feafa-115">À mesure que vous modifiez et étendez votre code de plug-in, vous pouvez créer et inscrire votre DLL afin de pouvoir tester votre plug-in dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="feafa-115">As you modify and extend your plug-in code, you can build and register your DLL so that you can test your plug-in in Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="feafa-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="feafa-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feafa-117">**Génération d’un plug-in d’interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="feafa-117">**Building a UI Plug-in**</span></span>](building-a-ui-plug-in.md)
</dt> </dl>

 

 




