---
title: Fichiers art
description: Fichiers art
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Apparences du lecteur Windows Media, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les habillages, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a246ac411a3dfe2c5bab529ddcccce5596434617
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513494"
---
# <a name="art-files"></a><span data-ttu-id="a088c-107">Fichiers art</span><span class="sxs-lookup"><span data-stu-id="a088c-107">Art Files</span></span>

<span data-ttu-id="a088c-108">Vous devez créer un ou plusieurs fichiers artistiques pour votre apparence.</span><span class="sxs-lookup"><span data-stu-id="a088c-108">You must create one or more art files for your skin.</span></span> <span data-ttu-id="a088c-109">Sans art, l’utilisateur n’aura rien à regarder.</span><span class="sxs-lookup"><span data-stu-id="a088c-109">Without art, the user will have nothing to look at.</span></span> <span data-ttu-id="a088c-110">Vous pouvez créer une apparence invisible, mais personne ne l’affichera !</span><span class="sxs-lookup"><span data-stu-id="a088c-110">You could create an invisible skin, but no one would see it!</span></span> <span data-ttu-id="a088c-111">Et même dans ce cas, vous devez toujours créer des fichiers art pour contenir vos images invisibles, car le fichier de définition d’apparence requiert des fichiers artistiques pour des éléments spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a088c-111">And even then, you would still have to create art files to hold your invisible images, because the skin definition file requires art files for specific elements.</span></span>

<span data-ttu-id="a088c-112">Il existe trois utilisations de l’art dans les habillages : images principales, images de mappage et autres images.</span><span class="sxs-lookup"><span data-stu-id="a088c-112">There are three uses for art in skins: primary images, mapping images, and alternate images.</span></span>

## <a name="primary-images"></a><span data-ttu-id="a088c-113">Images principales</span><span class="sxs-lookup"><span data-stu-id="a088c-113">Primary Images</span></span>

<span data-ttu-id="a088c-114">Vous devez créer une image principale pour votre apparence.</span><span class="sxs-lookup"><span data-stu-id="a088c-114">You must create a primary image for your skin.</span></span> <span data-ttu-id="a088c-115">C’est ce que les utilisateurs verront quand ils installeront votre apparence.</span><span class="sxs-lookup"><span data-stu-id="a088c-115">This is what the users will see when they install your skin.</span></span> <span data-ttu-id="a088c-116">L’image principale est composée d’une ou de plusieurs images créées par des contrôles d’apparence spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a088c-116">The primary image is composed of one or more images that are created by specific skin controls.</span></span>

<span data-ttu-id="a088c-117">Si vous avez plus d’un contrôle, vous devez spécifier l’ordre de plan, qui définit les contrôles qui sont affichés devant les autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="a088c-117">If you have more than one control, you must specify the z-order, which defines which controls are displayed in front of other controls.</span></span> <span data-ttu-id="a088c-118">Chaque élément d' **affichage** aura une image d’arrière-plan à laquelle vous pouvez ajouter d’autres images d’élément, ce qui vous permet de créer une image composite principale.</span><span class="sxs-lookup"><span data-stu-id="a088c-118">Each **View** element will have a background image that you can add other element images to, allowing you to create a primary composite image.</span></span>

<span data-ttu-id="a088c-119">Vous pouvez également avoir des images secondaires, telles qu’une barre d’État coulissante, qui ne s’affichent pas lorsque votre apparence s’affiche pour la première fois, mais qui s’affichent lorsque l’utilisateur effectue une action.</span><span class="sxs-lookup"><span data-stu-id="a088c-119">You also may have secondary images, such as a sliding tray, that do not display when your skin first appears, but that show up when the user takes some action.</span></span> <span data-ttu-id="a088c-120">Celles-ci suivent les mêmes règles que les images principales, car elles sont créées avec un ensemble de contrôles.</span><span class="sxs-lookup"><span data-stu-id="a088c-120">These follow the same rules as primary images, in that they are created with a set of controls.</span></span>

## <a name="mapping-images"></a><span data-ttu-id="a088c-121">Mapper des images</span><span class="sxs-lookup"><span data-stu-id="a088c-121">Mapping Images</span></span>

