---
title: Noms de Version-Independent WFP et ciblant des versions spécifiques de Windows
description: Dans de nombreux cas, l’API WFP (Windows Filtering Platform) fournit plusieurs versions d’une fonction ou d’une structure.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509368"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a><span data-ttu-id="3e960-103">Noms de Version-Independent WFP et ciblant des versions spécifiques de Windows</span><span class="sxs-lookup"><span data-stu-id="3e960-103">WFP Version-Independent Names and Targeting Specific Versions of Windows</span></span>

<span data-ttu-id="3e960-104">Dans de nombreux cas, l’API WFP (Windows Filtering Platform) fournit plusieurs versions d’une fonction ou d’une structure.</span><span class="sxs-lookup"><span data-stu-id="3e960-104">In many cases, the Windows Filtering Platform (WFP) API provides more than one version of a function or structure.</span></span>

<span data-ttu-id="3e960-105">La plupart des noms de données et de fonctions dans l’API WFP se terminent par un numéro de version, tel que « 0 » ou « 1 », même s’il n’y a qu’une seule version.</span><span class="sxs-lookup"><span data-stu-id="3e960-105">Most data and function names in the WFP API end with a version number, such as "0" or "1", even if there is only one version.</span></span>

## <a name="version-mapping-in-fwpvih"></a><span data-ttu-id="3e960-106">Mappage de version dans fwpvi. h</span><span class="sxs-lookup"><span data-stu-id="3e960-106">Version Mapping in fwpvi.h</span></span>

<span data-ttu-id="3e960-107">Le fichier d’en-tête fwpvi. h est inclus à partir du kit de développement logiciel (SDK) Windows 7 et de WDK.</span><span class="sxs-lookup"><span data-stu-id="3e960-107">The fwpvi.h header file is included starting with the Windows 7 SDK and WDK.</span></span> <span data-ttu-id="3e960-108">Ce fichier d’en-tête mappe le nom de l’API sans version à la version appropriée pour une utilisation avec un système d’exploitation donné.</span><span class="sxs-lookup"><span data-stu-id="3e960-108">This header file maps the versionless API name to the version that is appropriate for use with a given operating system.</span></span>

<span data-ttu-id="3e960-109">Par exemple, voici un bref extrait de la version de fwpvi. h inclus dans le kit de développement logiciel (SDK) Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e960-109">For example, here is a brief excerpt from the version of fwpvi.h included in the Windows 8 SDK.</span></span>


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



<span data-ttu-id="3e960-110">Comme indiqué ci-dessus, il n’existe qu’une seule version de **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) : tout appel à **FwpmNetEventCreateEnumHandle** appellera toujours **FwpmNetEventCreateEnumHandle0**, quel que soit le système d’exploitation ciblé.</span><span class="sxs-lookup"><span data-stu-id="3e960-110">As shown above, there is only one version of **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – so any call to **FwpmNetEventCreateEnumHandle** will always call **FwpmNetEventCreateEnumHandle0**, regardless of the operating system targeted.</span></span>

<span data-ttu-id="3e960-111">Toutefois, il existe trois versions de **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)et [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span><span class="sxs-lookup"><span data-stu-id="3e960-111">However, there are three versions of of **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1), and [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span></span> <span data-ttu-id="3e960-112">Le fichier d’en-tête fwpvi. h garantit qu’un appel à **FwpmNetEventEnum** appellera la version la plus appropriée pour le système d’exploitation ciblé :</span><span class="sxs-lookup"><span data-stu-id="3e960-112">The fwpvi.h header file ensures that a call to **FwpmNetEventEnum** will call the version most appropriate to the targeted operating system:</span></span>

-   <span data-ttu-id="3e960-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) pour Windows 8 (ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="3e960-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) for Windows 8 (or later)</span></span>
-   <span data-ttu-id="3e960-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) pour Windows 7 est ciblé</span><span class="sxs-lookup"><span data-stu-id="3e960-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) for Windows 7 is targeted</span></span>
-   <span data-ttu-id="3e960-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) pour les systèmes d’exploitation antérieurs (tels que Windows Vista ou Windows Vista avec Service Pack 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="3e960-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) for earlier operating systems (such as Windows Vista or Windows Vista with Service Pack 1 (SP1))</span></span>

## <a name="calling-version-independent-functions-and-structures"></a><span data-ttu-id="3e960-116">Appel de fonctions et de structures Version-Independent</span><span class="sxs-lookup"><span data-stu-id="3e960-116">Calling Version-Independent Functions and Structures</span></span>

<span data-ttu-id="3e960-117">Les développeurs WFP ciblant une version de système d’exploitation ou WDK particulière sont encouragés à toujours programmer les macros indépendantes de la version.</span><span class="sxs-lookup"><span data-stu-id="3e960-117">WFP developers targeting a particular operating system or WDK version are encouraged to always program against the version-independent macros.</span></span> <span data-ttu-id="3e960-118">Cette opération sélectionne automatiquement la dernière version prise en charge dans le système d’exploitation que vous ciblez.</span><span class="sxs-lookup"><span data-stu-id="3e960-118">This will automatically select the latest version supported in the operating system you are targeting.</span></span> <span data-ttu-id="3e960-119">L’utilisation des fichiers d’en-tête les plus récents est recommandée, même lorsque vous ciblez un système d’exploitation antérieur.</span><span class="sxs-lookup"><span data-stu-id="3e960-119">Use of the most recent header files is recommended, even when targeting an earlier operating system.</span></span> <span data-ttu-id="3e960-120">Cela permet de garantir que la dernière version prise en charge est utilisée et peut également faciliter la maintenance et la mise à jour de votre code.</span><span class="sxs-lookup"><span data-stu-id="3e960-120">Doing this consistently will ensure the latest supported version is used, and can also make it easier to maintain and update your code.</span></span>

<span data-ttu-id="3e960-121">La [documentation de référence sur les API WFP](fwp-reference.md) décrit chaque version d’une API numérotée.</span><span class="sxs-lookup"><span data-stu-id="3e960-121">The [WFP API reference documentation](fwp-reference.md) describes each version of a numbered API.</span></span> <span data-ttu-id="3e960-122">Si plusieurs versions existent, le système d’exploitation ciblé est noté.</span><span class="sxs-lookup"><span data-stu-id="3e960-122">If more than one version exists, the targeted operating system is noted.</span></span> <span data-ttu-id="3e960-123">Toutefois, les développeurs veulent généralement appeler les API indépendantes de la version (sans nombre) et indiquer le système d’exploitation ciblé (tel que **NTDDI \_ win6** pour Windows Vista ou **NTDDI \_ WIN8** pour Windows 8).</span><span class="sxs-lookup"><span data-stu-id="3e960-123">However, developers will generally want to call the version-independent (numberless) APIs, and indicate the targeted operating system (such as **NTDDI\_WIN6** for Windows Vista or **NTDDI\_WIN8** for Windows 8).</span></span>

<span data-ttu-id="3e960-124">Pour garantir une gestion correcte des fonctions qui acceptent des paramètres différents dans différentes versions, vous pouvez inclure des blocs conditionnels tels que `#if (NTDDI_VERSION >= NTDDI_WIN7)` .</span><span class="sxs-lookup"><span data-stu-id="3e960-124">To ensure proper handling of functions that take different parameters in different versions, you can include conditional blocks such as `#if (NTDDI_VERSION >= NTDDI_WIN7)`.</span></span>

 

 




