---
title: Marshaling des types de données OLE
description: Marshaling des types de données Automation et OLE.
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- MIDL et COM MIDL, marshaling de types de données OLE
- marshaling MIDL
- MIDL de données OLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970c6e0fef9d0fc88b8a0a11a087fa4396d7a7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093437"
---
# <a name="marshaling-ole-data-types"></a>Marshaling des types de données OLE

pour faciliter l’utilisation de certains types de données Automation et OLE, ainsi que certains handles système fréquemment utilisés dans COM, les typedefs pour ces types de données et leurs fonctions d’assistance associées sont disponibles en important des fichiers IDL Windows et en établissant une liaison avec les fichiers DLL OLE et Automation. Ces fichiers sont automatiquement installés sur votre système.

-   Pour utiliser le type de données [**BSTR**](/previous-versions/windows/desktop/automat/bstr) dans les appels de procédure distante, importez le fichier Wtypes. idl dans votre fichier de définition d’interface (IDL) et liez-le à oleaut32. lib lors de la génération de votre application distribuée. Cela permet à vos stubs d’utiliser les fonctions d’assistance prêtes à l’emploi **BSTR \_ Users**, BSTR **\_ UserMarshal**, **BSTR \_ UserUnmarshal** et **BSTR \_ UserFree**.
-   Pour utiliser d’autres types de données Automation, comme [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) et [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray), ou des types qui utilisent ces types (par exemple, [**DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) et [**EXCEPINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)), importez le fichier objidl. idl dans votre fichier IDL et liez-le à oleaut32. lib au moment de la génération. Cela vous permettra d’utiliser les routines d’assistance appropriées.
-   Pour utiliser des types de données OLE (tels que CLIPFORMAT, SNB, STGMEDIUM, ASYNC \_ STGMEDIUM) ou des handles du système (tels que HMETAFILE \_ PICT, HENHMETAFILE, HMETAFILE, HBITMAP, HPALETTE et HGLOBAL), importez le fichier objidl. idl dans votre fichier de définition d’interface et liez-le au moment de la génération.
-   Les handles OLE suivants sont également définis avec l’attribut **\[ Wire \_ Marshal \]** , mais uniquement en tant que handles dans un ordinateur, car ils ne peuvent pas être utilisés dans les appels de procédure distante à d’autres ordinateurs à l’heure actuelle : HWND, HMENU, HACCEL, HDC, Hfont, HICON, HBRUSH. Importez le fichier objidl. idl dans votre fichier IDL et liez-le à ole32. lib au moment de la génération pour utiliser ces handles dans la communication entre processus sur un ordinateur unique.

Pour plus d’informations, [consultez l' \_ attribut Wire Marshal](/windows/desktop/Rpc/the-wire-marshal-attribute), [la \_ fonction Users type](/windows/desktop/Rpc/the-type-usersize-function), [la fonction \_ UserMarshal](/windows/desktop/Rpc/the-type-usermarshal-function)de type, [la fonction \_ UserUnmarshal](/windows/desktop/Rpc/the-type-userunmarshal-function)de type, [la fonction \_ UserFree de type](/windows/desktop/Rpc/the-type-userfree-function)et les [stubs ciblant des plateformes 32 bits ou 64 bits spécifiques](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md).

 

 