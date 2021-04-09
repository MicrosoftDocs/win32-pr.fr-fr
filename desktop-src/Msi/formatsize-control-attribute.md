---
description: Si ce bit est défini pour un contrôle de texte statique, le contrôle essaie automatiquement de mettre en forme le texte affiché sous la forme d’un nombre qui représente un nombre d’octets.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Formater l’attribut de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201959"
---
# <a name="formatsize-control-attribute"></a><span data-ttu-id="9c0f3-103">Formater l’attribut de contrôle</span><span class="sxs-lookup"><span data-stu-id="9c0f3-103">FormatSize Control Attribute</span></span>

<span data-ttu-id="9c0f3-104">Si ce bit est défini pour un contrôle de texte statique, le contrôle essaie automatiquement de mettre en forme le texte affiché sous la forme d’un nombre qui représente un nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-104">If this bit is set for a static text control, the control automatically attempts to format the displayed text as a number that represents a count of bytes.</span></span> <span data-ttu-id="9c0f3-105">Pour une mise en forme appropriée, le texte du contrôle doit être défini sur une chaîne qui représente un nombre exprimé en unités de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-105">For proper formatting, the control's text must be set to a string that represents a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="9c0f3-106">La valeur affichée est ensuite exprimée en kilo-octets (Ko), mégaoctets (Mo) ou gigaoctets (Go) et affichée avec la chaîne appropriée qui représente les unités.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-106">The displayed value is then formatted in kilobytes (KB), megabytes (MB), or gigabytes (GB), and displayed with the appropriate string that represents the units.</span></span> <span data-ttu-id="9c0f3-107">Pour plus d’informations, consultez [contrôle de texte](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="9c0f3-107">For more information, see [Text Control](text-control.md).</span></span>



| <span data-ttu-id="9c0f3-108">Valeur numérique du texte d’origine</span><span class="sxs-lookup"><span data-stu-id="9c0f3-108">Numerical value of original text</span></span> | <span data-ttu-id="9c0f3-109">Chaîne d’unité utilisée</span><span class="sxs-lookup"><span data-stu-id="9c0f3-109">Unit string used</span></span> |
|----------------------------------|------------------|
| <span data-ttu-id="9c0f3-110">Inférieur à 20480</span><span class="sxs-lookup"><span data-stu-id="9c0f3-110">Less than 20480</span></span>                  | <span data-ttu-id="9c0f3-111">Ko</span><span class="sxs-lookup"><span data-stu-id="9c0f3-111">KB</span></span>               |
| <span data-ttu-id="9c0f3-112">Inférieur à 20971520</span><span class="sxs-lookup"><span data-stu-id="9c0f3-112">Less than 20971520</span></span>               | <span data-ttu-id="9c0f3-113">Mo</span><span class="sxs-lookup"><span data-stu-id="9c0f3-113">MB</span></span>               |
| <span data-ttu-id="9c0f3-114">Inférieur à 10737418240</span><span class="sxs-lookup"><span data-stu-id="9c0f3-114">Less than 10737418240</span></span>            | <span data-ttu-id="9c0f3-115">Go</span><span class="sxs-lookup"><span data-stu-id="9c0f3-115">GB</span></span>               |



 

## <a name="valid-controls"></a><span data-ttu-id="9c0f3-116">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="9c0f3-116">Valid Controls</span></span>



| <span data-ttu-id="9c0f3-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="9c0f3-117">Decimal</span></span> | <span data-ttu-id="9c0f3-118">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="9c0f3-118">Hexadecimal</span></span> | <span data-ttu-id="9c0f3-119">Contrôler</span><span class="sxs-lookup"><span data-stu-id="9c0f3-119">Control</span></span>                          |
|---------|-------------|----------------------------------|
| <span data-ttu-id="9c0f3-120">524 288</span><span class="sxs-lookup"><span data-stu-id="9c0f3-120">524288</span></span>  | <span data-ttu-id="9c0f3-121">0x00080000</span><span class="sxs-lookup"><span data-stu-id="9c0f3-121">0x00080000</span></span>  | <span data-ttu-id="9c0f3-122">msidbControlAttributesFormatSize</span><span class="sxs-lookup"><span data-stu-id="9c0f3-122">msidbControlAttributesFormatSize</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9c0f3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9c0f3-123">Remarks</span></span>

