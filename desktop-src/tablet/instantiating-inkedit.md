---
description: Cette rubrique décrit les différentes façons dont vous pouvez instancier un contrôle InkEdit.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Instanciation de InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde7e94566b076a4d9d6f6928fc08199ee71fa19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485193"
---
# <a name="instantiating-inkedit"></a><span data-ttu-id="d3320-103">Instanciation de InkEdit</span><span class="sxs-lookup"><span data-stu-id="d3320-103">Instantiating InkEdit</span></span>

<span data-ttu-id="d3320-104">Cette rubrique décrit les différentes façons dont vous pouvez instancier un contrôle [InkEdit](inkedit-control.md) .</span><span class="sxs-lookup"><span data-stu-id="d3320-104">This topic describes the various ways that you can instantiate an [InkEdit](inkedit-control.md) control.</span></span>

## <a name="visual-basic-net-and-c"></a><span data-ttu-id="d3320-105">Visual Basic .NET et C\#</span><span class="sxs-lookup"><span data-stu-id="d3320-105">Visual Basic .NET and C\#</span></span>

<span data-ttu-id="d3320-106">Si vous utilisez Microsoft Visual Basic .NET ou C \# , faites glisser le contrôle [InkEdit](./inkedit-control.md) de la boîte à outils dans Visual Studio vers le formulaire ou la page où vous souhaitez que le contrôle apparaisse.</span><span class="sxs-lookup"><span data-stu-id="d3320-106">If you are working with Microsoft Visual Basic .NET or C\#, drag the [InkEdit](./inkedit-control.md) control from the Toolbox in Visual Studio to the form or page where you want the control to appear.</span></span>

## <a name="win32c"></a><span data-ttu-id="d3320-107">Win32/C++</span><span class="sxs-lookup"><span data-stu-id="d3320-107">Win32/C++</span></span>

<span data-ttu-id="d3320-108">Le contrôle [InkEdit](inkedit-control-reference.md) est une superclasse du contrôle Rich Edit 4,5 Win32 OLE incorporable.</span><span class="sxs-lookup"><span data-stu-id="d3320-108">The [InkEdit](inkedit-control-reference.md) control is a superclass of the Rich Edit 4.5 Win32 OLE embeddable control.</span></span>

<span data-ttu-id="d3320-109">Les applications Win32 instancient le contrôle [InkEdit](inkedit-control-reference.md) en appelant [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) et en passant InkEdit en tant que classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d3320-109">Win32 applications instantiate the [InkEdit](inkedit-control-reference.md) control by calling [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) and passing INKEDIT as the window class.</span></span> <span data-ttu-id="d3320-110">INKEDIT est défini dans le. h.</span><span class="sxs-lookup"><span data-stu-id="d3320-110">INKEDIT is defined in InkEd.h.</span></span> <span data-ttu-id="d3320-111">Une fois le contrôle créé, vous pouvez « parler » au contrôle avec des messages.</span><span class="sxs-lookup"><span data-stu-id="d3320-111">After the control is created, you can "talk" to the control with messages.</span></span> <span data-ttu-id="d3320-112">Les messages Rich Edit (EM \_ \* ) sont transmis de l’instruction InkEdit à la modification enrichie non modifiée ; toutes les fonctionnalités de modification enrichies existantes sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="d3320-112">Rich Edit messages (EM\_\*) are passed from InkEdit to Rich Edit unaltered; all of the existing Rich Edit functionality is available.</span></span>

<span data-ttu-id="d3320-113">Pour créer un contrôle [InkEdit](inkedit-control-reference.md) , appelez la fonction [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) , en spécifiant la classe de fenêtre InkEdit.</span><span class="sxs-lookup"><span data-stu-id="d3320-113">To create an [InkEdit](inkedit-control-reference.md) control, call the [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) function, specifying the InkEdit window class.</span></span> <span data-ttu-id="d3320-114">Utilisez [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour inscrire InkEd.dll.</span><span class="sxs-lookup"><span data-stu-id="d3320-114">Use [LoadLibrary()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to register InkEd.dll.</span></span> <span data-ttu-id="d3320-115">Spécifiez la \_ constante définie de la classe INKEDIT pour le paramètre de classe de fenêtre et utilisez les styles de fenêtre comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="d3320-115">Specify the INKEDIT\_CLASS defined constant for the window class parameter and use the window styles as specified in the following examples.</span></span>

### <a name="instantiating-a-multiline-inkedit-control"></a><span data-ttu-id="d3320-116">Instanciation d’un contrôle InkEdit multiligne</span><span class="sxs-lookup"><span data-stu-id="d3320-116">Instantiating a Multiline InkEdit Control</span></span>


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER|ES_MULTILINE,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



### <a name="instantiating-a-single-line-inkedit-control"></a><span data-ttu-id="d3320-117">Instanciation d’un contrôle Single-Line InkEdit</span><span class="sxs-lookup"><span data-stu-id="d3320-117">Instantiating a Single-Line InkEdit Control</span></span>


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



> [!Note]  
> <span data-ttu-id="d3320-118">Contrairement à RichEdit, vous devez vous assurer d’appeler [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) avant de créer le contrôle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="d3320-118">Unlike with RichEdit, you must be sure to call [CoInitialize()](/windows/win32/api/objbase/nf-objbase-coinitialize) before creating the [InkEdit](inkedit-control-reference.md) control.</span></span> <span data-ttu-id="d3320-119">Appelez [CoUninitialize ()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) lorsque votre application s’arrête.</span><span class="sxs-lookup"><span data-stu-id="d3320-119">Call [CoUninitialize()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) when your application shuts down.</span></span> <span data-ttu-id="d3320-120">Après avoir appelé CoUninitialize (), vous devez appeler [FreeLibrary (s \_ hLib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) pour décrémenter le nombre de références sur le fichier InkEdit.dll.</span><span class="sxs-lookup"><span data-stu-id="d3320-120">After calling CoUninitialize(), you must call [FreeLibrary(s\_hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) to decrement the reference count on the InkEdit.dll file.</span></span>

 

<span data-ttu-id="d3320-121">Si vous utilisez le style de fenêtre [es \_ NOIME](../controls/rich-edit-control-styles.md) , la prise en charge de la correction intégrée n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d3320-121">If you use the [ES\_NOIME](../controls/rich-edit-control-styles.md) window style, the built-in correction support is not available.</span></span> <span data-ttu-id="d3320-122">Si vous ne spécifiez pas de fenêtre parente, le contrôle est créé comme une fenêtre de niveau supérieur et le \_ style WS SYSMENU est ajouté ; cela désactive également la prise en charge de la correction intégrée.</span><span class="sxs-lookup"><span data-stu-id="d3320-122">If you don't specify a parent window, the control is created as a top-level window and the WS\_SYSMENU style is added; this also disables the built-in correction support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3320-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3320-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3320-124">Ajout de contrôles Ink à un projet</span><span class="sxs-lookup"><span data-stu-id="d3320-124">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