<span data-ttu-id="a088c-122">L’une des fonctionnalités les plus puissantes des apparences du lecteur Windows Media est que vous pouvez utiliser le mappage d’images pour déclencher des événements pour votre apparence.</span><span class="sxs-lookup"><span data-stu-id="a088c-122">One of the most powerful features of Windows Media Player skins is that you can use image mapping to trigger events for your skin.</span></span> <span data-ttu-id="a088c-123">Les images interactives sont des fichiers qui contiennent des images spéciales.</span><span class="sxs-lookup"><span data-stu-id="a088c-123">Image maps are files that contain special images.</span></span> <span data-ttu-id="a088c-124">Toutefois, les images d’un fichier image map ne sont pas censées être affichées par l’utilisateur, mais elles sont utilisées par le lecteur Windows Media pour agir quand l’utilisateur clique sur votre apparence.</span><span class="sxs-lookup"><span data-stu-id="a088c-124">The images in an image map file, however, are not meant to be viewed by the user, but are used by Windows Media Player to take action when the user clicks on your skin.</span></span>

<span data-ttu-id="a088c-125">Différents contrôles requièrent différents genres de cartes d’images.</span><span class="sxs-lookup"><span data-stu-id="a088c-125">Different controls need different kinds of image maps.</span></span> <span data-ttu-id="a088c-126">Par exemple, si vous colorez une partie d’une image mapper une valeur rouge spécifique et que l’utilisateur clique sur la zone correspondante de votre image principale, un bouton déclenche un événement.</span><span class="sxs-lookup"><span data-stu-id="a088c-126">For example, if you color part of an image map a specific red value, and the user clicks on the corresponding area of your primary image, a button will fire an event.</span></span> <span data-ttu-id="a088c-127">La couleur est utilisée pour définir les événements déclenchés par un clic dans une zone particulière de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="a088c-127">Color is used to define which events are triggered by clicking in a particular area of the skin.</span></span>

## <a name="alternate-images"></a><span data-ttu-id="a088c-128">Images de remplacement</span><span class="sxs-lookup"><span data-stu-id="a088c-128">Alternate Images</span></span>

<span data-ttu-id="a088c-129">Vous pouvez également configurer d’autres images à afficher lorsqu’un utilisateur effectue une opération.</span><span class="sxs-lookup"><span data-stu-id="a088c-129">You can also set up alternate images to display when a user does something.</span></span> <span data-ttu-id="a088c-130">Par exemple, vous pouvez créer une image de remplacement d’un bouton qui s’affichera uniquement lorsque la souris pointe sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="a088c-130">For example, you can create an alternate image of a button that will be displayed only when the mouse hovers over the button.</span></span> <span data-ttu-id="a088c-131">C’est un bon moyen de permettre aux utilisateurs de savoir ce qu’ils peuvent faire et permet également d’obtenir une interface utilisateur hautement détectable.</span><span class="sxs-lookup"><span data-stu-id="a088c-131">This is a good way to let users know what they can do, and also allows for a highly discoverable user interface.</span></span> <span data-ttu-id="a088c-132">En utilisant avec prudence les info-bulles et les images de survol, vous pouvez créer des interfaces utilisateur inhabituelles qui fournissent aux utilisateurs des commentaires sur les options disponibles.</span><span class="sxs-lookup"><span data-stu-id="a088c-132">By using ToolTips and hover images carefully, you can create unusual user interfaces that still give the user feedback about what options are available.</span></span>

<span data-ttu-id="a088c-133">Les sections suivantes fournissent plus d’informations sur les fichiers artistiques :</span><span class="sxs-lookup"><span data-stu-id="a088c-133">The following sections provide more information about art files:</span></span>

-   [<span data-ttu-id="a088c-134">Images principales</span><span class="sxs-lookup"><span data-stu-id="a088c-134">Primary Images</span></span>](primary-images.md)
-   [<span data-ttu-id="a088c-135">Mapper des images</span><span class="sxs-lookup"><span data-stu-id="a088c-135">Mapping Images</span></span>](mapping-images.md)
-   [<span data-ttu-id="a088c-136">Images de remplacement</span><span class="sxs-lookup"><span data-stu-id="a088c-136">Alternate Images</span></span>](alternate-images.md)
-   [<span data-ttu-id="a088c-137">Formats de fichier art</span><span class="sxs-lookup"><span data-stu-id="a088c-137">Art File Formats</span></span>](art-file-formats.md)
-   [<span data-ttu-id="a088c-138">Exemple d’art simple</span><span class="sxs-lookup"><span data-stu-id="a088c-138">Simple Art Example</span></span>](simple-art-example.md)

## <a name="related-topics"></a><span data-ttu-id="a088c-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a088c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a088c-140">**Fichiers d’apparence**</span><span class="sxs-lookup"><span data-stu-id="a088c-140">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




