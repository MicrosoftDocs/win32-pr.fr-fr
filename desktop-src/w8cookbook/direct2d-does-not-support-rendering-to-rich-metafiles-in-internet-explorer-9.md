---
title: Direct2D ne prend pas en charge le rendu des sous-fichiers enrichis dans Internet Explorer 9
description: Direct2D ne prend pas en charge le rendu des sous-fichiers enrichis dans Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314822"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a><span data-ttu-id="a0322-103">Direct2D ne prend pas en charge le rendu des sous-fichiers enrichis dans Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="a0322-103">Direct2D does not support rendering to rich metafiles in Internet Explorer 9</span></span>

## <a name="platforms"></a><span data-ttu-id="a0322-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="a0322-104">Platforms</span></span>

<span data-ttu-id="a0322-105">**Clients** – Windows Vista, Windows 7, Windows 8</span><span class="sxs-lookup"><span data-stu-id="a0322-105">**Clients** – Windows Vista, Windows 7, Windows 8</span></span>  
<span data-ttu-id="a0322-106">**Serveurs** – windows Server 2008, windows Server 2008 R2, windows server 2012</span><span class="sxs-lookup"><span data-stu-id="a0322-106">**Servers** – Windows Server 2008, Windows Server 2008 R2, Windows Server 2012</span></span>  




## <a name="description"></a><span data-ttu-id="a0322-107">Description</span><span class="sxs-lookup"><span data-stu-id="a0322-107">Description</span></span>

<span data-ttu-id="a0322-108">En raison des modifications de rendu internes dans Internet Explorer 9, les API brutes [IHTMLElementRender ::D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) et [IViewObject ::D](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) créent désormais un métafichier contenant une seule bitmap qui représente le contenu Web au lieu d’un métafichier riche contenant du texte et des informations vectorielles.</span><span class="sxs-lookup"><span data-stu-id="a0322-108">Due to internal rendering changes in Internet Explorer 9, the [IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) and [IViewObject::Draw](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) APIs will now create a metafile containing a single bitmap that represents the web content instead of a rich metafile containing text and vector info.</span></span> <span data-ttu-id="a0322-109">Cette modification est due au passage du rendu GDI au rendu de Direct2D à accélération matérielle (D2D).</span><span class="sxs-lookup"><span data-stu-id="a0322-109">This change was due to the move from GDI rendering to hardware-accelerated Direct2D (D2D) rendering.</span></span>

<span data-ttu-id="a0322-110">Cette modification affecte les applications qui utilisent ces API et s’appuie sur du texte ou des informations vectorielles dans le métafichier.</span><span class="sxs-lookup"><span data-stu-id="a0322-110">This change affects apps that use these APIs and rely on text or vector info in the metafile.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a0322-111">Manifestation</span><span class="sxs-lookup"><span data-stu-id="a0322-111">Manifestation</span></span>

<span data-ttu-id="a0322-112">En fonction de l’application affectée par cette modification, les utilisateurs peuvent constater un comportement incorrect ou rompu dans leurs applications.</span><span class="sxs-lookup"><span data-stu-id="a0322-112">Depending on the app that is affected by this change, users might see broken or incorrect behavior in their apps.</span></span>

## <a name="mitigation"></a><span data-ttu-id="a0322-113">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="a0322-113">Mitigation</span></span>

<span data-ttu-id="a0322-114">Les applications qui ont uniquement besoin d’extraire des informations textuelles d’un document Web (sans informations de positionnement) peuvent utiliser la propriété [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) pour extraire du texte.</span><span class="sxs-lookup"><span data-stu-id="a0322-114">Apps that only need to extract text info from a web document (without positioning info) can use the [innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) property to extract text.</span></span>

<span data-ttu-id="a0322-115">Les applications qui utilisent IViewObject ::D RAW peuvent utiliser la [fonctionnalité \_ IVIEWOBJECTDRAW \_ DMLT9 \_ avec \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) la clé de contrôle de fonctionnalité GDI pour revenir au rendu GDI si le mode de document :</span><span class="sxs-lookup"><span data-stu-id="a0322-115">Apps that use IViewObject::Draw can use the [FEATURE\_IVIEWOBJECTDRAW\_DMLT9\_WITH\_GDI](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) feature control key to revert to GDI rendering if the document mode:</span></span>

-   <span data-ttu-id="a0322-116">Est inférieur ou égal à 8</span><span class="sxs-lookup"><span data-stu-id="a0322-116">Is less or equal to 8</span></span>
-   <span data-ttu-id="a0322-117">Le FCK autorise cet hôte à utiliser GDI</span><span class="sxs-lookup"><span data-stu-id="a0322-117">The FCK authorizes that host to use GDI</span></span>
-   <span data-ttu-id="a0322-118">Et un contexte de périphérique de métafichier est transmis à l’API</span><span class="sxs-lookup"><span data-stu-id="a0322-118">And a metafile DC is passed to the API</span></span>

## <a name="resources"></a><span data-ttu-id="a0322-119">Ressources</span><span class="sxs-lookup"><span data-stu-id="a0322-119">Resources</span></span>

-   <span data-ttu-id="a0322-120">[IHTMLElementRender ::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0322-120">[IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span></span>
-   [<span data-ttu-id="a0322-121">IViewObject ::D RAW</span><span class="sxs-lookup"><span data-stu-id="a0322-121">IViewObject::Draw</span></span>](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   <span data-ttu-id="a0322-122">[IHTMLElement :: innerText, propriété](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0322-122">[IHTMLElement::innerText Property](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span></span>
-   <span data-ttu-id="a0322-123">[Contrôles de fonctionnalités Internet (I... Budget](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0322-123">[Internet Feature Controls (I..L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span></span>

 

 