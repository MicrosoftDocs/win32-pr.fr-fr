---
description: La fonction ShowJavaConsole est une aide au débogage pour les développeurs Java. Les applets (ou tout autre code Java) s’exécutant dans Internet Explorer peuvent l’utiliser pour afficher des messages d’erreur et d’autres informations.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: ShowJavaConsole fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540468"
---
# <a name="showjavaconsole-function"></a>ShowJavaConsole fonction)

La fonction **ShowJavaConsole** est une aide au débogage pour les développeurs Java. Les applets (ou tout autre code Java) s’exécutant dans Internet Explorer peuvent l’utiliser pour afficher des messages d’erreur et d’autres informations.

## <a name="syntax"></a>Syntaxe


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

<dl></dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

L’appel de **ShowJavaConsole** entraîne l’affichage de la fenêtre de la console Java par la machine virtuelle Java. La fenêtre de la console Java elle-même peut afficher la sortie du débogage à partir du code Java qui s’exécute dans le processus appelant. En règle générale, cela ne peut être utilisé que par une application hébergeant la machine virtuelle Java. Il n’existe qu’une seule fenêtre de console Java par processus. plusieurs appels à l’API entraînent l’affichage de la même fenêtre. En d’autres termes, si la fenêtre de console est déjà affichée, rien ne se produit. Si la fenêtre n’a pas été affichée ou si l’utilisateur l’a fermée, la fenêtre s’affiche.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
