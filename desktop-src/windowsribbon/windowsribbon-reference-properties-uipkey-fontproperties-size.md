---
title: UI_PKEY_FontProperties_Size
description: Identifie la \_ propriété de \_ taille FontProperties de l’interface utilisateur \_ .
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106545728"
---
# <a name="ui_pkey_fontproperties_size"></a><span data-ttu-id="f87a5-103">\_Taille de \_ FontProperties de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="f87a5-103">UI\_PKEY\_FontProperties\_Size</span></span>

<span data-ttu-id="f87a5-104">Identifie la \_ propriété de \_ taille FontProperties de l’interface utilisateur \_ .</span><span class="sxs-lookup"><span data-stu-id="f87a5-104">Identifies the UI\_PKEY\_FontProperties\_Size property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a><span data-ttu-id="f87a5-105">Notes</span><span class="sxs-lookup"><span data-stu-id="f87a5-105">Remarks</span></span>

<span data-ttu-id="f87a5-106">\_ \_ La taille FontProperties de l’interface utilisateur \_ est utilisée par une application pour interroger la valeur du contrôle de **taille de police** .</span><span class="sxs-lookup"><span data-stu-id="f87a5-106">UI\_PKEY\_FontProperties\_Size is used by an application to query the value of the **Font size** control.</span></span>

<span data-ttu-id="f87a5-107">Les valeurs valides pour cette propriété sont comprises entre 1 et 9999 inclus.</span><span class="sxs-lookup"><span data-stu-id="f87a5-107">Valid values for this property range from 1 to 9999, inclusive.</span></span> <span data-ttu-id="f87a5-108">Si un utilisateur tente d’entrer une valeur non valide, l’entrée est rejetée et le contrôle de **taille de police** revient à la dernière valeur valide.</span><span class="sxs-lookup"><span data-stu-id="f87a5-108">If a user tries to enter an invalid value, the entry is rejected and the **Font size** control reverts to the last valid value.</span></span>

<span data-ttu-id="f87a5-109">Si une application tente de définir la taille de police par programmation sur une valeur en dehors de la plage valide, l’infrastructure du ruban invalide toutes les propriétés de police et définit les contrôles de police (**taille de police** et **type de police**) à vide ou à leur état par défaut, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f87a5-109">If an application attempts to set font size programmatically to a value outside the valid range, the Ribbon framework invalidates all font properties and sets the font controls (**Font size** and **Font face**) to blank or to their default state, where appropriate.</span></span>

<span data-ttu-id="f87a5-110">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="f87a5-110">The default value is 0.</span></span>

<span data-ttu-id="f87a5-111">La valeur 0 indique qu’aucune taille de point unique n’est sélectionnée (aucun texte, ou une série de texte de taille hétérogène, est sélectionnée).</span><span class="sxs-lookup"><span data-stu-id="f87a5-111">A value of 0 specifies that no single point size is selected (either no text, or a run of heterogeneously sized text, is selected).</span></span>

<span data-ttu-id="f87a5-112">Un utilisateur ne peut pas définir la valeur 0 pour le contrôle de la taille de la **police** .</span><span class="sxs-lookup"><span data-stu-id="f87a5-112">A user cannot set the **Font size** control to 0.</span></span>

<span data-ttu-id="f87a5-113">En dehors de 0, les valeurs valides pour la plage de taille FontProperties de l’interface utilisateur est \_ \_ \_ comprise entre *MinimumFontSize* et *MaximumFontSize* comme déclaré dans le balisage de [contrôle de police](windowsribbon-controls-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="f87a5-113">Other than 0, valid values for UI\_PKEY\_FontProperties\_Size range between *MinimumFontSize* and *MaximumFontSize* as declared in the [Font Control](windowsribbon-controls-fontcontrol.md) markup.</span></span>

> [!Note]  
> <span data-ttu-id="f87a5-114">Le contrôle de **taille de police** est défini sur vide lorsque la taille de police est définie par programme sur 0, par exemple lorsqu’une exécution de texte de taille hétérogène est mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="f87a5-114">The **Font size** control is set to blank when the font size is programmatically set to 0, such as when a run of heterogeneously sized text is highlighted.</span></span>

 

<span data-ttu-id="f87a5-115">Lorsqu’une exécution de texte de taille hétérogène est sélectionnée, l’application doit interroger l' [interface utilisateur \_ \_ FontProperties \_](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) de l’IU pour capturer les commandes **agrandir la police** et **réduire la police** .</span><span class="sxs-lookup"><span data-stu-id="f87a5-115">Where a run of heterogeneously sized text is selected, the application should query [UI\_PKEY\_FontProperties\_DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) to capture **Grow font** and **Shrink font** commands.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f87a5-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f87a5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f87a5-117">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="f87a5-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="f87a5-118">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="f87a5-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




