---
title: Modifications du modèle en mode IME
description: Modèle mode IME remplacé par utilisateur par thread
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781c322949f17d4d3313b6a9b7b5eff9b1e83b06
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316157"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="de01f-103">Modèle mode IME remplacé par utilisateur par thread</span><span class="sxs-lookup"><span data-stu-id="de01f-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="de01f-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="de01f-104">Platforms</span></span>

<dl> <span data-ttu-id="de01f-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="de01f-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="de01f-106">Serveurs-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="de01f-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="de01f-107">Description</span><span class="sxs-lookup"><span data-stu-id="de01f-107">Description</span></span>

<span data-ttu-id="de01f-108">Dans Windows 8, le mode de conversion IME et le mode phrase IME étaient basés sur le contexte de l’utilisateur, et la modification du mode d’une application a affecté toutes les autres applications.</span><span class="sxs-lookup"><span data-stu-id="de01f-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="de01f-109">Ce comportement peut être désactivé à l’aide de la paramètre « laissez-moi définir une méthode d’entrée différente pour chaque fenêtre d’application » dans la section Paramètres avancés du panneau de configuration de langue.</span><span class="sxs-lookup"><span data-stu-id="de01f-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="de01f-110">Pour améliorer la compatibilité, dans Windows 8.1 les modes sont stockés dans un contexte d’entrée, quelle que soit la façon dont le contrôle « me laisser définir une méthode d’entrée différente pour chaque fenêtre d’application » est défini.</span><span class="sxs-lookup"><span data-stu-id="de01f-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="de01f-111">Dans Windows 8.1, le paramètre « laissez-moi définir une méthode d’entrée différente pour chaque fenêtre d’application » affecte uniquement la sélection de la méthode d’entrée proprement dite.</span><span class="sxs-lookup"><span data-stu-id="de01f-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="de01f-112">Au démarrage de l’application, le mode IME est défini sur les valeurs par défaut suivantes :</span><span class="sxs-lookup"><span data-stu-id="de01f-112">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="de01f-113">Panneau de saisie du logiciel</span><span class="sxs-lookup"><span data-stu-id="de01f-113">Software input panel</span></span> | <span data-ttu-id="de01f-114">Clavier matériel</span><span class="sxs-lookup"><span data-stu-id="de01f-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="de01f-115">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="de01f-115">KOR, JPN</span></span> | <span data-ttu-id="de01f-116">Il en va</span><span class="sxs-lookup"><span data-stu-id="de01f-116">On</span></span>                   | <span data-ttu-id="de01f-117">Désactivé</span><span class="sxs-lookup"><span data-stu-id="de01f-117">Off</span></span>               |
| <span data-ttu-id="de01f-118">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="de01f-118">CHS,CHT</span></span>  | <span data-ttu-id="de01f-119">Il en va</span><span class="sxs-lookup"><span data-stu-id="de01f-119">On</span></span>                   | <span data-ttu-id="de01f-120">Il en va</span><span class="sxs-lookup"><span data-stu-id="de01f-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="de01f-121">Manifestations</span><span class="sxs-lookup"><span data-stu-id="de01f-121">Manifestations</span></span>

<span data-ttu-id="de01f-122">Quand un utilisateur modifie le mode IME sur une application, la modification n’affecte pas les autres applications.</span><span class="sxs-lookup"><span data-stu-id="de01f-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="de01f-123">Ressources</span><span class="sxs-lookup"><span data-stu-id="de01f-123">Resources</span></span>

-   [<span data-ttu-id="de01f-124">Valeurs du mode de conversion IME</span><span class="sxs-lookup"><span data-stu-id="de01f-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="de01f-125">Valeurs du mode de phrase IME</span><span class="sxs-lookup"><span data-stu-id="de01f-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 