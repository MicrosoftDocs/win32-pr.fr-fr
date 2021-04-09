---
description: '\\Panneau de configuration HKCU \\ international.'
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: AddHijriDate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860809"
---
# <a name="addhijridate"></a><span data-ttu-id="6cb4d-103">AddHijriDate</span><span class="sxs-lookup"><span data-stu-id="6cb4d-103">AddHijriDate</span></span>

<span data-ttu-id="6cb4d-104">**\\Panneau de configuration HKCU \\ international**</span><span class="sxs-lookup"><span data-stu-id="6cb4d-104">**HKCU\\Control Panel\\International**</span></span>



| <span data-ttu-id="6cb4d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="6cb4d-105">Data type</span></span> | <span data-ttu-id="6cb4d-106">Plage</span><span class="sxs-lookup"><span data-stu-id="6cb4d-106">Range</span></span>                      | <span data-ttu-id="6cb4d-107">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="6cb4d-107">Default value</span></span> |
|-----------|----------------------------|---------------|
| <span data-ttu-id="6cb4d-108">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="6cb4d-108">REG\_SZ</span></span>   | <span data-ttu-id="6cb4d-109">*Valeur d’ajustement valide*</span><span class="sxs-lookup"><span data-stu-id="6cb4d-109">*A valid adjustment value*</span></span> | <span data-ttu-id="6cb4d-110">(aucune)</span><span class="sxs-lookup"><span data-stu-id="6cb4d-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="6cb4d-111">Description</span><span class="sxs-lookup"><span data-stu-id="6cb4d-111">Description</span></span>

<span data-ttu-id="6cb4d-112">Spécifie des ajustements à la date dans le calendrier Hijri.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-112">Specifies adjustments to the date within the Hijri calendar.</span></span>

<span data-ttu-id="6cb4d-113">Le calendrier islamique est un calendrier lunaire utilisé dans le monde islamique.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-113">The Hijri calendar is a lunar calendar used in the Islamic world.</span></span> <span data-ttu-id="6cb4d-114">Les mois commencent et se terminent en fonction d’un décret basé sur l’observation de la nouvelle lune.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-114">The months begin and end according to a decree that is based on the observation of the new moon.</span></span> <span data-ttu-id="6cb4d-115">Il est difficile de prédire avec précision les débuts et les fins des mois, et il existe des variations régionales, de sorte qu’un ajustement entre zéro et deux jours est apporté au calendrier.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-115">It is difficult to accurately predict the beginnings and endings of the months, and there are regional variations, so an adjustment of between zero and two days is made to the calendar.</span></span>

<span data-ttu-id="6cb4d-116">La valeur de Registre **AddHijriDate** stocke cette valeur d’ajustement comme suit.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-116">The **AddHijriDate** registry value stores this adjustment value as follows.</span></span>



