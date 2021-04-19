---
title: Gestion du clavier dans les contrôles
description: Gestion du clavier dans les contrôles
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106538790"
---
# <a name="keyboard-handling-in-controls"></a><span data-ttu-id="7c411-103">Gestion du clavier dans les contrôles</span><span class="sxs-lookup"><span data-stu-id="7c411-103">Keyboard Handling in Controls</span></span>

<span data-ttu-id="7c411-104">La prise en charge de la gestion du clavier pour les fonctionnalités suivantes est fortement recommandée, bien qu’elle soit reconnue qu’elle n’est pas applicable à tous les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="7c411-104">Keyboard handling support for the following functionality is strongly recommended, although it is recognized that it is not applicable to all containers.</span></span>

-   <span data-ttu-id="7c411-105">Prise en charge des \_ bits d’État OLEMISC ACTSLIKELABEL et OLEMISC \_ ACTSLIKEBUTTON.</span><span class="sxs-lookup"><span data-stu-id="7c411-105">Support for OLEMISC\_ACTSLIKELABEL and OLEMISC\_ACTSLIKEBUTTON status bits.</span></span>
-   <span data-ttu-id="7c411-106">L’implémentation de la propriété ambiante DisplayAsDefault (si elle existe, elle peut retourner **false**).</span><span class="sxs-lookup"><span data-stu-id="7c411-106">Implementing the DisplayAsDefault ambient property (if it exists, it can return **FALSE**).</span></span>
-   <span data-ttu-id="7c411-107">Implémentation de la gestion des onglets, y compris l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="7c411-107">Implementing tab handling, including tab order.</span></span>

<span data-ttu-id="7c411-108">Certains conteneurs utilisent des contrôles ActiveX dans les scénarios de documents composés traditionnels.</span><span class="sxs-lookup"><span data-stu-id="7c411-108">Some containers will use ActiveX controls in traditional compound document scenarios.</span></span> <span data-ttu-id="7c411-109">Par exemple, une feuille de calcul peut permettre à un utilisateur d’incorporer un contrôle ActiveX dans une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="7c411-109">For example, a spreadsheet may allow a user to embed an ActiveX control into a worksheet.</span></span> <span data-ttu-id="7c411-110">Dans de tels scénarios, le conteneur effectue une gestion différente du clavier, car l’interface clavier doit rester cohérente avec les attentes de l’utilisateur d’une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="7c411-110">In such scenarios, the container would do keyboard handling differently, because the keyboard interface should remain consistent with the user's expectations of a spreadsheet.</span></span> <span data-ttu-id="7c411-111">La documentation de ces produits doit informer les utilisateurs des différences de gestion des contrôles dans ces différents scénarios.</span><span class="sxs-lookup"><span data-stu-id="7c411-111">Documentation for such products should inform users of differences in control handling in these different scenarios.</span></span> <span data-ttu-id="7c411-112">D’autres conteneurs doivent s’efforcer d’honorer correctement les fonctionnalités ci-dessus, y compris la gestion des mnémoniques.</span><span class="sxs-lookup"><span data-stu-id="7c411-112">Other containers should endeavor to honor the above functionality correctly, including Mnemonic handling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c411-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c411-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c411-114">Containers</span><span class="sxs-lookup"><span data-stu-id="7c411-114">Containers</span></span>](containers.md)
</dt> </dl>

 

 




