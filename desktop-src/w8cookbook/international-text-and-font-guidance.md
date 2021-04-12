---
title: Aide sur le texte et les polices internationaux
description: Aide sur le texte et les polices internationaux
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104381974"
---
# <a name="international-text-and-font-guidance"></a><span data-ttu-id="4f3c0-103">Aide sur le texte et les polices internationaux</span><span class="sxs-lookup"><span data-stu-id="4f3c0-103">International text and font guidance</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4f3c0-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="4f3c0-104">Affected Platforms</span></span>

<dl> <span data-ttu-id="4f3c0-105">Clients-Windows 8 \| Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4f3c0-105">Clients - Windows 8 \| Windows 8.1</span></span>  
<span data-ttu-id="4f3c0-106">Serveurs-Windows Server 2012 \| Windows server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4f3c0-106">Servers - Windows Server 2012 \| Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="4f3c0-107">Description</span><span class="sxs-lookup"><span data-stu-id="4f3c0-107">Description</span></span>

<span data-ttu-id="4f3c0-108">Depuis avant Windows 2000, la prise en charge de l’affichage de texte pour les nouveaux scripts a été ajoutée dans chaque version majeure de Windows.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-108">Since before Windows 2000, text-display support for new scripts has been added in each major release of Windows.</span></span> <span data-ttu-id="4f3c0-109">Vous trouverez des descriptions des modifications apportées dans chaque version majeure dans l’article [prise en charge des scripts et des polices pour Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) dans le [Centre de développement global](https://msdn.microsoft.com/goglobal/default).</span><span class="sxs-lookup"><span data-stu-id="4f3c0-109">You can find descriptions of the changes made in each major release in the [Script and Font Support for Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) article at the [Go Global Development Center](https://msdn.microsoft.com/goglobal/default).</span></span>

<span data-ttu-id="4f3c0-110">Notez que la prise en charge d’un script peut nécessiter certaines modifications apportées aux composants de pile de texte, ainsi que les modifications apportées aux polices.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-110">Note that support for a script may require certain changes to text stack components as well as changes to fonts.</span></span> <span data-ttu-id="4f3c0-111">Le système d’exploitation Windows possède de nombreux composants de pile de texte : DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 et d’autres.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-111">The Windows operating system has many text stack components: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32, and others.</span></span> <span data-ttu-id="4f3c0-112">Les informations fournies concernent principalement GDI et DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-112">The information provided pertains primarily to GDI and DirectWrite.</span></span> <span data-ttu-id="4f3c0-113">Elle s’applique également aux infrastructures d’interface utilisateur telles que RichEdit ou l’agent de rendu MSHTML utilisé pour les applications du Windows Store de Windows 8 et pour le rendu du contenu Web, bien que ces composants puissent présenter certaines différences.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-113">It is also generally applicable to UI frameworks such as RichEdit or the MSHTML rendering agent used for Windows 8 Store apps and for rendering web content, though those components may exhibit certain differences.</span></span>

## <a name="best-practices"></a><span data-ttu-id="4f3c0-114">Bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="4f3c0-114">Best Practices</span></span>

<span data-ttu-id="4f3c0-115">**Conseils typographiques pour les développeurs**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-115">**Typography guidance for developers**</span></span>

<span data-ttu-id="4f3c0-116">La typographie est au cœur du langage de conception Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-116">Typography is at the heart of the Microsoft design language.</span></span> <span data-ttu-id="4f3c0-117">Chacun des principes de conception de Microsoft renforce l’importance de la typographie.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-117">Each of the Microsoft design principles reinforces the importance of typography.</span></span> <span data-ttu-id="4f3c0-118">Pour la première fois, les développeurs d’applications disposent d’un ensemble de frameworks qui prennent en charge des fonctionnalités typographiques avancées.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-118">For the first time, app developers have a set of frameworks that support advanced typographic features.</span></span> <span data-ttu-id="4f3c0-119">Accédez à [affichage et modification de texte](/previous-versions/windows/apps/hh465442(v=win.10)) pour plus d’informations sur l’utilisation de JavaScript et HTML pour afficher et modifier du texte dans les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-119">Go to [Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10)) for information about how to use JavaScript and HTML to display and edit text in Windows Store apps.</span></span>

<span data-ttu-id="4f3c0-120">**Métriques de police**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-120">**Font metrics**</span></span>

<span data-ttu-id="4f3c0-121">Les métriques de police sont une zone particulièrement importante pour les développeurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-121">Font metrics are an area of particular importance to application developers.</span></span> <span data-ttu-id="4f3c0-122">Les fichiers de polices contiennent différentes valeurs liées aux métriques verticales et horizontales.</span><span class="sxs-lookup"><span data-stu-id="4f3c0-122">Font files contain various values related to vertical and horizontal metrics.</span></span> <span data-ttu-id="4f3c0-123">Ces valeurs sont documentées dans la [spécification OpenType](https://www.microsoft.com/typography/otspec/) . elles sont exposées par le biais d’une série d’API disponibles dans [structure des \_ \_ métriques de police DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) et au niveau de la [structure TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span><span class="sxs-lookup"><span data-stu-id="4f3c0-123">These values are documented in the [OpenType specification](https://www.microsoft.com/typography/otspec/) and these are exposed via a variety of APIs found at [DWRITE\_FONT\_METRICS structure](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) and at [TEXTMETRIC Structure](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span></span>

## <a name="resources"></a><span data-ttu-id="4f3c0-124">Ressources</span><span class="sxs-lookup"><span data-stu-id="4f3c0-124">Resources</span></span>

-   [<span data-ttu-id="4f3c0-125">Prise en charge des scripts et des polices pour Windows</span><span class="sxs-lookup"><span data-stu-id="4f3c0-125">Script and Font Support for Windows</span></span>](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [<span data-ttu-id="4f3c0-126">Accédez au centre de développement global</span><span class="sxs-lookup"><span data-stu-id="4f3c0-126">Go Global Development Center</span></span>](https://msdn.microsoft.com/goglobal/default)
-   <span data-ttu-id="4f3c0-127">[Affichage et modification de texte](/previous-versions/windows/apps/hh465442(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="4f3c0-127">[Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10))</span></span>
-   [<span data-ttu-id="4f3c0-128">Spécification OpenType</span><span class="sxs-lookup"><span data-stu-id="4f3c0-128">OpenType specification</span></span>](https://www.microsoft.com/typography/otspec/)
-   [<span data-ttu-id="4f3c0-129">DWRITE \_ , \_ structure des métriques de police</span><span class="sxs-lookup"><span data-stu-id="4f3c0-129">DWRITE\_FONT\_METRICS structure</span></span>](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [<span data-ttu-id="4f3c0-130">TEXTMETRIC, structure</span><span class="sxs-lookup"><span data-stu-id="4f3c0-130">TEXTMETRIC Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 