| <span data-ttu-id="6cb4d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cb4d-117">Value</span></span>          | <span data-ttu-id="6cb4d-118">Signification</span><span class="sxs-lookup"><span data-stu-id="6cb4d-118">Meaning</span></span>                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb4d-119">AddHijriDate-2</span><span class="sxs-lookup"><span data-stu-id="6cb4d-119">AddHijriDate-2</span></span> | <span data-ttu-id="6cb4d-120">Soustraire deux jours.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-120">Subtract two days.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="6cb4d-121">AddHijriDate</span><span class="sxs-lookup"><span data-stu-id="6cb4d-121">AddHijriDate</span></span>   | <span data-ttu-id="6cb4d-122">Soustraire un jour.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-122">Subtract one day.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="6cb4d-123">(vide)</span><span class="sxs-lookup"><span data-stu-id="6cb4d-123">(blank)</span></span>        | <span data-ttu-id="6cb4d-124">Aucun ajustement n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-124">No adjustment is necessary.</span></span> <span data-ttu-id="6cb4d-125">(Si la date n’a pas été ajustée, cette entrée n’apparaît pas dans le registre.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-125">(If the date has not been adjusted, this entry does not appear in the registry.</span></span> <span data-ttu-id="6cb4d-126">Si la date a été ajustée, puis restaurée à sa valeur d’origine, cette entrée apparaît dans le registre sans valeur.)</span><span class="sxs-lookup"><span data-stu-id="6cb4d-126">If the date has been adjusted and then restored to its original value, this entry appears in the registry with no value.)</span></span> |
| <span data-ttu-id="6cb4d-127">AddHijriDate + 1</span><span class="sxs-lookup"><span data-stu-id="6cb4d-127">AddHijriDate+1</span></span> | <span data-ttu-id="6cb4d-128">Ajoutez un jour.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-128">Add one day.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="6cb4d-129">AddHijriDate + 2</span><span class="sxs-lookup"><span data-stu-id="6cb4d-129">AddHijriDate+2</span></span> | <span data-ttu-id="6cb4d-130">Ajoutez deux jours.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-130">Add two days.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="6cb4d-131">Par défaut, cette entrée n’existe pas dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-131">This entry does not exist in the registry by default.</span></span> <span data-ttu-id="6cb4d-132">Vous pouvez l’ajouter à l’aide de l’éditeur du Registre Regedit.exe ou à l’aide de la méthode de modification décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-132">You can add it by using the registry editor Regedit.exe or by using the change method described below.</span></span>

## <a name="change-method"></a><span data-ttu-id="6cb4d-133">Modifier la méthode</span><span class="sxs-lookup"><span data-stu-id="6cb4d-133">Change Method</span></span>

<span data-ttu-id="6cb4d-134">Pour modifier la valeur de cette entrée ou l’ajouter au registre, commencez par installer les fichiers pour le script complexe et les langues de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-134">To change the value of this entry, or to add it to the registry, first install the files for complex script and right-to-left languages.</span></span> <span data-ttu-id="6cb4d-135">Dans le panneau de configuration, cliquez sur **Options régionales et linguistiques**, puis cliquez sur l’onglet **langues** . Sous **prise en charge de langues supplémentaires**, activez la case à cocher pour **installer les fichiers de script complexe et les langues de droite à gauche (y compris le thaï)**.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-135">In Control Panel, click **Regional and Language Options**, then click the **Languages** tab. Under **Supplemental language support**, select the checkbox to **Install files for complex script and right-to-left languages (including Thai)**.</span></span> <span data-ttu-id="6cb4d-136">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-136">Click **OK**.</span></span>

<span data-ttu-id="6cb4d-137">Pour modifier la valeur de cette entrée, ou pour l’ajouter au registre, dans le panneau de configuration, cliquez sur **Options régionales et linguistiques**.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-137">To change the value of this entry, or to add it to the registry, from Control Panel, click **Regional and Language Options**.</span></span> <span data-ttu-id="6cb4d-138">Dans le champ **standards et formats** , sélectionnez les paramètres régionaux qui utilisent le calendrier Hijri.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-138">In the **Standards and Formats** field, select a locale that uses the Hijri calendar.</span></span> <span data-ttu-id="6cb4d-139">Cliquez sur le bouton **personnaliser** , puis sur l’onglet **Date** . Dans la liste déroulante **ajuster la date Hijri à :** , sélectionnez la valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-139">Click the **Customize** button, then click the **Date** tab. In the **Adjust Hijri date to:** drop-down list, select the appropriate value.</span></span> <span data-ttu-id="6cb4d-140">Cliquez sur **OK**, puis de nouveau sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="6cb4d-140">Click **OK**, then click **OK** again.</span></span>

## <a name="activation-method"></a><span data-ttu-id="6cb4d-141">Méthode d’activation</span><span class="sxs-lookup"><span data-stu-id="6cb4d-141">Activation Method</span></span>

<span data-ttu-id="6cb4d-142">Les modifications apportées à cette entrée par le biais du panneau de configuration prennent effet immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6cb4d-142">Changes to this entry made through Control Panel take effect immediately.</span></span>

 

 



