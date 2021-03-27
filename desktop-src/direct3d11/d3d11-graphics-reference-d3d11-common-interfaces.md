---
title: Interfaces de version courantes
description: Cette section contient des informations sur les interfaces de version courantes.
ms.assetid: d228c3c2-e2ff-4723-aec1-5c3ce82c321d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f535650fa24593cc4b663c1a2b01a1a2d53a9b3b
ms.sourcegitcommit: 8f833c83be1accc119cc57e67b608ffe1e0159b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2020
ms.locfileid: "103734684"
---
# <a name="common-version-interfaces"></a><span data-ttu-id="87419-103">Interfaces de version courantes</span><span class="sxs-lookup"><span data-stu-id="87419-103">Common version interfaces</span></span>

<span data-ttu-id="87419-104">Cette section contient des informations sur les interfaces de version courantes.</span><span class="sxs-lookup"><span data-stu-id="87419-104">This section contains information about the common version interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="87419-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="87419-105">In this section</span></span>

| <span data-ttu-id="87419-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="87419-106">Topic</span></span> | <span data-ttu-id="87419-107">Description</span><span class="sxs-lookup"><span data-stu-id="87419-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="87419-108">**ID3D10Blob**</span><span class="sxs-lookup"><span data-stu-id="87419-108">**ID3D10Blob**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3d10blob) | <span data-ttu-id="87419-109">Cette interface est utilisée pour retourner des données de longueur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="87419-109">This interface is used to return arbitrary-length data.</span></span> |
| <span data-ttu-id="87419-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87419-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span> | <span data-ttu-id="87419-111">Cette interface est utilisée pour retourner des données de longueur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="87419-111">This interface is used to return data of arbitrary length.</span></span> |
| [<span data-ttu-id="87419-112">**ID3DDestructionNotifier**</span><span class="sxs-lookup"><span data-stu-id="87419-112">**ID3DDestructionNotifier**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier) | <span data-ttu-id="87419-113">Utilisé pour enregistrer les rappels lorsqu’un objet nano-COM direct 3D est détruit.</span><span class="sxs-lookup"><span data-stu-id="87419-113">Used to register for callbacks when a Direct 3D nano-COM object is destroyed.</span></span> |
| [<span data-ttu-id="87419-114">**ID3DInclude**</span><span class="sxs-lookup"><span data-stu-id="87419-114">**ID3DInclude**</span></span>](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) | <span data-ttu-id="87419-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) est une interface include que l’utilisateur implémente pour permettre à une application d’appeler des méthodes substituables par l’utilisateur pour l’ouverture et la fermeture des \# fichiers include du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="87419-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader \#include files.</span></span> |
| [<span data-ttu-id="87419-116">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="87419-116">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) | <span data-ttu-id="87419-117">L’interface [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) permet à une application de décrire des sections conceptuelles et des marqueurs dans le workflow de code de l’application.</span><span class="sxs-lookup"><span data-stu-id="87419-117">The [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) interface enables an application to describe conceptual sections and markers within the application's code flow.</span></span> <span data-ttu-id="87419-118">Un outil correctement activé, tel que Microsoft Visual Studio Ultimate 2012, peut afficher les sections et les marqueurs visuellement le long de la ligne de temps Microsoft Direct3D de l’outil, tandis que l’outil débogue l’application.</span><span class="sxs-lookup"><span data-stu-id="87419-118">An appropriately enabled tool, such as Microsoft Visual Studio Ultimate 2012, can display these sections and markers visually along the tool's Microsoft Direct3D time line, while the tool debugs the application.</span></span> <span data-ttu-id="87419-119">Ces notes visuelles permettent aux utilisateurs d’un tel outil de naviguer vers des parties de la chronologie qui présentent un intérêt, ou de comprendre l’ensemble des appels Direct3D générés par certaines sections du code de l’application.</span><span class="sxs-lookup"><span data-stu-id="87419-119">These visual notes allow users of such a tool to navigate to parts of the time line that are of interest, or to understand what set of Direct3D calls are produced by certain sections of the application's code.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="87419-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87419-120">Related topics</span></span>

[<span data-ttu-id="87419-121">Référence de version commune</span><span class="sxs-lookup"><span data-stu-id="87419-121">Common version reference</span></span>](d3d11-graphics-reference-d3d11-common.md)
