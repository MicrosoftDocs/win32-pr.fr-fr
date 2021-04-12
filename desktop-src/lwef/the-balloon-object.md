---
title: Objet Balloon
description: Objet Balloon
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0c94803e9efadde1ae4a8410273ed49437291a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104198904"
---
# <a name="the-balloon-object"></a><span data-ttu-id="4ae76-103">Objet Balloon</span><span class="sxs-lookup"><span data-stu-id="4ae76-103">The Balloon Object</span></span>

<span data-ttu-id="4ae76-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ae76-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4ae76-105">Microsoft agent prend en charge le sous-titrage textuel de la méthode [**Speak**](speak-method.md) à l’aide d’une bulle de texte animé.</span><span class="sxs-lookup"><span data-stu-id="4ae76-105">Microsoft Agent supports textual captioning of [**Speak**](speak-method.md) method using a cartoon word balloon.</span></span> <span data-ttu-id="4ae76-106">La méthode de [**réflexion**](think-method.md) vous permet d’afficher du texte sans sortie audio dans une bulle de mot « pensée ».</span><span class="sxs-lookup"><span data-stu-id="4ae76-106">The [**Think**](think-method.md) method enables you to display text without audio output in a "thought" word balloon.</span></span>

<span data-ttu-id="4ae76-107">Les valeurs par défaut de la fenêtre de la bulle initiale d’un caractère sont définies et compilées dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4ae76-107">A character's initial word balloon window defaults are defined and compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4ae76-108">Une fois exécuté, les propriétés [**activées**](enabled-property.md) et de [**police**](https://www.bing.com/search?q=**Font**) de l’info-bulle peuvent être remplacées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ae76-108">Once running, the balloon's [**Enabled**](enabled-property.md) and [**Font**](https://www.bing.com/search?q=**Font**) properties may be overridden by the user.</span></span> <span data-ttu-id="4ae76-109">Si un utilisateur modifie les propriétés de la bulle de mot, il affecte tous les caractères.</span><span class="sxs-lookup"><span data-stu-id="4ae76-109">If a user changes the word balloon's properties, they affect all characters.</span></span> <span data-ttu-id="4ae76-110">Les bulles de mot [**parole**](speak-method.md) et de [**réflexion**](think-method.md) utilisent les mêmes paramètres de propriété pour la taille.</span><span class="sxs-lookup"><span data-stu-id="4ae76-110">Both the [**Speak**](speak-method.md) and [**Think**](think-method.md) word balloons use the same property settings for size.</span></span> <span data-ttu-id="4ae76-111">Vous pouvez accéder aux propriétés de la bulle de texte d’un caractère par le biais de l’objet [**Balloon**](/windows/desktop/lwef/the-balloon-object) , qui est un enfant de l’objet [**character**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="4ae76-111">You can access the properties for a character's word balloon through the [**Balloon**](/windows/desktop/lwef/the-balloon-object) object, which is a child of the [**Character**](/windows/desktop/lwef/the-characters-object) object.</span></span>

<span data-ttu-id="4ae76-112">L’objet [**Balloon**](/windows/desktop/lwef/the-balloon-object) prend en charge les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ae76-112">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object supports the following properties:</span></span>

-   [<span data-ttu-id="4ae76-113">**BackColor**</span><span class="sxs-lookup"><span data-stu-id="4ae76-113">**BackColor**</span></span>](backcolor-property.md)
-   [<span data-ttu-id="4ae76-114">**BorderColor**</span><span class="sxs-lookup"><span data-stu-id="4ae76-114">**BorderColor**</span></span>](bordercolor-property.md)
-   [<span data-ttu-id="4ae76-115">**CharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="4ae76-115">**CharsPerLine**</span></span>](charsperline-property.md)
-   [<span data-ttu-id="4ae76-116">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="4ae76-116">**Enabled**</span></span>](enabled-property.md)
-   [<span data-ttu-id="4ae76-117">**FontCharSet**</span><span class="sxs-lookup"><span data-stu-id="4ae76-117">**FontCharSet**</span></span>](fontcharset-property.md)
-   [<span data-ttu-id="4ae76-118">**FontName**</span><span class="sxs-lookup"><span data-stu-id="4ae76-118">**FontName**</span></span>](fontname-property-bal.md)
-   [<span data-ttu-id="4ae76-119">**Gras**</span><span class="sxs-lookup"><span data-stu-id="4ae76-119">**FontBold**</span></span>](fontbold-property.md)
-   [<span data-ttu-id="4ae76-120">**Italique**</span><span class="sxs-lookup"><span data-stu-id="4ae76-120">**FontItalic**</span></span>](fontitalic-property.md)
-   [<span data-ttu-id="4ae76-121">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="4ae76-121">**FontSize**</span></span>](fontsize-property-bal.md)
-   [<span data-ttu-id="4ae76-122">**FontStrikeThru**</span><span class="sxs-lookup"><span data-stu-id="4ae76-122">**FontStrikeThru**</span></span>](fontstrikethru-property.md)
-   [<span data-ttu-id="4ae76-123">**Souligné**</span><span class="sxs-lookup"><span data-stu-id="4ae76-123">**FontUnderline**</span></span>](fontunderline-property.md)
-   [<span data-ttu-id="4ae76-124">**CouleurTexte**</span><span class="sxs-lookup"><span data-stu-id="4ae76-124">**ForeColor**</span></span>](forecolor-property.md)
-   [<span data-ttu-id="4ae76-125">**NumberOfLines**</span><span class="sxs-lookup"><span data-stu-id="4ae76-125">**NumberOfLines**</span></span>](numberoflines-property.md)
-   [<span data-ttu-id="4ae76-126">**Style**</span><span class="sxs-lookup"><span data-stu-id="4ae76-126">**Style**</span></span>](style-property.md)
-   [<span data-ttu-id="4ae76-127">**Parent**</span><span class="sxs-lookup"><span data-stu-id="4ae76-127">**Visible**</span></span>](visible-property-bal.md)

 

 