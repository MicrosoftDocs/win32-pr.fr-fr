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
# <a name="instantiating-inkedit"></a>Instanciation de InkEdit

Cette rubrique décrit les différentes façons dont vous pouvez instancier un contrôle [InkEdit](inkedit-control.md) .

## <a name="visual-basic-net-and-c"></a>Visual Basic .NET et C\#

Si vous utilisez Microsoft Visual Basic .NET ou C \# , faites glisser le contrôle [InkEdit](./inkedit-control.md) de la boîte à outils dans Visual Studio vers le formulaire ou la page où vous souhaitez que le contrôle apparaisse.

## <a name="win32c"></a>Win32/C++

Le contrôle [InkEdit](inkedit-control-reference.md) est une superclasse du contrôle Rich Edit 4,5 Win32 OLE incorporable.

Les applications Win32 instancient le contrôle [InkEdit](inkedit-control-reference.md) en appelant [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) et en passant InkEdit en tant que classe de fenêtre. INKEDIT est défini dans le. h. Une fois le contrôle créé, vous pouvez « parler » au contrôle avec des messages. Les messages Rich Edit (EM \_ \* ) sont transmis de l’instruction InkEdit à la modification enrichie non modifiée ; toutes les fonctionnalités de modification enrichies existantes sont disponibles.

Pour créer un contrôle [InkEdit](inkedit-control-reference.md) , appelez la fonction [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) , en spécifiant la classe de fenêtre InkEdit. Utilisez [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour inscrire InkEd.dll. Spécifiez la \_ constante définie de la classe INKEDIT pour le paramètre de classe de fenêtre et utilisez les styles de fenêtre comme indiqué dans les exemples suivants.

### <a name="instantiating-a-multiline-inkedit-control"></a>Instanciation d’un contrôle InkEdit multiligne


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



### <a name="instantiating-a-single-line-inkedit-control"></a>Instanciation d’un contrôle Single-Line InkEdit


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
> Contrairement à RichEdit, vous devez vous assurer d’appeler [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) avant de créer le contrôle [InkEdit](inkedit-control-reference.md) . Appelez [CoUninitialize ()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) lorsque votre application s’arrête. Après avoir appelé CoUninitialize (), vous devez appeler [FreeLibrary (s \_ hLib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) pour décrémenter le nombre de références sur le fichier InkEdit.dll.

 

Si vous utilisez le style de fenêtre [es \_ NOIME](../controls/rich-edit-control-styles.md) , la prise en charge de la correction intégrée n’est pas disponible. Si vous ne spécifiez pas de fenêtre parente, le contrôle est créé comme une fenêtre de niveau supérieur et le \_ style WS SYSMENU est ajouté ; cela désactive également la prise en charge de la correction intégrée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ajout de contrôles Ink à un projet](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
