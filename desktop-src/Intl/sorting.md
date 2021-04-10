---
description: Pour NLS, le tri (également connu sous le nom de &\# 0034 ; collation&\# 0034 ;) est la disposition des chaînes.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Tri (internationalisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210793"
---
# <a name="sorting"></a><span data-ttu-id="15032-103">Tri</span><span class="sxs-lookup"><span data-stu-id="15032-103">Sorting</span></span>

<span data-ttu-id="15032-104">Pour NLS, le tri (également appelé « classement ») est la disposition des chaînes.</span><span class="sxs-lookup"><span data-stu-id="15032-104">For NLS, sorting (also known as "collation") is the arrangement of strings.</span></span> <span data-ttu-id="15032-105">Il existe deux types de tri :</span><span class="sxs-lookup"><span data-stu-id="15032-105">There are two types of sorting:</span></span>

-   <span data-ttu-id="15032-106">Tri linguistique.</span><span class="sxs-lookup"><span data-stu-id="15032-106">Linguistic sorting.</span></span> <span data-ttu-id="15032-107">Réorganise les chaînes avec des caractéristiques linguistiques similaires en groupes (par tris).</span><span class="sxs-lookup"><span data-stu-id="15032-107">Arranges strings with similar linguistic characteristics into groups (by sorts).</span></span>
-   <span data-ttu-id="15032-108">Tri ordinal (non linguistique).</span><span class="sxs-lookup"><span data-stu-id="15032-108">Ordinal (non-linguistic) sorting.</span></span> <span data-ttu-id="15032-109">Réorganise les chaînes dans une séquence ordonnée.</span><span class="sxs-lookup"><span data-stu-id="15032-109">Arranges the strings in an ordered sequence.</span></span>

<span data-ttu-id="15032-110">Le tri utilise les fonctions de comparaison de chaînes NLS, telles que [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) et [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), ou les fonctions d’API « Wrapper », telles que [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), qui appellent en interne les fonctions de comparaison de chaînes nls.</span><span class="sxs-lookup"><span data-stu-id="15032-110">Sorting uses the NLS string comparison functions, such as [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) and [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), or "wrapper" API functions, such as [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), that internally call the NLS string comparison functions.</span></span>

<span data-ttu-id="15032-111">Pour plus d’informations sur l’implémentation du tri dans vos applications, consultez [gestion du tri dans vos applications](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="15032-111">For details about implementing sorting in your applications, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="15032-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15032-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15032-113">À propos de la prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="15032-113">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="15032-114">Gestion du tri dans vos applications</span><span class="sxs-lookup"><span data-stu-id="15032-114">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="15032-115">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="15032-115">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[<span data-ttu-id="15032-116">LCMapString</span><span class="sxs-lookup"><span data-stu-id="15032-116">LCMapString</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