<span data-ttu-id="9c0f3-124">Pour définir cet attribut sur un contrôle, incluez les bits de format dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="9c0f3-124">To set this attribute on a control, include the FormatSize bits in the Attributes column of the control's record in the [Control Table](control-table.md).</span></span> <span data-ttu-id="9c0f3-125">Le texte du contrôle doit être défini sur une chaîne représentant un nombre exprimé en unités de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-125">The control's text must be set to a string representing a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="9c0f3-126">Le texte des chaînes d’unité est défini dans la [table UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="9c0f3-126">The text of the unit strings are defined in the [UIText Table](uitext-table.md).</span></span> <span data-ttu-id="9c0f3-127">Le positionnement de la chaîne d’unité est contrôlé par la propriété [**LeftUnit**](leftunit.md) .</span><span class="sxs-lookup"><span data-stu-id="9c0f3-127">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="9c0f3-128">Si la propriété **LeftUnit** est définie comme n’importe quelle valeur, la chaîne d’unité apparaît avant la valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-128">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span> <span data-ttu-id="9c0f3-129">Si tout autre caractère numérique apparaît dans le texte associé au contrôle, la valeur affichée n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-129">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="9c0f3-130">Au moment de l’exécution, le programme d’installation résout la valeur de la propriété [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) sur le nombre total d’octets requis pour l’installation, en unités de 512.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-130">At run time, the installer resolves the [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) Property to the total number of bytes required for the installation in units of 512.</span></span> <span data-ttu-id="9c0f3-131">Un contrôle de texte statique avec le bit de mise en forme peut être utilisé pour mettre automatiquement en forme et étiqueter le nombre total d’octets requis pour l’installation, en Ko, Mo ou Go, selon le cas.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-131">A static text control with FormatSize bit can be used to automatically format and label the total number of bytes required for the installation in KB, MB, or GB as appropriate.</span></span> <span data-ttu-id="9c0f3-132">Dans le cadre de cet exemple, supposons que le nombre total d’octets est 18 336 768.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-132">For the purposes of this example, assume the total number of bytes is 18,336,768.</span></span> <span data-ttu-id="9c0f3-133">Le programme d’installation définit la valeur de la propriété PrimaryVolumeSpaceRequired sur 18 336 768 divisée par 512, ou 35 814.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-133">The installer sets the value of the PrimaryVolumeSpaceRequired property to 18,336,768 divided by 512, or 35,814.</span></span> <span data-ttu-id="9c0f3-134">Le nombre affiché par le contrôle de texte avec la fonction de formatage est 17MB.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-134">The number displayed by the text control with FormatSize would be 17MB.</span></span>

<span data-ttu-id="9c0f3-135">Les valeurs numériques du texte d’origine sont indiquées en unités de 512.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-135">The numerical values of the original text are given in units of 512.</span></span> <span data-ttu-id="9c0f3-136">Dans le tableau ci-dessus, la chaîne 20 480 correspond à la chaîne de base de connaissances, car 20 480 fois 512 produit un résultat de 10 485 760 octets ou de 10 240 Ko.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-136">In the table above, the string 20,480 corresponds to the KB string because 20,480 times 512 yields a result of 10,485,760 bytes or 10,240 KB.</span></span>

<span data-ttu-id="9c0f3-137">Les chaînes d’unités listées dans le tableau précédent font référence aux clés de la [table UIText](uitext-table.md), où le texte de la chaîne d’unité est défini.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-137">The unit strings listed in the previous table refer to keys in the [UIText Table](uitext-table.md), where the text of the unit string is defined.</span></span>

<span data-ttu-id="9c0f3-138">Le positionnement de la chaîne d’unité est contrôlé par la propriété [**LeftUnit**](leftunit.md) .</span><span class="sxs-lookup"><span data-stu-id="9c0f3-138">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="9c0f3-139">Si la propriété **LeftUnit** est définie comme n’importe quelle valeur, la chaîne d’unité apparaît avant la valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-139">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span>

<span data-ttu-id="9c0f3-140">Si tout autre caractère numérique apparaît dans le texte associé au contrôle, la valeur affichée n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="9c0f3-140">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="9c0f3-141">Pour plus d’informations, consultez [contrôles](controls.md)et [attributs](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="9c0f3-141">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



