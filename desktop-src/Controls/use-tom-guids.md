---
title: Utilisation des GUID TOM
description: Les GUID TOM (Text Object Model) sont fournis dans Tom. h à l’intérieur des \_ instructions d’interface MIDL. Pour utiliser les interfaces associées, vous devez d’abord déclarer l’interface à l’aide du GUID.
ms.assetid: 48FF98C9-D42E-4E7F-874F-8E56F730E24E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c937d8b3c3612a3a49f27f18ac7c392b7a596
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104462811"
---
# <a name="how-to-use-tom-guids"></a><span data-ttu-id="d2acc-104">Utilisation des GUID TOM</span><span class="sxs-lookup"><span data-stu-id="d2acc-104">How to Use TOM GUIDs</span></span>

<span data-ttu-id="d2acc-105">Les GUID TOM (Text Object Model) sont fournis dans Tom. h à l’intérieur des \_ instructions d’interface MIDL.</span><span class="sxs-lookup"><span data-stu-id="d2acc-105">Text Object Model (TOM) GUIDs are given in Tom.h inside the MIDL\_INTERFACE statements.</span></span> <span data-ttu-id="d2acc-106">Pour utiliser les interfaces associées, vous devez d’abord déclarer l’interface à l’aide du GUID.</span><span class="sxs-lookup"><span data-stu-id="d2acc-106">To use the associated interfaces, you must first declare the interface by using the GUID.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d2acc-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="d2acc-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d2acc-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="d2acc-108">Technologies</span></span>

-   [<span data-ttu-id="d2acc-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="d2acc-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d2acc-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="d2acc-110">Prerequisites</span></span>

-   <span data-ttu-id="d2acc-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d2acc-111">C/C++</span></span>
-   <span data-ttu-id="d2acc-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="d2acc-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d2acc-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="d2acc-113">Instructions</span></span>

### <a name="use-a-tom-guid"></a><span data-ttu-id="d2acc-114">Utiliser un GUID TOM</span><span class="sxs-lookup"><span data-stu-id="d2acc-114">Use a TOM GUID</span></span>

<span data-ttu-id="d2acc-115">L’exemple de code suivant montre comment utiliser l’interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) .</span><span class="sxs-lookup"><span data-stu-id="d2acc-115">The following example code demonstrates how to use the [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) interface.</span></span>


```C++
#define DEFINE_GUIDXXX(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8) \
        EXTERN_C const GUID CDECL name \
                = { l, w1, w2, { b1, b2,  b3,  b4,  b5,  b6,  b7,  b8 } }

DEFINE_GUIDXXX(IID_ITextDocument,0x8CC497C0,0xA1DF,0x11CE,0x80,0x98,
                0x00,0xAA,0x00,0x47,0xBE,0x5D);
```



## <a name="related-topics"></a><span data-ttu-id="d2acc-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2acc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2acc-117">Utilisation du modèle d’objet de texte</span><span class="sxs-lookup"><span data-stu-id="d2acc-117">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="d2acc-118">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="d2acc-118">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="d2acc-119">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="d2acc-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




