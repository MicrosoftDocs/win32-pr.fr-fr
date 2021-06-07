---
title: Modifications du modèle en mode IME
description: Modèle mode IME remplacé par utilisateur par thread
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443245"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="0c963-103">Modèle mode IME remplacé par utilisateur par thread</span><span class="sxs-lookup"><span data-stu-id="0c963-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="0c963-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="0c963-104">Platforms</span></span>

<dl> <span data-ttu-id="0c963-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0c963-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="0c963-106">Serveurs-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0c963-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="0c963-107">Description</span><span class="sxs-lookup"><span data-stu-id="0c963-107">Description</span></span>

<span data-ttu-id="0c963-108">Dans Windows 8, le mode de conversion IME et le mode phrase IME étaient basés sur le contexte de l’utilisateur, et la modification du mode d’une application a affecté toutes les autres applications.</span><span class="sxs-lookup"><span data-stu-id="0c963-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="0c963-109">Ce comportement peut être désactivé à l’aide de la paramètre « laissez-moi définir une méthode d’entrée différente pour chaque fenêtre d’application » dans la section Paramètres avancés du panneau de configuration de langue.</span><span class="sxs-lookup"><span data-stu-id="0c963-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="0c963-110">Pour améliorer la compatibilité, dans Windows 8.1 les modes sont stockés dans un contexte d’entrée, quelle que soit la façon dont le contrôle « me laisser définir une méthode d’entrée différente pour chaque fenêtre d’application » est défini.</span><span class="sxs-lookup"><span data-stu-id="0c963-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="0c963-111">Dans Windows 8.1, le paramètre « laissez-moi définir une méthode d’entrée différente pour chaque fenêtre d’application » affecte uniquement la sélection de la méthode d’entrée proprement dite.</span><span class="sxs-lookup"><span data-stu-id="0c963-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="0c963-112">Au démarrage de l’application, le mode IME est défini sur les valeurs par défaut suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c963-112">At application start up, the IME mode is set to the following defaults:</span></span>



| &nbsp;   | <span data-ttu-id="0c963-113">Panneau de saisie du logiciel</span><span class="sxs-lookup"><span data-stu-id="0c963-113">Software input panel</span></span> | <span data-ttu-id="0c963-114">Clavier matériel</span><span class="sxs-lookup"><span data-stu-id="0c963-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="0c963-115">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="0c963-115">KOR, JPN</span></span> | <span data-ttu-id="0c963-116">Activé</span><span class="sxs-lookup"><span data-stu-id="0c963-116">On</span></span>                   | <span data-ttu-id="0c963-117">Désactivé</span><span class="sxs-lookup"><span data-stu-id="0c963-117">Off</span></span>               |
| <span data-ttu-id="0c963-118">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="0c963-118">CHS,CHT</span></span>  | <span data-ttu-id="0c963-119">Activé</span><span class="sxs-lookup"><span data-stu-id="0c963-119">On</span></span>                   | <span data-ttu-id="0c963-120">Activé</span><span class="sxs-lookup"><span data-stu-id="0c963-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="0c963-121">Manifestations</span><span class="sxs-lookup"><span data-stu-id="0c963-121">Manifestations</span></span>

<span data-ttu-id="0c963-122">Quand un utilisateur modifie le mode IME sur une application, la modification n’affecte pas les autres applications.</span><span class="sxs-lookup"><span data-stu-id="0c963-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="0c963-123">Ressources</span><span class="sxs-lookup"><span data-stu-id="0c963-123">Resources</span></span>

-   [<span data-ttu-id="0c963-124">Valeurs du mode de conversion IME</span><span class="sxs-lookup"><span data-stu-id="0c963-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="0c963-125">Valeurs du mode de phrase IME</span><span class="sxs-lookup"><span data-stu-id="0c963-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 