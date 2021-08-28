---
description: handle d’une chaîne de Windows Runtime.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b43c92d439cec10c0d1683efb1e8ceafd8165a35c3c8aa9a1b35150e43a33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121569"
---
# <a name="hstring"></a>HSTRING

handle d’une chaîne de Windows Runtime.


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>Remarques

utilisez **HSTRING** pour représenter des chaînes immuables dans le Windows Runtime.

JavaScript et d’autres langages, tels que C \# et Microsoft Visual Basic, peuvent utiliser des chaînes qui sont représentées à l’aide de **HSTRING**. Le tableau suivant montre comment un **HSTRING** est représenté dans d’autres langues.



| Langage de programmation                                                                    | Représentation sous forme de chaîne                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | [WinRT :: hstring](/uwp/cpp-ref-for-winrt/hstring) , classe     |
| Extensions de composant Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx)) | [Platform :: String](/cpp/cppcx/platform-string-class) , classe |
| JavaScript                                                                              | String (objet)                                              |
| .NET Framework                                                                          | System. String (classe)                                        |



 

Le descripteur **HSTRING** est un type de handle standard. Sémantiquement, un **HSTRING** contenant la valeur **null** représente la chaîne vide, qui se compose de caractères de contenu nuls et d’un caractère **null** de fin. La création d’une chaîne via [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) avec zéro caractère génère la valeur de handle **null**. Lors de l’appel de [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) avec la valeur **null**, un pointeur vers une chaîne vide, suivi uniquement par le caractère de fin **nul** , est retourné. Il n’existe aucune valeur distincte pour représenter un **HSTRING** qui n’est pas initialisé.

Appelez la fonction [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) pour créer un **HSTRING**, puis appelez la fonction [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) pour libérer la référence à la mémoire des chaînes de sauvegarde. Appelez la fonction [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) pour créer une référence de chaîne, qui est également appelée une *chaîne de passe rapide*.

Copiez un **HSTRING** en appelant la fonction [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) .

Concaténer deux chaînes en appelant la fonction [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) .

Accédez à la mémoire de la chaîne de sauvegarde en appelant la fonction [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) .

**HSTRING** peut stocker et utiliser des caractères **null** incorporés. Utilisez la fonction [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) pour rechercher les caractères **null** incorporés avant d’utiliser des fonctions qui peuvent produire des résultats inattendus. par exemple, la plupart des fonctions Windows utilisent **LPCWSTR** comme paramètre d’entrée, et elles calculent la longueur de la chaîne uniquement jusqu’à ce que la première valeur **null** soit rencontrée.

La chaîne de sauvegarde doit rester immuable et se terminer par null. Lorsque le code appelant crée une référence de chaîne à l’aide de la fonction [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , la mémoire qui contient la représentation sous forme de chaîne de stockage appartient à l’appelant. le Windows Runtime s’appuie sur le contenu de la chaîne d’origine pour rester inchangé. lors du passage d’une référence de chaîne dans le Windows Runtime, il incombe à l’appelant de s’assurer que le contenu de la chaîne est invariable et que **NUL** se termine pendant la durée de l’appel. le Windows Runtime libère toutes les références à la référence de chaîne lorsque l’appel est retourné.

Quand vous recevez un **HSTRING** en tant que paramètre de sortie, il est recommandé de définir le handle sur la **valeur null** lorsque vous n’en avez plus besoin.

Appelez la fonction [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) pour allouer une mémoire tampon de chaîne mutable que vous pouvez utiliser pour créer un **HSTRING** immuable. Lorsque vous avez terminé de remplir la mémoire tampon, vous appelez la fonction [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) pour créer le **HSTRING**. Ce modèle de construction en deux phases active une fonctionnalité similaire à un « générateur de chaîne ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Hstring. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>


</dt> <dt>

[**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
