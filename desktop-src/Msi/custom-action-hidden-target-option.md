---
description: Utilisez les indicateurs d’option suivants pour spécifier que le programme d’installation n’écrit pas la valeur entrée dans le champ cible de la table CustomAction dans le journal. Pour définir l’option, ajoutez la valeur de ce tableau à la valeur du champ type de la table CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Option cible masquée des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034651"
---
# <a name="custom-action-hidden-target-option"></a><span data-ttu-id="3f023-104">Option cible masquée des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="3f023-104">Custom Action Hidden Target Option</span></span>

<span data-ttu-id="3f023-105">Utilisez les indicateurs d’option suivants pour spécifier que le programme d’installation n’écrit pas la valeur entrée dans le champ cible de la [table CustomAction](customaction-table.md) dans le journal.</span><span class="sxs-lookup"><span data-stu-id="3f023-105">Use the following option flags to specify that the installer not write the value entered into the Target field of the [CustomAction table](customaction-table.md) into the log.</span></span> <span data-ttu-id="3f023-106">Pour définir l’option, ajoutez la valeur de ce tableau à la valeur du champ type de la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="3f023-106">To set the option add the value in this table to the value in the Type field of the CustomAction table.</span></span>



| <span data-ttu-id="3f023-107">Constante</span><span class="sxs-lookup"><span data-stu-id="3f023-107">Constant</span></span>                            | <span data-ttu-id="3f023-108">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="3f023-108">Hexadecimal</span></span> | <span data-ttu-id="3f023-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f023-109">Decimal</span></span> | <span data-ttu-id="3f023-110">Description</span><span class="sxs-lookup"><span data-stu-id="3f023-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f023-111">(aucun)</span><span class="sxs-lookup"><span data-stu-id="3f023-111">(none)</span></span>                              | <span data-ttu-id="3f023-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="3f023-112">0x0000</span></span>      | <span data-ttu-id="3f023-113">0</span><span class="sxs-lookup"><span data-stu-id="3f023-113">0</span></span>       | <span data-ttu-id="3f023-114">Le programme d’installation peut écrire la valeur dans la colonne cible de la table CustomAction dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="3f023-114">The installer may write the value in the Target column of the CustomAction table into the log file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="3f023-115">**msidbCustomActionTypeHideTarget**</span><span class="sxs-lookup"><span data-stu-id="3f023-115">**msidbCustomActionTypeHideTarget**</span></span> | <span data-ttu-id="3f023-116">0x2000</span><span class="sxs-lookup"><span data-stu-id="3f023-116">0x2000</span></span>      | <span data-ttu-id="3f023-117">8 192</span><span class="sxs-lookup"><span data-stu-id="3f023-117">8192</span></span>    | <span data-ttu-id="3f023-118">Le programme d’installation ne peut pas écrire la valeur dans la colonne cible de la [table CustomAction](customaction-table.md) dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="3f023-118">The installer is prevented from writing the value in the Target column of the [CustomAction table](customaction-table.md) into the log file.</span></span> <span data-ttu-id="3f023-119">La propriété CustomActionData n’est pas non plus journalisée lorsque le programme d’installation exécute l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="3f023-119">The CustomActionData property is also not logged when the installer executes the custom action.</span></span><br/> <span data-ttu-id="3f023-120">Étant donné que le programme d’installation définit la valeur de CustomActionData à partir d’une propriété portant le même nom que l’action personnalisée, cette propriété doit être listée dans la propriété [**MsiHiddenProperties**](msihiddenproperties.md) pour empêcher sa valeur d’apparaître dans le journal.</span><span class="sxs-lookup"><span data-stu-id="3f023-120">Because the installer sets the value of CustomActionData from a property with the same name as the custom action, that property must be listed in the [**MsiHiddenProperties**](msihiddenproperties.md) Property to prevent its value from appearing in the log.</span></span><br/> |



 

<span data-ttu-id="3f023-121">Pour plus d’informations, consultez [empêcher l’écriture d’informations confidentielles dans le fichier journal](preventing-confidential-information-from-being-written-into-the-log-file.md) .</span><span class="sxs-lookup"><span data-stu-id="3f023-121">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f023-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f023-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f023-123">Référence des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="3f023-123">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="3f023-124">À propos des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="3f023-124">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="3f023-125">Utilisation d’actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="3f023-125">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 




