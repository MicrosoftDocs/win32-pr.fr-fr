---
title: Utilisation des GUID TOM
description: Les GUID TOM (Text Object Model) sont fournis dans Tom. h à l’intérieur des \_ instructions d’interface MIDL. Pour utiliser les interfaces associées, vous devez d’abord déclarer l’interface à l’aide du GUID.
ms.assetid: 48FF98C9-D42E-4E7F-874F-8E56F730E24E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c937d8b3c3612a3a49f27f18ac7c392b7a596
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115329"
---
# <a name="how-to-use-tom-guids"></a>Utilisation des GUID TOM

Les GUID TOM (Text Object Model) sont fournis dans Tom. h à l’intérieur des \_ instructions d’interface MIDL. Pour utiliser les interfaces associées, vous devez d’abord déclarer l’interface à l’aide du GUID.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="use-a-tom-guid"></a>Utiliser un GUID TOM

L’exemple de code suivant montre comment utiliser l’interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) .


```C++
#define DEFINE_GUIDXXX(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8) \
        EXTERN_C const GUID CDECL name \
                = { l, w1, w2, { b1, b2,  b3,  b4,  b5,  b6,  b7,  b8 } }

DEFINE_GUIDXXX(IID_ITextDocument,0x8CC497C0,0xA1DF,0x11CE,0x80,0x98,
                0x00,0xAA,0x00,0x47,0xBE,0x5D);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du modèle d’objet de texte](using-the-text-object-model.md)
</dt> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




