---
description: Pour chaque mot de passe qui doit être entré par l’utilisateur, ajoutez un contrôle d’édition sur une boîte de dialogue qui stocke la valeur du mot de passe dans une propriété.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Création de l’interface utilisateur pour l’entrée de mot de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518650"
---
# <a name="authoring-the-user-interface-for-password-input"></a><span data-ttu-id="c2184-103">Création de l’interface utilisateur pour l’entrée de mot de passe</span><span class="sxs-lookup"><span data-stu-id="c2184-103">Authoring the User Interface for Password Input</span></span>

<span data-ttu-id="c2184-104">Pour chaque mot de passe qui doit être entré par l’utilisateur, ajoutez un contrôle d’édition sur une boîte de dialogue qui stocke la valeur du mot de passe dans une propriété.</span><span class="sxs-lookup"><span data-stu-id="c2184-104">For each password that must be entered by the user, add an edit control on a dialog that stores the value of the password into a property.</span></span> <span data-ttu-id="c2184-105">Ce [contrôle d’édition](edit-control.md) doit avoir l' [attribut de contrôle de mot de passe](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="c2184-105">This [edit control](edit-control.md) should have the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="c2184-106">Cela spécifie que la propriété entrée est un mot de passe et empêche le programme d’installation d’écrire la propriété dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="c2184-106">This specifies that the property entered is a password and prevents the installer from writing the property to the log file.</span></span>

<span data-ttu-id="c2184-107">Les [attributs de contrôle](control-attributes.md) du contrôle de modification de mot de passe sont MsidbControlAttributesVisible, MsidbControlAttributesEnabled et msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span><span class="sxs-lookup"><span data-stu-id="c2184-107">The [control attributes](control-attributes.md) for the password edit control are msidbControlAttributesVisible, msidbControlAttributesEnabled, and msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span></span> <span data-ttu-id="c2184-108">Les cases X, Y, largeur, hauteur et contrôle \_ dépendent de la disposition du contrôle dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c2184-108">The X, Y, Width, Height, and Control\_Next depend on the layout of the control on the dialog.</span></span>

[<span data-ttu-id="c2184-109">Table de contrôle</span><span class="sxs-lookup"><span data-stu-id="c2184-109">Control Table</span></span>](control-table.md)



| <span data-ttu-id="c2184-110">Dialogue\_</span><span class="sxs-lookup"><span data-stu-id="c2184-110">Dialog\_</span></span> | <span data-ttu-id="c2184-111">contrôle\_</span><span class="sxs-lookup"><span data-stu-id="c2184-111">Control\_</span></span>            | <span data-ttu-id="c2184-112">Type</span><span class="sxs-lookup"><span data-stu-id="c2184-112">Type</span></span> | <span data-ttu-id="c2184-113">X</span><span class="sxs-lookup"><span data-stu-id="c2184-113">X</span></span>   | <span data-ttu-id="c2184-114">O</span><span class="sxs-lookup"><span data-stu-id="c2184-114">Y</span></span>   | <span data-ttu-id="c2184-115">Largeur</span><span class="sxs-lookup"><span data-stu-id="c2184-115">Width</span></span> | <span data-ttu-id="c2184-116">Hauteur</span><span class="sxs-lookup"><span data-stu-id="c2184-116">Height</span></span> | <span data-ttu-id="c2184-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="c2184-117">Attributes</span></span> | <span data-ttu-id="c2184-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="c2184-118">Property</span></span>         | <span data-ttu-id="c2184-119">Texte</span><span class="sxs-lookup"><span data-stu-id="c2184-119">Text</span></span> | <span data-ttu-id="c2184-120">Contrôle \_ suivant</span><span class="sxs-lookup"><span data-stu-id="c2184-120">Control\_Next</span></span> | <span data-ttu-id="c2184-121">Aide</span><span class="sxs-lookup"><span data-stu-id="c2184-121">Help</span></span> |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| <span data-ttu-id="c2184-122">MyDialog</span><span class="sxs-lookup"><span data-stu-id="c2184-122">MyDialog</span></span> | <span data-ttu-id="c2184-123">TestUserPasswordEdit</span><span class="sxs-lookup"><span data-stu-id="c2184-123">TestUserPasswordEdit</span></span> | <span data-ttu-id="c2184-124">Modifier</span><span class="sxs-lookup"><span data-stu-id="c2184-124">Edit</span></span> | <span data-ttu-id="c2184-125">25</span><span class="sxs-lookup"><span data-stu-id="c2184-125">25</span></span>  | <span data-ttu-id="c2184-126">120</span><span class="sxs-lookup"><span data-stu-id="c2184-126">120</span></span> | <span data-ttu-id="c2184-127">300</span><span class="sxs-lookup"><span data-stu-id="c2184-127">300</span></span>   | <span data-ttu-id="c2184-128">20</span><span class="sxs-lookup"><span data-stu-id="c2184-128">20</span></span>     | <span data-ttu-id="c2184-129">2097155</span><span class="sxs-lookup"><span data-stu-id="c2184-129">2097155</span></span>    | <span data-ttu-id="c2184-130">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="c2184-130">TESTUSERPASSWORD</span></span> |      | <span data-ttu-id="c2184-131">Annuler</span><span class="sxs-lookup"><span data-stu-id="c2184-131">Cancel</span></span>        |      |



 

<span data-ttu-id="c2184-132">Continuez à [sécuriser l’installation](securing-the-installation.md).</span><span class="sxs-lookup"><span data-stu-id="c2184-132">Continue to [Securing the installation](securing-the-installation.md).</span></span>

 

 



