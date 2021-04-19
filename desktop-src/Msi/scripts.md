---
description: Une action personnalisée peut appeler des fonctions écrites en VBScript ou JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: scripts ;
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533643"
---
# <a name="scripts"></a><span data-ttu-id="a025d-103">scripts ;</span><span class="sxs-lookup"><span data-stu-id="a025d-103">Scripts</span></span>

<span data-ttu-id="a025d-104">Une action personnalisée peut appeler des fonctions écrites en VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="a025d-104">A custom action can call functions that are written in VBScript or JScript.</span></span> <span data-ttu-id="a025d-105">Windows Installer ne fournit pas le moteur de script.</span><span class="sxs-lookup"><span data-stu-id="a025d-105">Windows Installer does not provide the script engine.</span></span> <span data-ttu-id="a025d-106">Les auteurs souhaitant utiliser un langage de script pendant l’installation doivent donc s’assurer que le moteur de script approprié est disponible.</span><span class="sxs-lookup"><span data-stu-id="a025d-106">Authors wishing to make use of a scripting language during installation must therefore ensure that the appropriate scripting engine is available.</span></span>

<span data-ttu-id="a025d-107">Le programme d’installation ne prend pas en charge la version 1,0 de JScript.</span><span class="sxs-lookup"><span data-stu-id="a025d-107">The installer does not support JScript version 1.0.</span></span>

<span data-ttu-id="a025d-108">Une action personnalisée 64 bits basée sur des scripts doit être marquée explicitement comme une action personnalisée 64 bits en ajoutant le bit **msidbCustomActionType64BitScript** au type numérique actions personnalisées dans la colonne type de la table [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a025d-108">A 64-bit custom action based on scripts must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction](customaction-table.md) table.</span></span> <span data-ttu-id="a025d-109">Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="a025d-109">For information see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

<span data-ttu-id="a025d-110">Les types d’actions personnalisées de base suivants appellent des fonctions écrites en script.</span><span class="sxs-lookup"><span data-stu-id="a025d-110">The following basic custom action types call functions written in script.</span></span>



| <span data-ttu-id="a025d-111">Type d’action personnalisé</span><span class="sxs-lookup"><span data-stu-id="a025d-111">Custom action type</span></span>                                 | <span data-ttu-id="a025d-112">Description</span><span class="sxs-lookup"><span data-stu-id="a025d-112">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a025d-113">Type d’action personnalisé 5</span><span class="sxs-lookup"><span data-stu-id="a025d-113">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="a025d-114">Fichier JScript stocké dans un flux de table binaire.</span><span class="sxs-lookup"><span data-stu-id="a025d-114">JScript file stored in a Binary table stream.</span></span>                                                  |
| [<span data-ttu-id="a025d-115">Type d’action personnalisée 21</span><span class="sxs-lookup"><span data-stu-id="a025d-115">Custom Action Type 21</span></span>](custom-action-type-21.md) | <span data-ttu-id="a025d-116">Fichier JScript installé avec un produit.</span><span class="sxs-lookup"><span data-stu-id="a025d-116">JScript file that is installed with a product.</span></span>                                                 |
| [<span data-ttu-id="a025d-117">Type d’action personnalisé 53</span><span class="sxs-lookup"><span data-stu-id="a025d-117">Custom Action Type 53</span></span>](custom-action-type-53.md) | <span data-ttu-id="a025d-118">Texte JScript spécifié par une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="a025d-118">JScript text specified by a property value.</span></span>                                                    |
| [<span data-ttu-id="a025d-119">Type d’action personnalisé 37</span><span class="sxs-lookup"><span data-stu-id="a025d-119">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="a025d-120">Texte JScript stocké dans la colonne cible de la table [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a025d-120">JScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span>  |
| [<span data-ttu-id="a025d-121">Type d’action personnalisé 6</span><span class="sxs-lookup"><span data-stu-id="a025d-121">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="a025d-122">Fichier VBScript stocké dans un flux de table [binaire](binary-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a025d-122">VBScript file stored in a [Binary](binary-table.md) table stream.</span></span>                             |
| [<span data-ttu-id="a025d-123">Type d’action personnalisée 22</span><span class="sxs-lookup"><span data-stu-id="a025d-123">Custom Action Type 22</span></span>](custom-action-type-22.md) | <span data-ttu-id="a025d-124">Fichier VBScript installé avec un produit.</span><span class="sxs-lookup"><span data-stu-id="a025d-124">VBScript file that is installed with a product.</span></span>                                                |
| [<span data-ttu-id="a025d-125">Type d’action personnalisé 54</span><span class="sxs-lookup"><span data-stu-id="a025d-125">Custom Action Type 54</span></span>](custom-action-type-54.md) | <span data-ttu-id="a025d-126">Texte VBScript spécifié par une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="a025d-126">VBScript text specified by a property value.</span></span>                                                   |
| [<span data-ttu-id="a025d-127">Type d’action personnalisé 38</span><span class="sxs-lookup"><span data-stu-id="a025d-127">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="a025d-128">Texte VBScript stocké dans la colonne cible de la table [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a025d-128">VBScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span> |



 

> [!Note]  
> <span data-ttu-id="a025d-129">Le programme d’installation exécute des actions personnalisées de script directement et n’utilise pas Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="a025d-129">The installer runs script custom actions directly and does not use the Windows Script Host.</span></span> <span data-ttu-id="a025d-130">L’objet **wscript** ne peut pas être utilisé à l’intérieur d’une action personnalisée de script, car cet objet est fourni par Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="a025d-130">The **WScript** object cannot be used inside a script custom action because this object is provided by the Windows Script Host.</span></span> <span data-ttu-id="a025d-131">Les objets dans le modèle d’objet Windows Script Host peuvent uniquement être utilisés dans des actions personnalisées si Windows Script Host est installé sur l’ordinateur en créant de nouvelles instances de l’objet, avec un appel à CreateObject et en fournissant le ProgId de l’objet (par exemple « WScript. Shell »).</span><span class="sxs-lookup"><span data-stu-id="a025d-131">Objects in the Windows Script Host object model can only be used in custom actions if Windows Script Host is installed on the computer by creating new instances of the object, with a call to CreateObject, and providing the ProgId of the object (for example "WScript.Shell").</span></span> <span data-ttu-id="a025d-132">Selon le type d’action personnalisée de script, l’accès à certains objets et méthodes du modèle objet Windows Script Host peut être refusé pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a025d-132">Depending on the type of script custom action, access to some objects and methods of the Windows Script Host object model may be denied for security reasons.</span></span>

 

<span data-ttu-id="a025d-133">Pour plus d’informations, consultez la [liste récapitulative de tous les types d’actions personnalisées](summary-list-of-all-custom-action-types.md) pour obtenir un résumé de tous les types d’actions personnalisées et la façon dont elles sont encodées dans la table [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a025d-133">For more information, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction](customaction-table.md) table.</span></span>

 

 



