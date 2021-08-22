---
description: Une fois que vous avez créé une DLL, vous pouvez utiliser les fonctions qu’elle définit dans une application. Voici une application console simple qui utilise la fonction myPuts exportée à partir de Myputs.dll (consultez Création d’une bibliothèque de Dynamic-Link simple).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Utilisation de la liaison dynamique Load-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 106d9d73808b56c664e44d8dcd71b74a65431316fd3daf47dd0736596c5aa5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902369"
---
# <a name="using-load-time-dynamic-linking"></a>Utilisation de la liaison dynamique Load-Time

Une fois que vous avez créé une DLL, vous pouvez utiliser les fonctions qu’elle définit dans une application. Voici une application console simple qui utilise la fonction myPuts exportée à partir de Myputs.dll (consultez [création d’une bibliothèque de Dynamic-Link simple](creating-a-simple-dynamic-link-library.md)).

Étant donné que cet exemple appelle la fonction DLL explicitement, le module de l’application doit être lié à la bibliothèque d’importation Myputs. lib. Pour plus d’informations sur la création de dll, consultez la documentation fournie avec vos outils de développement.


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liaison dynamique au moment du chargement](load-time-dynamic-linking.md)
</dt> </dl>

 

 



